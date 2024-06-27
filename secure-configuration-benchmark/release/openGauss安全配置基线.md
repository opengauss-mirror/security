# openGauss安全配置基线 v1.0

|版本|修订说明|修订时间|访问链接|
| ------------ | ------------ | ------------ | ------------ |
|1.0|初始修订|2024年06月|本文档|

## 连接配置

### OPENGAUSS.O_6.G_1.R_1：禁止侦听主机上所有IP地址

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_1

**规则名称:**
禁止侦听主机上所有IP地址

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

参数`listen_addresses`指定服务器在哪些TCP/IP地址上侦听客户端连接。侦听地址配置参数`listen_addresses`不允许包含表示所有IP地址的“*”或“0.0.0.0”或“::”字符串。对于包含多个网卡的主机，侦听所有IP地址将无法做到网络隔离，通过禁止侦听主机上所有IP地址可以阻止来自其他网络的恶意连接请求。

**影响:**
无

**检查方法:**

执行如下SQL语句检查参数`listen_addresses`配置，如果返回不为空则表示失败。

```sql
SELECT name,setting FROM pg_settings WHERE name = 'listen_addresses' AND
(position('*' in setting) OR position('0.0.0.0' in setting) OR position('::' in setting));
```

**修复方法:**

避免侦听主机上所有网卡地址，设置参数`listen_addresses`为“localhost”或需要接收业务请求的网卡IP地址，多个地址用逗号隔开，然后重启数据库。侦听地址以localhost和192.168.1.1为例命令如下。

```bash
gs_guc set -Z datanode -N all -I all -c "listen_addresses='localhost,192.168.1.1'"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无

### OPENGAUSS.O_6.G_1.R_2：确保对外服务端口使用非默认端口号


**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_2

**规则名称:**
确保对外服务端口使用非默认端口号

**级别:**
要求

**相关要求:**
无

**规则背景说明:**
参数`port`为数据库服务侦听的TCP端口号。采用默认端口号容易被恶意攻击者获取并攻击，需将对外服务端口号配置为非默认端口号。默认端口号请参考产品相关文档说明。

**影响:**

参数`port`由安装时的配置文件指定，请勿轻易修改，否则修改后会影响数据库正常通信。

**检查方法:**

以端口号5432为例，如果`port`参数值为默认端口号则失败。

```sql
SELECT name,setting FROM pg_settings WHERE name = 'port' AND setting = '5432';
```

**修复方法:**
用户需在安装数据库时通过配置文件指定各个实例的端口号。

**参考来源:**
无

### OPENGAUSS.O_6.G_1.R_3：确保数据库实例的最大连接数配置正确

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_3

**规则名称:**
确保数据库实例的最大连接数配置正确

**级别：**
要求

**相关要求：**
无

**规则背景说明:**：

参数`max_connections`控制数据库DN实例的最大连接数。参数设置过大可能引起数据库请求更多的System V共享内存或者信号量，导致超出操作系统默认配置允许的值。用户需要根据业务规格确定参数值的大小或咨询技术支持。

**影响：**

此参数会影响数据库的并发能力。

**检查方法：**

检查`max_connections`参数配置，用户需要根据业务规格确定配置多大并发连接数目。

```sql
openGauss=# show max_connections;
 max_connections
-----------------
 200
(1 row)
```

**修复方法：**

以配置最大连接数为200为例，通过如下命令修改参数 `max_connections`的值，然后重启数据库。

```bash
gs_guc set -Z datanode -N all -I all -c "max_connections=200"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无

### OPENGAUSS.O_6.G_1.R_4：确保Database的最大连接数配置正确

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_4

**规则名称:**
确保Database的最大连接数配置正确

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

为了控制访问数据库的会话数量，推荐配置会话数量限制在1024个以内。若设置参数`datconnlimit`为-1，表示不限制连接数据库的会话数量。

**影响:**

参数`datconnlimit`设置过小会影响数据库最大并发连接数，设置过大或不限制可能会由于会话数量超出系统负载能力，影响数据库的可用性。

**检查方法:**

执行如下SQL语句检查是否存在不限制连接数的数据库：

```sql
SELECT datname FROM pg_database WHERE datistemplate = false AND datconnlimit = -1;
```

**修复方法:**

```sql
UPDATE pg_database SET datconnlimit=<CONN_LIMIT_VALUE> WHERE datname=<DATABASE_NAME>;
```

其中`<CONN_LIMIT_VALUE>`表示设置的数据库允许的最大会话连接数，`<DATABASE_NAME>`为数据库名称。

**参考来源:**
无

### OPENGAUSS.O_6.G_1.R_5：确保系统管理员使用的连接数配置正确


**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_5

**规则名称:**
确保系统管理员使用的连接数配置正确

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

参数`sysadmin_reserved_connections`表示预留给数据库系统管理员的最少连接数，为系统管理员预留连接通道，避免连接被普通用户或恶意用户占用导致管理员无法连接。此参数值必须小于`max_connections`的值。

**影响:**
无

**检查方法:**

```sql
openGauss=# show sysadmin_reserved_connections;
sysadmin_reserved_connections
-------------------------------
3
(1 row)
```

**修复方法:**

修改参数`sysadmin_reserved_connections`为3，然后重启数据库。

```bash
gs_guc set -Z datanode -N all -I all -c "sysadmin_reserved_connections=3"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无

### OPENGAUSS.O_6.G_1.R_6：确保用户的最大连接数配置正确

**配置组ID：**
OPENGAUSS.G_1

**配置组名称：**
连接配置

**规则ID：**
OPENGAUSS.O_6.G_1.R_6

**规则名称：**
确保用户的最大连接数配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

在openGauss数据库中，不应该允许用户无限制数量的连接。如果用户参数`rolconnlimit`设置为-1，表示允许无限制数量的并发连接。根据业务需求限制不同用户的最大连接数，可避免连接被某个用户全部占用。

**影响：**
当前用户实际连接数超过用户的最大连接数限制后无法创建新连接。

**检查方法：**

执行以下SQL语句检查是否存在不限制连接数的用户，其中以`gs_role`开头的为内置角色不允许连接、无需检查。

```sql
SELECT rolname, rolconnlimit FROM pg_roles WHERE rolname NOT LIKE 'gs_role%' AND rolconnlimit = -1;
```

**修复方法：**

```sql
ALTER ROLE <role_name> CONNECTION LIMIT <connection_num>;
```

其中`<role_name>`表示用户名，`<connection_num>`表示配置的最大连接数。

**参考来源：**
无

### OPENGAUSS.O_6.G_1.R_7：确保UNIX域套接字的访问权限配置正确

**配置组ID：**
OPENGAUSS.G_1

**配置组名称：**
连接配置

**规则ID：**
OPENGAUSS.O_6.G_1.R_7

**规则名称：**
确保UNIX域套接字的访问权限配置正确

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`unix_socket_permissions`用于设置UNIX域套接字的访问权限。推荐配置是`0700`（只有当前连接数据库的用户自己可以访问，同组或者其他人都没有权限），满足文件权限最小化要求，避免文件被其他用户访问或篡改而影响套接字通信功能。

**影响：**
无

**检查方法：**

检查`unix_socket_permissions`参数配置值是否为`0700`，如果不是则失败。

```sql
openGauss=# show unix_socket_permissions;
 unix_socket_permissions
-------------------------
0700
(1 row)
```

**修复方法：**

修改`unix_socket_permissions`参数值为`0700`，然后重启数据库。

```bash
gs_guc set -Z datanode -N all -I all -c "unix_socket_permissions=0700"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无

### OPENGAUSS.O_6.G_1.R_8：确保除服务端节点外无host条目使用trust认证

**配置组ID：**
OPENGAUSS.G_1

**配置组名称：**
连接配置

**规则ID：**
COPENGAUSS.O_6.G_1.R_8

**规则名称：**
确保除服务端节点外无host条目使用trust认证

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

服务端节点部署在安全内网环境中，仅允许初始用户在服务端使用trust认证方式通讯。应配置`pg_hba.conf`除服务端节点外没有host条目使用trust认证方法。trust认证即无需认证即可允许连接。目前仅允许与运行数据库的OS用户同名的初始用户在服务端本地连接使用trust认证，其他远程连接或非初始用户连接等场景都需要经过服务端认证。用户在`pg_hba.conf`配置文件中增加客户端host条目时应避免使用trust认证方法，否则会导致与服务端连接失败。

**影响：**
无

**检查方法：**

通过如下shell命令检查`pg_hba.conf`配置中是否存在trust认证条目，其中`${GAUSSDATA}`为DN的数据目录。此检查需要人工确认哪些是服务端节点IP和本地环回IP，其中127.0.0.1和::1为本地环回IP，需确保除服务端节点IP和本地环回IP外无host条目使用trust认证。

```bash
grep -P '^[^#]*host(ssl|nossl)?\s+.+[Tt][Rr][Uu][Ss][Tt]\s*$' ${GAUSSDATA}/pg_hba.conf
```

**修复方法：**

除了初始用户连接服务端节点外，文件`pg_hba.conf`中其他host项配置为非trust认证方法。

**参考来源：**
无

### OPENGAUSS.O_6.G_1.R_9：确保没有host条目使用md5认证

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_9

**规则名称:**
确保没有host条目使用md5认证

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

md5认证方式存在安全风险，可能导致密码被破解，应采用更安全的sha256认证或证书认证方式。保留md5认证方式是为了兼容开源社区工具，但在生产环境中禁止使用md5认证。

**影响:**
无

**检查方法:**

通过如下shell命令检查`pg_hba.conf`配置中是否存在md5认证条目，其中`${GAUSSDATA}`为DN的数据目录。

```bash
grep -P '^[^#]*host(ssl|nossl)?\s+.+[Mm][Dd][5]\s*$' ${GAUSSDATA}/pg_hba.conf
```

**修复方法:**

为客户端host项配置认证方式为sha256。例如，配置用户`user1`通过IP为`192.168.0.1`的客户端连接数据库`db1`，认证方式为sha256，配置命令如下。

```bash
gs_guc reload -Z datanode -N all -I all -h "host db1 user1 192.168.0.1/32 sha256"
```

**参考来源:**
无

### OPENGAUSS.O_6.G_1.R_10：确保没有hostnossl条目

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_10

**规则名称:**
确保没有hostnossl条目

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

`hostnossl`条目指定不使用SSL加密连接，而`host`条目允许SSL和非SSL连接，`hostssl`则只能使用SSL连接。从安全角度考虑，推荐使用SSL加密连接对传输数据加密，避免信息泄露。

**影响:**
无

**检查方法:**

通过如下shell命令检查`pg_hba.conf`配置中是否存在`hostnossl`条目，其中`${GAUSSDATA}`为DN的数据目录。

```bash
grep -P '^[^#]*hostnossl' ${GAUSSDATA}/pg_hba.conf
```

**修复方法:**

将配置文件`pg_hba.conf`中所有`hostnossl`条目改为`host`或`hostssl`。

**参考来源:**
无

### OPENGAUSS.O_6.G_1.R_11：确保没有host条目的数据库指定为all

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_11

**规则名称:**
确保没有host条目的数据库指定为all

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

host连接条目若指定数据库为all，则允许用户连接到任何一个数据库。在满足业务需求的前提下，建议为不同的用户或客户端IP指定所需连接的数据库，避免不同业务之间相互影响。

**影响:**
无

**检查方法:**

通过如下shell命令检查`pg_hba.conf`配置中是否存在数据库指定为all的条目，其中`${GAUSSDATA}`为DN的数据目录。此检查需要人工确认哪些是服务端节点IP和本地环回IP（如127.0.0.1和::1），确保除服务端节点IP和本地环回IP外无host条目的数据库指定为all。

```bash
grep -P '^[^#]*host(ssl|nossl)?\s+[Aa][Ll][Ll]' ${GAUSSDATA}/pg_hba.conf
```

**修复方法:**

除服务端内部连接外，根据业务需要将配置文件`pg_hba.conf`中host、hostssl条目中的数据库为all的条目修改为需要连接的数据库。

**参考来源:**
无

### OPENGAUSS.O_6.G_1.R_12：确保没有host条目的用户指定为all

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_12

**规则名称:**
确保没有host条目的用户指定为all

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

host条目配置user为all表示允许所有用户连接到数据库。推荐host条目的user取值仅为需要连接数据库的用户。

**影响:**
如果用户需要连接数据库，但`pg_hba.conf`中没有添加对该用户的配置会导致连接失败。

**检查方法:**

通过如下shell命令检查`pg_hba.conf`配置中是否存在用户指定为all的条目，其中`${GAUSSDATA}`为DN的数据目录。此检查需要人工确认哪些是服务端节点IP和本地环回IP（如127.0.0.1和::1），需确保除服务端节点IP和本地环回IP外无host条目的用户指定为all。

```bash
grep -P '^[^#]*host(ssl|nossl)?\s+\S+\s+[Aa][Ll][Ll]' ${GAUSSDATA}/pg_hba.conf
```

**修复方法:**

除服务端内部连接外，根据业务需要将配置文件`pg_hba.conf`中host、hostssl对应用户为all的条目修改为需要连接数据库的用户。

**参考来源:**
无

### OPENGAUSS.O_6.G_1.R_13：确保没有host条目的源地址指定为0.0.0.0/0

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_13

**规则名称:**
确保没有host条目的源地址指定为0.0.0.0/0

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

host条目配置源地址为0.0.0.0/0意味着允许任意IP连接到数据库，这可能导致数据库被恶意用户进行网络攻击，影响数据库的安全性。推荐host条目配置的源地址仅为需要连接数据库的IP。

**影响:**
无

**检查方法:**

通过如下shell命令检查`pg_hba.conf`配置中是否存在源地址指定为0.0.0.0/0的条目，其中`${GAUSSDATA}`为DN的数据目录。

```bash
grep '0.0.0.0/0' ${GAUSSDATA}/pg_hba.conf
```

**修复方法:**

在配置文件`pg_hba.conf`中删除所有host、hostssl源地址为0.0.0.0/0的条目，或将地址改为需要连接数据库的客户端IP地址。

**参考来源:**
无

### OPENGAUSS.O_6.G_1.R_14：确保服务端使能SSL连接

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_14

**规则名称:**
确保服务端使能SSL连接

**级别:**
要求

**规则背景说明:**

SSL协议是为网络通信提供安全及数据完整性的一种安全协议。在使用数据库过程中应使用SSL协议进行TCP/IP连接以确保数据传输安全。参数`ssl`用于控制服务端是否使能SSL连接，参数为`on`表示使能SSL，此时服务端允许客户端通过SSL连接或非SSL连接，如果设置为`off`则只能通过非SSL连接。有关创建服务器私钥和证书的细节信息，可以参考openGauss的产品文档。

**影响：**

开启此参数需要同时确保`ssl_cert_file`、`ssl_key_file`和`ssl_ca_file`参数配置正确，并确保SSL证书权限为0600，不正确的配置可能会导致数据库无法正常启动。此外，开启SSL连接对性能会有一定影响。

**检查方法：**

检查参数ssl的配置是否为on，如果不为on则失败。

```sql
openGauss=# show ssl;
 ssl
-----
 on
(1 row)
```

**修复方法：**

配置参数`ssl`参数为`on`，然后重启数据库。

```bash
gs_guc set -Z datanode -N all -I all -c "ssl=on"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无

## 文件目录安全

### OPENGAUSS.O_6.G_2.R_1：确保数据库安装目录权限最小化

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_1

**规则名称：**
确保数据库安装目录权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`${GAUSSHOME}` 是 openGauss 的安装目录，为了防止安装目录下的文件被恶意篡改或破坏，此目录应该受到保护，不允许非数据库安装用户访问。正确的权限设置能确保数据库系统的安全性。

**影响：**
无

**检查方法：**

执行如下 shell 命令，如果返回 `${GAUSSHOME}` 目录下的任何文件或目录，则表示权限设置失败。

```bash
find -L ${GAUSSHOME} -prune \( ! -user ${GAUSSUSER} -o ! -group ${GAUSSGROUP} -o -perm /g=rwx,o=rwx \)
```

环境变量 `${GAUSSUSER}` 和 `${GAUSSGROUP}` 需要配置为数据库的安装用户和用户组。

**修复方法:**

```bash
chmod 0700 ${GAUSSHOME}
```

**参考来源:**
无

### OPENGAUSS.O_6.G_2.R_2：确保共享目录权限最小化

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_2

**规则名称：**
确保共享目录权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`${GAUSSHOME}/share` 目录包含了 openGauss 的共享组件，其中 `${GAUSSHOME}` 为数据库安装目录。为了防止共享组件被恶意篡改或破坏，此目录应该受到保护，不允许非数据库安装用户访问。

**影响：**
无

**检查方法：**

执行如下 shell 命令，如果返回 `${GAUSSHOME}/share` 目录则失败。

```bash
find ${GAUSSHOME}/share -prune -type d \( -perm -g=w -o -perm -o=w \) -exec ls -ld {} \;
```

**修复方法：**

```bash
chmod  0700 ${GAUSSHOME}/share
```

**参考来源：**
无

### OPENGAUSS.O_6.G_2.R_3：确保二进制文件目录权限最小化

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_3

**规则名称：**
确保二进制文件目录权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`${GAUSSHOME}/bin` 目录包含了数据库的二进制文件，其中 `${GAUSSHOME}` 为数据库安装目录。为了防止二进制文件被恶意篡改或破坏给客户信息安全造成威胁，此目录应该受到保护，不允许非数据库安装用户访问。

**影响：**
无

**检查方法：**

执行如下 shell 命令，如果返回 `${GAUSSHOME}/bin` 目录则失败。

```bash
find ${GAUSSHOME}/bin -prune -perm /g=rwx,o=rwx
```

**修复方法：**

```bash
chmod  0700 ${GAUSSHOME}/bin
```

**参考来源：**
无

### OPENGAUSS.O_6.G_2.R_4：确保数据目录权限最小化

**配置组ID:**
OPENGAUSS.G_2

**配置组名称:**
文件目录安全

**规则ID:**
OPENGAUSS.O_6.G_2.R_4

**规则名称:**
确保数据目录权限最小化

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

数据目录包含了用户数据文件，为了防止数据文件被恶意篡改或破坏给客户的数据信息安全造成威胁，此目录应该受到保护，不允许非数据库安装用户访问。

**影响:**
无

**检查方法:**

执行如下 shell 命令，如果返回数据目录则失败。

```bash
find ${GAUSSDATA} -prune \( ! -user ${GAUSSUSER} -o ! -group ${GAUSSGROUP} -o -perm /g=rwx,o=rwx \)
```

其中 `${GAUSSDATA}` 为 DN 的 data 目录，用户可通过 GUC 参数 `data_directory` 查询 DN 的 data 目录。环境变量 `${GAUSSUSER}` 和 `${GAUSSGROUP}` 需要配置为数据库的安装用户和用户组。

**修复方法:**

```bash
chmod 0700 ${GAUSSDATA}
```

其中 `${GAUSSDATA}` 为 DN 的 data 目录。

**参考来源：**
无

### OPENGAUSS.O_6.G_2.R_5：确保日志归档目录权限最小化

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_5

**规则名称：**
确保日志归档目录权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`${GAUSSHOME}/archive` 目录为日志归档目录，其中 `${GAUSSHOME}` 为数据库安装目录。当 `wal_level` 参数配置为 `archive` 时，该目录权限应该设置为 `0700` 以确保只允许数据库的安装运行用户访问。

**影响：**
无

**检查方法：**

执行如下 shell 命令，如果返回 `${GAUSSHOME}/archive` 目录则失败。如果 `${GAUSSHOME}/archive` 目录不存在则无需进行检查。

```bash
find ${GAUSSHOME}/archive -prune \( ! -user ${GAUSSUSER} -o ! -group ${GAUSSGROUP} -o -perm /g=rwx,o=rwx \)
```

环境变量 `${GAUSSUSER}` 和 `${GAUSSGROUP}` 需要配置为数据库的安装用户和用户组。

**修复方法：**

```bash
chmod 0700 ${GAUSSHOME}/archive
```

**参考来源：**
无

### OPENGAUSS.O_6.G_2.R_6：确保postgresql.conf文件权限最小化

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_6

**规则名称：**
确保postgresql.conf文件权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

配置文件`postgresql.conf`包含数据库运行的配置参数，为了防止配置文件被恶意篡改，此文件应该受到保护，不允许非数据库安装用户访问。

**影响：**
无

**检查方法：**

执行如下shell命令，如果返回`postgresql.conf`文件路径则失败。

```bash
find ${GAUSSDATA}/postgresql.conf \( ! -user ${GAUSSUSER} -o ! -group ${GAUSSGROUP} -o -perm /u=x,g=rwx,o=rwx \)
```

其中`${GAUSSDATA}`为DN的data目录，用户可通过GUC参数`data_directory`查询DN的data目录。环境变量`${GAUSSUSER}`和`${GAUSSGROUP}`需要配置为数据库的安装用户和用户组。

**修复方法：**

```bash
chmod 0600 ${GAUSSDATA}/postgresql.conf
```
其中`${GAUSSDATA}`为DN的data目录。

**参考来源：**
无

### OPENGAUSS.O_6.G_2.R_7：确保pg_hba.conf文件权限最小化

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_7

**规则名称：**
确保pg_hba.conf文件权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

配置文件`pg_hba.conf`包含了连接数据库的配置信息，如客户端认证方法等。为了防止配置文件被恶意篡改，此文件应该受到保护，仅允许数据库的安装用户访问。

**影响：**
无

**检查方法：**

执行如下shell命令，如果返回`pg_hba.conf`文件路径则失败。

```bash
find ${GAUSSDATA}/pg_hba.conf \( ! -user ${GAUSSUSER} -o ! -group ${GAUSSGROUP} -o -perm /u=x,g=rwx,o=rwx \)
```

其中`${GAUSSDATA}`为DN的data目录，用户可通过GUC参数`data_directory`查询DN的data目录。环境变量`${GAUSSUSER}`和`${GAUSSGROUP}`需要配置为数据库的安装用户和用户组。

**修复方法：**

```bash
chmod 0600 ${GAUSSDATA}/pg_hba.conf
```

其中`${GAUSSDATA}`为DN的data目录。

**参考来源：**
无

### OPENGAUSS.O_6.G_2.R_8：确保日志目录权限最小化

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_8

**规则名称：**
确保日志目录权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`${GAUSSLOG}`为数据库日志目录，目录下日志文件中包含很多运行信息，为了防止日志文件被恶意篡改或破坏给客户的数据信息安全造成威胁，此目录应该受到保护，不允许非数据库安装用户访问。

**影响：**
无

**检查方法：**

执行如下shell命令，如果返回`${GAUSSLOG}`目录则失败。

```bash
find ${GAUSSLOG} -prune \( ! -user ${GAUSSUSER} -o ! -group ${GAUSSGROUP} -o -perm /g=rwx,o=rwx \)
```

环境变量`${GAUSSUSER}`和`${GAUSSGROUP}`需要配置为数据库的安装用户和用户组。

**修复方法：**

```bash
chmod 0700 ${GAUSSLOG}
```

**参考来源：**
无

## 安全认证配置

### OPENGAUSS.O_6.G_3.R_1：确保客户端认证超时时间配置正确

**配置组ID:**
OPENGAUSS.G_3

**配置组名称:**
安全认证配置

**规则ID:**
OPENGAUSS.O_6.G_3.R_1

**规则名称:**
确保客户端认证超时时间配置正确

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

参数`authentication_timeout`控制完成客户端认证的时间上限，默认为一分钟。如果一个客户端没有在参数设定时间内完成与服务器端的认证，则服务器自动中断与客户端的连接，这样就避免了出问题的客户端无限制地占用连接数。

**影响:**
参数值设置过小可能因超时导致认证失败。

**检查方法:**

检查`authentication_timeout`参数设置，建议设置为1min。

```sql
openGauss=# show authentication_timeout;
 authentication_timeout
------------------------
 1min
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "authentication_timeout=1min"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_3.R_2：确保认证加密迭代次数配置正确

**配置组ID:**
OPENGAUSS.G_3

**配置组名称:**
安全认证配置

**规则ID:**
OPENGAUSS.O_6.G_3.R_2

**规则名称:**
确保认证加密迭代次数配置正确

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

通过`auth_iteration_count`参数配置对认证凭据进行单向哈希时的迭代次数。迭代次数设置过小会降低口令存储的安全性，设置过大会导致创建用户和认证等涉及口令加密的场景性能劣化。请根据实际硬件条件合理设置迭代次数，迭代次数最低应设置为10000次。

**影响:**

参数值设置过大会导致创建用户和认证等涉及口令加密的场景性能劣化，推荐采用默认迭代次数。

**检查方法:**

检查`auth_iteration_count`参数配置，如果小于10000则失败。

```sql
openGauss=# show auth_iteration_count;
 auth_iteration_count
----------------------
 10000
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "auth_iteration_count=10000"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_3.R_3：确保账户登录失败尝试次数配置正确

**配置组ID：**
OPENGAUSS.G_3

**配置组名称：**
安全认证配置

**规则ID：**
OPENGAUSS.O_6.G_3.R_3

**规则名称：**
确保账户登录失败尝试次数配置正确

**级别：**
要求

**规则背景说明：**

通过参数`failed_login_attempts`配置帐户登录失败尝试次数可以防止口令被暴力破解。参数`failed_login_attempts`默认值为10，表示连续认证失败次数超过10次后，帐户将被自动锁定。

**影响：**

配置参数`failed_login_attempts`为非0时，当连续认证失败次数超过此参数值后，帐户将被自动锁定。

**检查方法：**

检查`failed_login_attempts`参数值配置，如果参数为0则配置失败。

```sql
openGauss=# show failed_login_attempts;
 failed_login_attempts
-----------------------
 10
(1 row)
```

**修复方法：**

配置`failed_login_attempts`为大于0小于或等于1000的整数值，建议保持默认值10。

```bash
gs_guc reload -Z datanode -N all -I all -c "failed_login_attempts=10"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_3.R_4：确保开启服务端内部Kerberos认证

**配置组ID：**
OPENGAUSS.G_3
**配置组名称：**
安全认证配置

**规则ID：**
OPENGAUSS.O_6.G_3.R_4

**规则名称：**
确保开启服务端内部Kerberos认证

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

使用`gs_om`工具开启和关闭服务端内部Kerberos认证。如果数据库部署在非安全网络中，通过开启服务端内部Kerberos认证可解决数据库服务端内部节点被仿冒风险。

**影响：**
无

**检查方法：**

可以通过查看DN数据目录下`pg_hba.conf`配置文件，确认服务端内部节点认证方式是否为`gss`，如果为`gss`表示已开启Kerberos认证。执行`cm_ctl query -Cv`查看数据库状态，可以看到Kerberos进程状态。

**修复方法：**

确保数据库处于正常运行状态。首先，执行如下命令停止数据库：

```bash
gs_om -t stop
```

安装server，执行如下命令，其中USER为数据库初始用户，安装服务端，IP1表示主server所在的IP节点，IP2表示备server所在的IP节点。服务端主备IP指定服务端内任意IP即可：

```bash
gs_om -t kerberos -m install -U USER --krb-server IP1 --krb-standby IP2
```

安装client，在服务端内任一节点执行一次命令即可:

```bash
gs_om -t kerberos -m install -U USER --krb-client
```


使环境变量配置生效：

```bash
source ~/.bashrc
```

启动数据库：

```bash
gs_om -t start
```

**参考来源：**
无

## 账号口令管理

### OPENGAUSS.O_6.G_4.R_1：确保开启密码复杂度校验

**配置组ID：**
OPENGAUSS.G_4

**配置组名称：**
账号口令管理

**规则ID：**
OPENGAUSS.O_6.G_4.R_1

**规则名称：**
确保开启密码复杂度校验

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

为了保证数据库的使用安全，确保开启密码复杂度校验，在创建用户或者修改密码时校验密码复杂度。密码复杂度过低容易被猜解或暴力破解，为了密码安全性考虑，请开启密码复杂度校验。

**影响:**
无

**检查方法:**

检查`password_policy`参数值是否为1，如果不为1则失败。

```sql
openGauss=# show password_policy;
 password_policy
-----------------
 1
(1 row)
```

**修复方法:**

```bash
gs_guc reload -Z datanode -N all -I all -c "password_policy=1"
```

**参考来源:**
无

### OPENGAUSS.O_6.G_4.R_2：确保密码加密方式配置正确

**配置组ID:**
OPENGAUSS.G_4

**配置组名称:**
账号口令管理

**规则ID:**
OPENGAUSS.O_6.G_4.R_2

**规则名称:**
确保密码加密方式配置正确

**级别:**
要求

**相关要求：**
无

**规则背景说明:**

参数`password_encryption_type`用于配置数据库采用何种加密方式对用户密码进行加密存储。参数支持3种配置方式：

- 0：采用md5方式对密码加密
- 1：采用sha256和md5两种方式分别对密码加密
- 2：采用sha256方式对密码加密

md5方式已经证明不安全，不应该配置，保留仅为兼容开源第三方工具。应该配置为sha256方式（默认配置）。

**影响:**
无

**检查方法:**

检查`password_encryption_type`参数配置，如果为0或1则失败。

```sql
openGauss=# show password_encryption_type;
 password_encryption_type
--------------------------
 2
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "password_encryption_type=2"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_4.R_3：确保密码不可重用天数配置正确

**配置组ID：**
OPENGAUSS.G_4

**配置组名称：**
账号口令管理

**规则ID：**
OPENGAUSS.O_6.G_4.R_3

**规则名称：**
确保密码不可重用天数配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

在使用`ALTER USER`或者`ALTER ROLE`修改用户密码时，参数`password_reuse_time`指定是否对新密码进行可重用天数检查。配置此参数后，密码只有超过此设置的时间后才允许被重用。在数据库使用过程中，推荐配置用户密码不可重用天数，以避免用户反复使用相同的密码导致密码被破解。

**影响：**
无

**检查方法：**

检查`password_reuse_time`参数配置，如果值为0则失败。

```sql
openGauss=# show password_reuse_time;
 password_reuse_time
---------------------
 60
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "password_reuse_time=60"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_4.R_4：确保账户自动解锁时间配置正确

**配置组ID：**
OPENGAUSS.G_4

**配置组名称：**
账号口令管理

**规则ID：**
OPENGAUSS.O_6.G_4.R_4

**规则名称：**
确保账户自动解锁时间配置正确

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`password_lock_time`用于指定帐户被锁定后自动解锁的时间。参数单位为天，支持浮点数据类型，整数部分表示天数，小数部分可以换算成时、分、秒。参数值为0表示密码验证失败时，自动锁定功能不生效。为防止口令被尝试暴力破解，要求此参数设置为非0值。

**影响：**
无

**检查方法：**

检视`password_lock_time`参数配置，如果值为0则失败。

```sql
openGauss=# show password_lock_time;
 password_lock_time
--------------------
 1d
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "password_lock_time=1"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_4.R_5：账号口令管理：确保首次登陆时修改初始用户的密码

**配置组ID:**
OPENGAUSS.G_4

**配置组名称:**
账号口令管理

**规则ID:**
OPENGAUSS.O_6.G_4.R_5

**规则名称:**
确保首次登陆时修改初始用户的密码

**级别:**
要求

**相关要求：**
无

**规则背景说明:**

初始用户是权限最高、id为10的系统管理员。如果在安装数据库时未指定初始用户的密码，则默认密码为空。安装完成后首次登陆时需要修改初始用户的密码。如果初始用户密码为空并且没有被及时修改，容易引起低成本的攻击事件，也容易引起外界质疑，带来安全风险。

**影响:**
初始用户的密码需要妥善保管，如果忘记数据库初始用户密码则无法找回。

**检查方法:**

执行如下SQL语句，如果显示`rolpassword`字段为空则表明检查失败。

```sql
SELECT rolpassword FROM pg_authid WHERE rolsuper=true;
```

**修复方法:**

执行如下SQL语句修改初始用户的密码。

```sql
ALTER ROLE 'rolename' PASSWORD 'xxxxxxxx';
```

**参考来源:**
无

### OPENGAUSS.O_6.G_4.R_6：账号口令管理：确保配置用户的有效期限

**配置组ID:**
OPENGAUSS.G_4

**配置组名称:**
账号口令管理

**规则ID:**
OPENGAUSS.O_6.G_4.R_6

**规则名称:**
确保配置用户的有效期限

**级别:**
建议

**相关要求：**
无

**规则背景说明:**

创建用户或角色时，使用`VALID BEGIN`关键字设置用户的有效开始时间，`VALID UNTIL`关键字设置用户的有效结束时间。如果忽略这两个关键字，则用户或角色将长期有效。数据库服务端各节点的用户过期时间以各节点操作系统的时钟为依据。为确保服务端各节点的时间一致性，建议在安装部署数据库时使用NTP（网络时间协议）。若忽略这一配置，可能存在各节点登录帐户过期时间不一致的风险。因此，建议根据业务需要合理地配置用户或角色的有效期，并及时清理无用的过期用户或角色。

**影响：**

配置用户有效期后，当用户不在有效期限范围内时，将无法与数据库建立连接。

**检查方法：**

通过如下SQL语句检查是否存在未配置有效期的用户，其中，`WHERE`条件中`rolsuper=true`时表示初始用户，无需配置有效期限；以`gs_role`开头的为数据库内置角色，也无需配置有效期限。

```sql
SELECT rolname, rolvalidbegin, rolvaliduntil 
FROM pg_roles 
WHERE rolsuper=false 
AND rolname NOT LIKE 'gs_role%' 
AND (rolvalidbegin IS NULL OR rolvaliduntil IS NULL);
```

**修复方法:**

```sql
ALTER ROLE <role_name> VALID BEGIN 'yyyy-mm-dd' VALID UNTIL 'yyyy-mm-dd';
```

**参考来源:**
无

### OPENGAUSS.O_6.G_4.R_7：账号口令管理：确保配置密码的有效期限

**配置组ID:**
OPENGAUSS.G_4

**配置组名称:**
账号口令管理

**规则ID:**
OPENGAUSS.O_6.G_4.R_7

**规则名称:**
确保配置密码的有效期限

**级别:**
建议

**相关要求：**
无

**规则背景说明:**

通过`password_effect_time`参数可以配置用户登录密码的有效期，而`password_notify_time`参数则用于配置密码到期前多少天进行提醒。一旦密码达到过期提醒的时间，系统会在用户登录数据库时提示用户修改密码。建议用户定期更新密码，提升密码使用的安全性。

**影响：**

考虑到数据库使用的特殊性及业务连续性，密码过期后用户仍然可以登录数据库，但每次登录时系统都会提示用户修改密码，直至密码被修改为止。

**检查方法：**

检查`password_effect_time`参数配置，如果值为0则失败。

```sql
openGauss=# show password_effect_time;
 password_effect_time
----------------------
 90
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "password_effect_time=90"
```

**参考来源：**
无

## 权限管理

### OPENGAUSS.O_6.G_5.R_1：禁止PUBLIC角色拥有pg_authid系统表的权限

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_1

**规则名称：**
禁止PUBLIC角色拥有pg_authid系统表的权限

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`pg_catalog`模式下的`pg_authid`系统表中包含了数据库中所有的角色信息。由于所有用户会继承`PUBLIC`角色的权限，为了防止敏感信息泄露或被更改，`PUBLIC`角色不允许拥有`pg_authid`系统表的任何权限。

**影响：**
无

**检查方法：**

执行如下SQL语句，如果查询结果显示不为空则失败。

```sql
SELECT relname,relacl FROM pg_class WHERE relname = 'pg_authid' AND CAST(relacl AS TEXT) LIKE '%,=%}';
```

**修复方法：**

```sql
REVOKE ALL ON pg_authid FROM PUBLIC;
```

**参考来源：**
无

### OPENGAUSS.O_6.G_5.R_2：禁止PUBLIC角色在public模式下拥有CREATE权限

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_2

**规则名称：**
禁止PUBLIC角色在public模式下拥有CREATE权限

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

如果PUBLIC角色在public模式下拥有CREATE权限，则任何用户都可以在public模式下创建表或者其他数据库对象，这可能导致安全风险，因为其他用户也可以查看和修改这些表和数据库对象。此外，为了解决CVE-2018-1058漏洞问题，应禁止PUBLIC角色在public模式下拥有CREATE权限。

**影响：**
配置后PUBLIC角色在public模式下无CREATE权限。

**检查方法：**

通过如下语句检查PUBLIC角色在public模式下是否拥有CREATE权限，如果返回`true`则表示配置失败。

```sql
SELECT CAST(has_schema_privilege('public','public','CREATE') AS TEXT);
has_schema_privilege
----------------------
false
(1 row)
```

**修复方法：**

```sql
REVOKE CREATE ON SCHEMA public FROM PUBLIC;
```

**参考来源：**
[A Guide to CVE-2018-1058: Protect Your Search Path](https://wiki.postgresql.org/wiki/A_Guide_to_CVE-2018-1058%3A_Protect_Your_Search_Path)

### OPENGAUSS.O_6.G_5.R_3：禁止将对象的所有权限授予PUBLIC角色

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_3

**规则名称：**
禁止将对象的所有权限授予PUBLIC角色

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

PUBLIC角色属于任何用户，如果将对象的所有权限授予PUBLIC角色，则任意用户都会继承此对象的所有权限，违背权限最小化原则。为了保障数据库数据的安全，此角色应该拥有尽可能少的权限，应禁止将对象的所有权限授予PUBLIC角色。

**影响：**
无

**检查方法：**

通过如下语句检查表或视图的所有权限是否授予PUBLIC角色，如果结果不为空则失败。

```sql
SELECT relname,relacl FROM pg_class 
WHERE (CAST(relacl AS TEXT) LIKE '%,=arwdDxt/%}' OR CAST(relacl AS TEXT) LIKE '{=arwdDxt/%}') 
AND (CAST(relacl AS TEXT) LIKE '%,=APmiv/%}' OR CAST(relacl AS TEXT) LIKE '{=APmiv/%}');
```

通过如下语句检查模式的所有权限是否授予PUBLIC角色，如果结果不为空则失败。

```sql
SELECT nspname,nspacl FROM pg_namespace 
WHERE (CAST(nspacl AS TEXT) LIKE '%,=UC/%}' OR CAST(nspacl AS TEXT) LIKE '{=UC/%}') 
AND (CAST(nspacl AS TEXT) LIKE '%,=APm/%}' OR CAST(nspacl AS TEXT) LIKE '{=APm/%}');
```

通过如下语句检查函数的所有权限是否授予PUBLIC角色，如果结果不为空则失败。

```sql
SELECT proname,proacl FROM pg_proc 
WHERE (CAST(proacl AS TEXT) LIKE '%,=X/%}' OR CAST(proacl AS TEXT) LIKE '{=X/%}') 
AND (CAST(proacl AS TEXT) LIKE '%,=APm/%}' OR CAST(proacl AS TEXT) LIKE '{=APm/%}');
```

其他数据库对象的权限检查可以参考上述命令进行排查。ACL权限参数说明如下表所示。

| 参数 | 参数说明 |
| --- | --- |
| r | SELECT |
| w | UPDATE |
| a | INSERT |
| d | DELETE |
| D | TRUNCATE |
| x | REFERENCES |
| t | TRIGGER |
| X | EXECUTE |
| U | USAGE |
| C | CREATE |
| c | CONNECT |
| T | TEMPORARY |
| A | ALTER |
| P | DROP |
| m | COMMENT |
| i | INDEX |
| v | VACUUM |
| * | 给前面权限的授权选项 |

**修复方法：**

撤销PUBLIC角色拥有的表或视图的所有权限

```sql
REVOKE ALL ON <OBJECT_NAME> FROM PUBLIC;
```

撤销PUBLIC角色拥有的模式的所有权限

```sql
REVOKE ALL ON SCHEMA <OBJECT_NAME> FROM PUBLIC;
```

撤销PUBLIC角色拥有的函数的所有权限（注意函数对象名称需要包含参数）

```sql
REVOKE ALL ON FUNCTION function_name([arg_type][, ...]) FROM PUBLIC;
```

**参考来源：**
无

### OPENGAUSS.O_6.G_5.R_4：禁止将初始用户用于执行普通业务操作

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_4

**规则名称：**
禁止将初始用户用于执行普通业务操作

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

数据库初始用户具有数据库的最高权限，并且具有所有的系统权限和对象权限。应仅将初始用户作为DBA管理用途，禁止用于执行普通业务操作。使用初始用户执行普通业务操作，违背权限最小化原则，同时可能带来安全风险。

**影响：**
无

**检查方法：**

通过如下语句查询初始用户当前的作业，排查是否存在非系统自动触发的普通业务操作。

```sql
SELECT s.* 
FROM pg_stat_activity as s, pg_roles as t 
WHERE s.usename = t.rolname and t.rolsuper = true;
```

**修复方法：**

检查初始用户是否用于执行普通业务操作。业务用户权限最小化，禁止使用初始用户执行普通业务操作。

**参考来源：**
无

### OPENGAUSS.O_6.G_5.R_5：确保使用非系统管理员执行普通业务操作

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_5

**规则名称：**
确保使用非系统管理员执行普通业务操作

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

数据库系统管理员拥有较高的数据库权限，使用系统管理员执行普通业务操作，违背权限最小化原则，同时可能带来安全风险。不要使用系统管理员执行普通业务操作。

**影响：**
无

**检查方法：**

通过如下语句查询系统管理员当前的作业，排查是否存在非系统自动触发的普通业务操作。

```sql
SELECT s.* 
FROM pg_stat_activity as s, pg_roles as t 
WHERE s.usename = t.rolname 
AND t.rolsystemadmin = true;
```

**修复方法：**

业务用户权限最小化，创建非管理员用户并用于执行普通业务操作。

**参考来源：**
无

### OPENGAUSS.O_6.G_5.R_6：确保撤销普通用户非必须的管理权限

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_6

**规则名称：**
确保撤销普通用户非必须的管理权限

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

普通用户指用于执行普通业务操作的非管理员用户。作为普通用户，不应该拥有超出其正常权限范围的管理权限，例如创建角色权限（CREATEROLE）、创建数据库权限（CREATEDB）、审计权限（AUDITADMIN）、监控权限（MONADMIN）、运维权限（OPRADMIN）、安全策略权限（POLADMIN）等。在满足正常业务需求的前提下，为了确保普通用户权限最小化，应撤销普通用户非必须的管理权限。

**影响：**
无

**检查方法：**

以下列举的是常用的管理权限，其他管理权限的检查方法类似，请根据需要进行排查。

检查拥有CREATEROLE权限的普通用户

```sql
SELECT rolname FROM pg_roles WHERE rolcreaterole = true AND rolsuper = false;
```

检查拥有CREATEDB权限的普通用户

```sql
SELECT rolname FROM pg_roles WHERE rolcreatedb = true AND rolsuper = false;
```

检查拥有AUDITADMIN权限的普通用户

```sql
SELECT rolname FROM pg_roles WHERE rolauditadmin = true AND rolsuper = false;
```

检查拥有MONADMIN权限的普通用户

```sql
SELECT rolname FROM pg_roles WHERE rolmonitoradmin = true AND rolsuper = false;
```

检查拥有OPRADMIN权限的普通用户

```sql
SELECT rolname FROM pg_roles WHERE roloperatoradmin = true AND rolsuper = false;
```

检查拥有POLADMIN权限的普通用户

```sql
SELECT rolname FROM pg_roles WHERE rolpolicyadmin = true AND rolsuper = false;
```

**修复方法：**

撤销CREATEROLE权限

```sql
ALTER ROLE <role_name> NOCREATEROLE;
```

撤销CREATEDB权限

```sql
ALTER ROLE <role_name> NOCREATEDB;
```

撤销AUDITADMIN权限

```sql
ALTER ROLE <role_name> NOAUDITADMIN;
```

撤销MONADMIN权限

```sql
ALTER ROLE <role_name> NOMONADMIN;
```

撤销OPRADMIN权限

```sql
ALTER ROLE <role_name> NOOPRADMIN;
```

撤销POLADMIN权限

```sql
ALTER ROLE <role_name> NOPOLADMIN;
```

**参考来源：**
无

### OPENGAUSS.O_6.G_5.R_7：禁止PUBLIC角色执行SECURITY DEFINER类型的函数

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_7

**规则名称：**
禁止PUBLIC角色执行SECURITY DEFINER类型的函数

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

在创建函数时声明`SECURITY DEFINER`表示函数以创建它的用户权限执行，如果使用不当会导致函数执行者借助创建者的权限执行越权操作，所以一定确保这样的函数不被滥用。为了安全考虑，禁止`PUBLIC`角色执行`SECURITY DEFINER`类型的函数。另外需要说明的是，`SECURITY DEFINER`和`AUTHID DEFINER`的功能相同。

**影响：**
禁止`PUBLIC`角色执行`SECURITY DEFINER`类型的函数后，如果其他用户需要执行此函数需要单独授予相应权限，否则会因权限不足导致执行失败。

**检查方法：**

执行如下SQL语句，查询非在`pg_catalog`模式下定位为`SECURITY DEFINER`类型的函数。

```sql
SELECT a.proname, b.nspname 
FROM pg_proc a, pg_namespace b 
WHERE a.pronamespace=b.oid 
AND b.nspname <> 'pg_catalog' 
AND a.prosecdef='t';
```

如果上述语句返回非空，则执行下面的SQL语句检查`PUBLIC`角色是否拥有此函数的执行权限，其中函数需要明确参数类型，必要时还需要在函数名前添加所在模式名前缀。如果返回`true`表示`PUBLIC`角色拥有此函数的执行权限，则检查结果失败。

```sql
SELECT CAST(has_function_privilege('public', 'function_name([arg_type][, ...])', 'EXECUTE') AS TEXT);
```

**修复方法：**

执行如下SQL语句撤销`PUBLIC`角色执行函数的权限，其中函数需要明确参数类型，必要时还需要在函数名前添加所在模式名前缀。

```sql
REVOKE EXECUTE ON FUNCTION function_name([arg_type][, ...]) FROM PUBLIC;
```

**参考来源：**
无

### OPENGAUSS.O_6.G_5.R_8：确保SECURITY INVOKER类型的函数定义符合预期

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_8

**规则名称：**
确保SECURITY INVOKER类型的函数定义符合预期

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`SECURITY INVOKER`函数是以调用它的用户的权限来执行，使用不当会导致函数创建者借助执行者的权限执行越权操作，所以在调用非自身创建的这类函数时，一定要先检查函数执行内容，避免造成函数创建者借助执行者的权限执行了越权的操作。

**影响：**
无

**检查方法：**

1、检查普通用户或管理员执行非自身创建的`SECURITY INVOKER`函数，其中`function_name`为被检查函数名称。

```sql
SELECT prosrc FROM pg_proc WHERE proname = 'function_name' AND prosecdef = false;
```

2、检查普通用户或管理员对非自身创建的含有触发器的表执行INSERT/UPDATE/DELETE/TRUNCATE操作，其中table_name为被检查表名。

```sql
SELECT a.prosrc 
FROM pg_proc a 
INNER JOIN PG_TRIGGER c ON a.oid = c.tgfoid 
INNER JOIN PG_CLASS b ON b.oid = c.tgrelid AND b.relname = 'table_name' 
WHERE a.prosecdef = false;
```

**修复方法:**

执行函数前，检查函数执行内容，避免造成函数创建者借助执行者的权限执行了越权的操作。

**参考来源:**
无

### OPENGAUSS.O_6.G_5.R_9：确保开启三权分立配置

**配置组ID:**
OPENGAUSS.G_5

**配置组名称:**
权限管理

**规则ID:**
OPENGAUSS.O_6.G_5.R_9

**规则名称:**
确保开启三权分立配置

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

设置参数`enableSeparationOfDuty`为`on`会开启三权分立配置，限制系统管理员的权限，系统管理员不再拥有创建用户或更改用户配置权限，并且不再拥有查看和维护数据库审计日志的权限。当开启三权分立时，建议用户关闭GUC参数`enable_copy_server_files`来控制系统管理员的copy权限，防止系统管理员通过copy命令读取或者修改用户配置文件。三权分立特性的详细说明请 参见相关产品文档。

**影响：**

如需使用三权分立权限管理模型，应在数据库初始化阶段指定，不建议来回切换权限管理模型。特别的，如需从非三权分立切换至三权分立权限管理模型，应重新审视已有用户的权限集合是否合理。

**检查方法：**

检查`enableSeparationOfDuty`参数值是否为`on`，如果不为on则失败。

```sql
openGauss=# show enableSeparationOfDuty;
 enableSeparationOfDuty
------------------------
on
(1 row)
```

**修复方法：**

修改参数`enableSeparationOfDuty`为`on`，然后重启数据库。修改命令如下：

```bash
gs_guc set -Z datanode -N all -I all -c "enableSeparationOfDuty = on"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无

### OPENGAUSS.O_6.G_5.R_10：确保取消系统管理员服务端文件COPY权限

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_10

**规则名称：**
确保取消系统管理员服务端文件COPY权限

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`enable_copy_server_files`允许系统管理员用户执行服务端文件的COPY操作，但远程COPY操作存在越权查看或修改敏感文件的风险。在生产环境下的数据库中，通常不建议打开该配置。该参数的默认值为`off`，表示只允许初始用户执行`COPY FROM FILENAME`或`COPY TO FILENAME`语句。

**影响：**
取消系统管理员的服务端文件COPY权限后，系统管理员将无法进行服务端文件的COPY操作。这一配置对初始用户无影响。

**检查方法：**

检查`enable_copy_server_files`参数值是否为`off`，如果不为off则失败。

```sql
openGauss=# show enable_copy_server_files;
 enable_copy_server_files
--------------------------
off
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "enable_copy_server_files=off"
```

**参考来源：**
无

## 数据库审计

### OPENGAUSS.O_6.G_6.R_1：确保开启数据库审计功能

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_1

**规则名称：**
确保开启数据库审计功能

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

审计日志记录是安全事件中事后追溯、定位问题原因及划分事故责任的重要手段。推荐开启数据库审计功能，将参数`audit_enabled`设置为`on`。

**影响：**

审计日志以二进制形式存储于`pg_audit`目录，开启审计功能后会增加磁盘空间占用，并对性能有一定影响。

**检查方法：**

检查`audit_enabled`参数值是否为`on`，不为`on`则失败。

```sql
openGauss=# show audit_enabled;
 audit_enabled
---------------
on
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_enabled = on"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_6.R_2：确保开启用户登录和注销审计

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_2

**规则名称：**
确保开启用户登录和注销审计

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`audit_login_logout`决定是否对用户登录（包括登录成功和登录失败）和注销操作记录审计日志。如果开启此选项可以追溯有哪些用户曾经登录数据库，何时注销登录，否则无法对用户登录和注销情况进行审计。

**影响：**
无

**检查方法：**

检查`audit_login_logout`参数值是否为7，不为7则失败。

```sql
openGauss=# show audit_login_logout;
 audit_login_logout
--------------------
 7
(1 row)
```

**修复方法：**

修改参数值为7，表示用户登录成功、失败和注销均记录审计日志。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_login_logout = 7"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_6.R_3：确保开启数据库启动、停止、恢复和切换审计

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_3

**规则名称：**
确保开启数据库启动、停止、恢复和切换审计

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`audit_database_process`决定是否对数据库的启动、停止、切换和恢复操作记录审计日志。开启此选项可以追溯数据库的运行状态变化。

**影响：**
无

**检查方法：**

检查`audit_database_process`参数值是否为1，如果不为1则失败。

```sql
openGauss=# show audit_database_process;
 audit_database_process
------------------------
 1
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_database_process = 1"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_6.R_4：确保开启用户锁定和解锁审计

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_4

**规则名称：**
确保开启用户锁定和解锁审计

**级别：**
要求

**相关要求：**
无

**规则背景说明:**

参数`audit_user_locked`决定是否对数据库用户的锁定和解锁操作记录审计日志。

**影响:**
无

**检查方法:**

检查`audit_user_locked`参数值是否为1，如果不为1则失败。

```sql
openGauss=# show audit_user_locked;
 audit_user_locked
-------------------
 1
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_user_locked = 1"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_6.R_5：确保开启权限授予和回收审计

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_5

**规则名称：**
确保开启权限授予和回收审计

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`audit_grant_revoke`决定是否对数据库用户权限授予和回收的操作记录审计日志。

**影响：**
无

**检查方法：**

检查`audit_grant_revoke`参数值是否为1，如果不为1则失败。

```sql
openGauss=# show audit_grant_revoke;
audit_grant_revoke
--------------------
1
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_grant_revoke = 1"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_6.R_6：确保开启数据库对象的添加、删除、修改审计

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_6

**规则名称：**
确保开启数据库对象的添加、删除、修改审计

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`audit_system_object`决定是否对数据库对象的CREATE、DROP、ALTER操作记录审计日志。这些数据库对象包括DATABASE、USER、SCHEMA、TABLE等。该参数的值由20个二进制位的组合求出，每个二进制位代表openGauss Kernel中的一类数据库对象。如果某个二进制位取值为0，则不审计对应数据库对象的CREATE、DROP、ALTER操作；如果取值为1，则审计这些操作。具体每个二进制位代表的审计对象请参考openGauss的官方文档中对`audit_system_object`参数的说明。

**影响：**
无

**检查方法：**

检查`audit_system_object`参数值配置，如果参数值小于默认值12295则失败。

```sql
openGauss=# show audit_system_object;
 audit_system_object
---------------------
 12295
(1 row)
```

**修复方法：**

参数`audit_system_object`参数值设置为12295，表示对DATABASE、SCHEMA、USER、DATA SOURCE、NODE GROUP等数据库对象的DDL操作的审计。用户可根据业务需要开启对更多数据库对象DDL操作的审计。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_system_object = 12295"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_6.R_7：确保开启数据库对象的查询审计

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_7

**规则名称：**
确保开启数据库对象的查询审计

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`audit_dml_state_select`决定是否对数据库对象的SELECT操作进行审计，默认值为0表示不开启。

**影响：**

开启此选项可以追溯用户对数据库的查询操作，但通常数据库查询操作使用相对频繁，开启此选项后会影响查询性能，并且会导致审计日志记录增加、占用更多磁盘空间。用户可根据业务需要决定是否开启。

**检查方法：**

检查`audit_dml_state_select`参数值是否为1，如果不为1则失败。

```sql
openGauss=# show audit_dml_state_select;
 audit_dml_state_select
------------------------
 0
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_dml_state_select = 1"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_6.R_8：确保审计优先策略配置正确

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_8

**规则名称：**
确保审计优先策略配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

控制审计日志的保存策略，以空间还是时间限制为优先策略。

**影响：**

空间策略可以保证审计日志磁盘占用的上限，但是不保证历史审计日志存留；时间限制策略保证特定时间段审计日志的保留，可能日志占用空间会变大。

**检查方法：**

检查`audit_resource_policy`参数值是否为`on`，如果不为`on`则失败。

```sql
openGauss=# show audit_resource_policy;
audit_resource_policy
-----------------------
on
(1 row)
```

**修复方法：**

修改参数`audit_resource_policy`为`on`(空间优先)。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_resource_policy = on"
```

**参考来源:**
无

### OPENGAUSS.O_6.G_6.R_9：确保单个审计文件的最长记录时间配置正确

**配置组ID:**
OPENGAUSS.G_6

**配置组名称:**
数据库审计

**规则ID:**
OPENGAUSS.O_6.G_6.R_9

**规则名称:**
确保单个审计文件的最长记录时间配置正确

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

参数`audit_rotation_interval`设置单个审计日志文件的最长记录时间。如果超过这个时间，将自动创建一个新的审计日志文件。

**影响:**

- 参数值设置过小会导致频繁产生审计日志文件。
- 设置过大会导致单个文件记录日志过多、文件占用空间较大，不利于审计日志文件管理。
- 请勿随意调整此参数，否则可能导致`audit_resource_policy`参数无法生效。

**检查方法:**

检查`audit_rotation_interval`参数值配置，建议配置最长记录时间为1天。

```sql
openGauss=# show audit_rotation_interval;
audit_rotation_interval
-------------------------
1d
(1 row)
```

**修复方法:**

参数`audit_rotation_interval`的单位为分钟（min），修改参数值为1440，即为1天(1d)。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_rotation_interval = 1440"
```

**参考来源:**
无

### OPENGAUSS.O_6.G_6.R_10：确保单个审计日志文件的最大容量配置正确

**配置组ID:**
OPENGAUSS.G_6

**配置组名称:**
数据库审计

**规则ID:**
OPENGAUSS.O_6.G_6.R_10

**规则名称:**
确保单个审计日志文件的最大容量配置正确

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

参数`audit_rotation_size`设置单个审计日志文件最大的容量。当审计日志文件达到最大容量时，将自动创建一个新的日志文件。

**影响:**

- 参数值设置过小会导致频繁产生审计日志文件。
- 设置过大会导致单个文件记录日志过多、文件占用空间较大，不利于审计日志文件管理。
- 请不要随意调整此参数，否则可能会导致`audit_resource_policy`参数无法生效。

**检查方法:**

检查`audit_rotation_size`参数值配置，建议配置为10MB。

```sql
openGauss=# show audit_rotation_size;
audit_rotation_size
---------------------
10MB
(1 row)
```

**修复方法:**

修改`audit_rotation_size`参数值10MB。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_rotation_size = 10MB"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_6.R_11：确保所有审计日志文件占用的最大磁盘空间配置正确

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_11

**规则名称：**
确保所有审计日志文件占用的最大磁盘空间配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`audit_space_limit`设置审计文件所占的最大磁盘空间。当审计文件总量超过最大值时，系统将在数据库日志文件中写入警告信息，并删除最早的审计文件，同时记录审计文件删除信息到审计日志中。

**影响：**

- 设置参数值过大会增加磁盘空间占用。
- 参数值过小则审计日志留存时间变短，可能导致重要日志信息丢失。

**检查方法：**

检查`audit_space_limit`参数值配置。

```sql
openGauss=# show audit_space_limit;
audit_space_limit
-------------------
1GB
(1 row)
```

**修复方法：**

根据实际需要配置参数`audit_space_limit`大小，建议配置不小于1GB。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_space_limit = 1GB"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_6.R_12：确保审计日志文件最大数目配置正确

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_12

**规则名称：**
确保审计日志文件最大数目配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`audit_file_remain_threshold`设置审计日志文件的最大保留数量。当审计文件总数超过指定值时，系统将向数据库日志文件中写入警告信息，并删除最早的审计文件，同时记录审计文件删除信息到审计日志中。

**影响：**

- 设置参数值过大会增加磁盘空间占用。
- 参数值过小则审计日志可记录周期变短，可能导致重要日志信息丢失。
- 随意调整此参数可能会影响`audit_resource_policy`参数的效果。

**检查方法：**

检查`audit_file_remain_threshold`参数值配置，通常建议配置为默认值1024。

```sql
openGauss=# show audit_file_remain_threshold;
 audit_file_remain_threshold
-----------------------------
 1024
(1 row)
```

**修复方法：**

修改`audit_file_remain_threshold`参数值为1048576。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_file_remain_threshold = 1048576"
```

**参考来源：**
无

## 错误报告和日志配置

### OPENGAUSS.O_6.G_7.R_1：确保开启日志收集器

**配置组ID：**
OPENGAUSS.G_7

**配置组名称:**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_1

**规则名称：**
确保开启日志收集器

**级别：**
要求

**规则背景说明：**

参数`logging_collector`控制开启后端日志收集进程`logger`进行日志收集。该进程捕获发送到`stderr`或`csvlog`的日志消息并写入日志文件。这种记录日志的方法比将日志记录到`syslog`更加有效，因为某些类型的消息在`syslog`的输出中无法显示。

**影响：**

将服务器日志发送到`stderr`时可以不使用`logging_collector`参数，此时日志消息会被发送到服务器的`stderr`指向的空间。这种方法的缺点是日志回滚困难，只适用于较小的日志容量。

**检查方法：**

检查`logging_collector`参数值是否为`on`，如果不为`on`则失败。

```sql
openGauss=# show logging_collector;
 logging_collector
-------------------
 on
(1 row)
```

**修复方法：**

在postgresql.conf配置文件中修改参数`logging_collector`为`on`，然后重启数据库。

```bash
gs_guc set -Z datanode -N all -I all -c "logging_collector=on"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_2：确保日志名称配置正确

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_2

**规则名称：**
确保日志名称配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_filename`设置服务器运行日志文件的名称。建议使用`%`转义字符定义日志文件名称，以便能够自动包含日期和时间信息，从而方便对日志文件进行有效的管理。

**影响：**
无

**检查方法：**

检查`log_filename`参数配置，建议保持默认配置，即使用包含日期和时间信息的格式。

```sql
openGauss=# show log_filename;
          log_filename
--------------------------------
 postgresql-%Y-%m-%d_%H%M%S.log
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "log_filename = 'postgresql-%Y-%m-%d_%H%M%S.log'"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_3：确保日志文件权限配置正确

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_3

**规则名称：**
确保日志文件权限配置正确

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

当开启参数`logging_collector`时，可以使用参数`log_file_mode`设置服务器日志文件的权限。因为日志文件中可能含有用户数据，所以日志文件访问必须受到限制，以防止日志信息泄露或被篡改。

**影响：**
无

**检查方法：**

检查`log_file_mode`参数值是否为`0600`，如果不是则失败。

```sql
openGauss=# show log_file_mode;
 log_file_mode
---------------
 0600
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "log_file_mode=0600"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_4：禁止覆盖写入同名日志文件

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_4

**规则名称：**
禁止覆盖写入同名日志文件

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`log_truncate_on_rotation`设置日志消息的写入方式。当设置为`on`时，数据库会以覆盖写入的方式写入服务器日志消息，这意味着当日志文件被轮转时，新的日志消息会覆盖旧的日志消息。当设置为`off`时，新的日志消息会被附加到同名的现有日志文件上，而不会覆盖旧的日志。为确保日志保留更长时间，需要将此参数设置为`off`，禁止覆盖写入同名日志文件。

**影响：**
无

**检查方法：**

检查`log_truncate_on_rotation`参数值是否为`off`，如果不为`off`则失败。

```sql
openGauss=# show log_truncate_on_rotation;
 log_truncate_on_rotation
--------------------------
 off
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "log_truncate_on_rotation=off"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_5：确保单个日志文件最大记录时间配置正确

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_5

**规则名称：**
确保单个日志文件最大记录时间配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_rotation_age`用于设置单个日志文件最大的日志记录时间。当日志记录时间超过该参数设置的最大值时，服务器将自动创建新的日志文件。正确的配置有助于避免日志文件过于频繁地产生，同时避免单个日志文件过大导致管理不便。

**影响：**

- 如果`log_rotation_age`参数值设置过小，将导致日志文件频繁产生，增加管理难度。
- 如果参数值设置过大，单个日志文件将记录过多的日志，可能导致文件占用空间过大，同样不利于日志文件管理。

**检查方法：**

检查`log_rotation_age`参数配置，建议配置为默认值`1d`（即一天）。

```sql
openGauss=# show log_rotation_age;
 log_rotation_age
------------------
 1d
(1 row)
```

**修复方法：**

参数`log_rotation_age`单位为min，默认值为1d，即1440min。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_rotation_age=1d"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_6：确保单个日志文件最大容量配置正确

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_6

**规则名称：**
确保单个日志文件最大容量配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_rotation_size`用于设置单个日志文件的最大容量。当日志文件达到该最大容量时，服务器将自动创建新的日志文件，以避免日志文件过大导致管理困难。

**影响：**

- 如果`log_rotation_size`参数值设置过小，会导致日志文件频繁产生，增加管理难度。
- 如果参数值设置过大，单个日志文件将记录过多的日志，可能导致文件占用空间过大，不利于日志文件管理。

**检查方法：**

检查`log_rotation_size`参数配置，建议配置为默认值`20MB`。

```sql
openGauss=# show log_rotation_size;
 log_rotation_size
-------------------
 20MB
(1 row)
```

**修复方法：**

参数`log_rotation_size`单位为KB，默认值为20MB。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_rotation_size=20MB"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_7：确保客户端日志等级配置正确

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_7

**规则名称：**
确保客户端日志等级配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`client_min_messages`控制按设置的等级将消息发送到客户端。有效的值包括`debug`、`debug5`、`debug4`、`debug3`、`debug2`、`debug1`、`info`、`log`、`notice`、`warning`、`error`、`fatal`、`panic`，其中`debug`和`debug2`等效。每个等级都包括排在他后面的所有级别中的日志。在实际设置过程中，如果设置的级别大于`error`，例如为`fatal`或`panic`，系统会默认将级别转为`error`。

**影响：**

- 日志级别`debug1`~`debug5`主要用于调试，生产环境不建议使用，否则发送给客户端的日志会增多。
- 建议保持默认值`notice`。

**检查方法：**

检查`client_min_messages`参数值，如果为`debug`或`debug1`~`debug5`则配置可能不正确。

```sql
openGauss=# show client_min_messages;
 client_min_messages
---------------------
 notice
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "client_min_messages=notice"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_8：确保服务器日志等级配置正确

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_8

**规则名称：**
确保服务器日志等级配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_min_messages`控制按的等级将消息写入到服务器日志。有效的值包括`debug`、`debug5`、`debug4`、`debug3`、`debug2`、`debug1`、`info`、`log`、`notice`、`warning`、`error`、`fatal`、`panic`。其中`debug`和`debug2`等效，每个级别都包含排在他后面的所有级别中的信息。

**影响：**

- 日志级别`debug1`~`debug5`主要用于调试，生产环境不建议使用，否则写入服务器的日志会增多。
- 建议保持默认值`warning`。

**检查方法：**

检查`log_min_messages`参数值，如果为`debug`或`debug1`~`debug5`则配置可能不正确。

```sql
openGauss=# show log_min_messages;
 log_min_messages
------------------
 warning
(1 row)
```

**修复方法：**

设置参数`log_min_messages`为`warning`。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_min_messages=warning"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_9：确保记录产生错误的SQL语句日志级别配置正确

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_9

**规则名称：**
确保记录产生错误的SQL语句日志级别配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_min_error_statement`控制是否在服务器日志中记录产生错误的SQL语句。有效值包括`debug`、`debug5`、`debug4`、`debug3`、`debug2`、`debug1`、`info`、`log`、`notice`、`warning`、`error`、`fatal`、`panic`。设置为`error`时，表示产生`error`、`fatal`、`panic`级别错误的语句都将被记录。设置为`panic`时，表示关闭此特性。由于有的SQL语句中包含用户个人信息，如果不需要记录出错的SQL语句，可以将参数设置为`panic`。

**影响：**
无

**检查方法：**

检查`log_min_error_statement`参数值是否为`error`，如果不为`error`则配置可能不正确。

```sql
openGauss=# show log_min_error_statement;
 log_min_error_statement
-------------------------
 error
(1 row)
```

**修复方法：**

设置参数`log_min_error_statement`为`error`。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_min_error_statement=error"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_10：确保开启用户登录时日志记录功能

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_10

**规则名称：**
确保开启用户登录时日志记录功能

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_connections`用于记录每次尝试连接到服务器的日志，以及成功完成客户端连接认证的日志。

**影响：**

- 开启`log_connections`可以记录所有用户登录尝试的日志，帮助管理员分析潜在的恶意连接或连接问题。
- 但同时，由于会记录所有的连接尝试，可能会导致日志文件增长迅速，增加磁盘存储压力。

**检查方法：**

通过执行以下SQL命令来检查`log_connections`参数值是否为`on`，如果不为`on`则失败。

```sql
openGauss=# show log_connections;
 log_connections
-----------------
 off
(1 row)
```

**修复方法：**

设置参数`log_connections`为`on`。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_connections=on"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_11：确保开启用户注销时日志记录功能

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_11

**规则名称：**
确保开启用户注销时日志记录功能

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_disconnections`用于设置是否记录客户端结束连接的信息，包括在会话结束时在服务器日志中输出一行，并包含会话的持续时间。

**影响：**

- 开启`log_disconnections`参数有助于分析客户端连接的断开情况，包括断开原因和会话持续时间。
- 同时，开启此参数可能会增加日志记录量，需要考虑到磁盘存储和日志管理的成本。

**检查方法：**

检查`log_disconnections`参数的值是否为`on`，如果不为`on`则失败。

```sql
openGauss=# show log_disconnections;
log_disconnections
--------------------
off
(1 row)
```

**修复方法：**

设置参数`log_disconnections`为`on`。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_disconnections=on"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_12：确保写入服务器日志的详细度配置正确

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_12

**规则名称：**
确保写入服务器日志的详细度配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_error_verbosity`用于控制写入服务器日志的详细度。有效值包括`TERSE`、`DEFAULT`和`VERBOSE`。

**影响：**
无

**检查方法：**

检查`log_error_verbosity`参数值是否为default，如果不为default则失败。

```sql
openGauss=# show log_error_verbosity;
 log_error_verbosity
---------------------
 default
(1 row)
```

**修复方法：**

设置参数`log_error_verbosity`为`default`。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_error_verbosity=default"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_13：确保日志不记录主机名

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_13

**规则名称：**
确保日志不记录主机名

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_hostname`控制连接日志消息中是否记录主机名。当`log_hostname`设置为`on`时，连接日志消息会同时显示连接主机的IP地址和主机名。由于解析主机名需要一定的时间，这可能会带来额外的性能开销。因此，建议将`log_hostname`设置为`off`，这样连接日志中只记录IP地址而不记录主机名。

**影响：**
无

**检查方法：**

检查`log_hostname`参数值是否为`off`，如果不为`off`则失败。

```sql
openGauss=# show log_hostname;
 log_hostname
--------------
 off
(1 row)
```

**修复方法：**

设置`log_hostname`参数为`off`。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_hostname=off"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_14：确保关闭解析树调试打印开关

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_14

**规则名称：**
确保关闭解析树调试打印开关

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`debug_print_parse`用于控制是否打印查询的解析树结果。当该参数设置为`on`时，查询的解析树结果将被打印到日志中，这可能会占用较多的日志空间，并对查询性能产生负面影响。在生产环境中，建议将`debug_print_parse`参数设置为`off`，以禁止将查询的解析树结果打印到日志中。

**影响：**
无

**检查方法：**

检查`debug_print_parse`参数值是否为`off`，如果不为`off`则失败。

```sql
openGauss=# show debug_print_parse;
debug_print_parse
-----------------
off
(1 row)
```

**修复方法：**

设置参数`debug_print_parse`为`off`。

```bash
gs_guc reload -Z datanode -N all -I all -c "debug_print_parse=off"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_15：确保关闭执行计划调试打印开关

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_15

**规则名称：**
确保关闭执行计划调试打印开关

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`debug_print_plan`用于控制是否打印查询的执行计划到日志中。默认情况下，该参数设置为`off`，表示不打印执行计划。但是，如果将其设置为`on`，则会将查询的执行计划打印到日志中，这可能会占用大量的日志空间，并对查询性能产生负面影响。因此，在生产环境中，建议将`debug_print_plan`参数设置为`off`，以禁止将查询的执行计划打印到日志中。

**影响：**
无

**检查方法：**

检查`debug_print_plan`参数值是否为`off`，如果不为`off`则失败。

```sql
openGauss=# show debug_print_plan;
debug_print_plan
----------------
off
(1 row)
```

**修复方法：**

将`debug_print_plan`参数设置为`off`。

```bash
gs_guc reload -Z datanode -N all -I all -c "debug_print_plan=off"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_7.R_16：确保关闭查询重写调试打印开关

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_16

**规则名称：**
确保关闭查询重写调试打印开关

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`debug_print_rewritten`用于控制是否打印查询重写的结果到日志中。默认情况下，该参数设置为`off`，表示不打印查询重写结果。但是，如果将其设置为`on`，则会将查询重写的结果打印到日志中，这可能会占用大量的日志空间，并对查询性能产生负面影响。因此，在生产环境中，建议将`debug_print_rewritten`参数设置为`off`，以禁止将查询重写结果打印到日志中。

**影响：**
无

**检查方法：**

检查`debug_print_rewritten`参数值是否为`off`，如果不为`off`则失败。

```sql
openGauss=# show debug_print_rewritten;
debug_print_rewritten
----------------------
off
(1 row)
```

**修复方法：**

将`debug_print_rewritten`参数设置为`off`。

```bash
gs_guc reload -Z datanode -N all -I all -c "debug_print_rewritten=off"
```

**参考来源：**
无

## 备份配置

### OPENGAUSS.O_6.G_8.R_1：确保WAL信息记录级别配置正确

**配置组ID：**
OPENGAUSS.G_8

**配置组名称：**
备份配置

**规则ID：**
OPENGAUSS.O_6.G_8.R_1

**规则名称：**
确保WAL信息记录级别配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

WAL（Write Ahead Log）即预写式日志，是数据库用于恢复事务持久性的一种机制。`wal_level`决定了写入WAL的信息量。为了在备机上开启只读查询，`wal_level`需要在主机上设置成`hot_standby`，并且备机设置`hot_standby`参数为`on`。对于分布式环境，不支持设置`hot_standby`为`off`，因此`wal_level`不可设置为`archive`或`minimal`，否则数据库将无法启动。建议设置`wal_level`参数为默认值`hot_standby`。

**影响：**
无

**检查方法：**

检查`wal_level`参数是否为默认值`hot_standby`，如果不是则失败。

```sql
openGauss=# show wal_level;
 wal_level
-----------
 hot_standby
(1 row)
```

**修复方法：**

设置参数`wal_level`值为`hot_standby`，并重启数据库使设置生效。

```bash
gs_guc set -Z datanode -N all -I all -c "wal_level=hot_standby"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无

### OPENGAUSS.O_6.G_8.R_2：确保开启归档模式

**配置组ID：**
OPENGAUSS.G_8

**配置组名称：**
备份配置

**规则ID：**
OPENGAUSS.O_6.G_8.R_2

**规则名称：**
确保开启归档模式

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`archive_mode`用于设置是否开启归档模式，该参数通常只建议当`wal_level`参数设置为`archive`时使用。当`wal_level`参数设置为`minimal`时，`archive_mode`参数无法使用。如果设置`archive_mode`参数为`on`，需要同时设置`archive_command`参数以指定归档WAL日志的命令。

**影响：**

- 开启归档模式后需要规划归档日志占用的磁盘空间。
- 在日志归档过程中可能会对数据库性能产生影响。

**检查方法：**

1. 先检查`wal_level`参数是否为`archive`。
2. 如果`wal_level`为`archive`，则检查`archive_mode`参数值是否为`on`。
3. 如果`wal_level`配置为`hot_standby`，则无需检查`archive_mode`。

```sql
openGauss=# show wal_level;
wal_level
-----------
hot_standby
(1 row)

openGauss=# show archive_mode;
archive_mode
------------
off
(1 row)
```

**修复方法：**

当`wal_level`参数为`archive时`，设置参数`archive_mode`为`on`，同时设置`archive_command`为归档WAL日志的命令，`archive_command`参数的值仅供参考，其中`--remove-destination`选项作用为拷贝前如果目标文件已存在，会先删除已存在的目标文件，然后执行拷贝操作。

```bash
gs_guc reload -Z datanode -N all -I all -c "archive_mode=on"
gs_guc reload -Z datanode -N all -I all -c "archive_command='cp --remove-destination %p /mnt/server/archive/%f'"
```

**参考来源:**
无

## 运行环境配置

### OPENGAUSS.O_6.G_9.R_1：确保文件权限掩码配置正确

**配置组ID:**
OPENGAUSS.G_9

**配置组名称:**
运行环境配置

**规则ID:**
OPENGAUSS.O_6.G_9.R_1

**规则名称:**
确保文件权限掩码配置正确

**级别:**
要求

**规则背景说明:**

在Linux运行环境中，创建文件的默认权限可通过文件权限掩码umask配置。为防止数据库文件被其他用户访问或篡改，应确保umask配置为0077，以确保只有数据库运行用户具有访问权限。umask值一般在`/etc/bashrc`、`/etc/profile`、`$HOME/.bash_profile`或`$HOME/.bashrc`中设置。

**影响:**
umask如果设置不合理，可能导致新建文件权限过小或过大，从而影响业务正常运行或导致安全风险。

**检查方法:**

执行umask命令，查询设置值。

```bash
$ umask
0077
```

**修复方法:**

步骤1：以`$HOME/.bashrc`文件为例，通过vi命令编辑文件，配置umask为0077。

```bash
umask 0077
```

步骤2：执行source $HOME/.bashrc使环境变量生效。

```bash
source $HOME/.bashrc
```

**参考来源：**
无

### OPENGAUSS.O_6.G_9.R_2：确保对其他用户隐藏进程信息

**配置组ID：**
OPENGAUSS.G_9

**配置组名称：**
运行环境配置

**规则ID：**
OPENGAUSS.O_6.G_9.R_2

**规则名称：**
确保对其他用户隐藏进程信息

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

为防止非数据库运行用户通过ps、top等操作系统命令收集数据库运行时的相关进程信息，建议使用`hidepid`选项对其他用户隐藏进程。这样可以确保只有root用户可以查看所有进程，而普通用户只能看到自己的进程。这样可以避免用户进程信息泄露，提升数据库运行环境的安全性。

**影响：**
无

**检查方法：**

通过如下命令检查`/proc`是否配置了`hidepid`选项，如果配置`hidepid=2`则成功，否则失败。

```bash
# mount | grep "proc on /proc" | grep hidepid
proc on /proc type proc (rw,nosuid,nodev,noexec,relatime,hidepid=2)
```

**修复方法：**

使用root用户执行如下`mount`命令，为`/proc`增加`hidepid=2`选项。

```bash
# mount -o remount,rw,nosuid,nodev,noexec,relatime,hidepid=2 /proc
```

编辑`/etc/fstab`文件，增加或修改配置如下，以便在服务器启动时自动启用保护。

```bash
proc /proc proc defaults,nosuid,nodev,noexec,relatime,hidepid=2 0 0
```

**参考来源：**
无

### OPENGAUSS.O_6.G_9.R_3：确保开启NTP时钟同步

**配置组ID：**
OPENGAUSS.G_9

**配置组名称：**
运行环境配置

**规则ID：**
OPENGAUSS.O_6.G_9.R_3

**规则名称：**
确保开启NTP时钟同步

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

NTP（Network Time Protocol，网络时间协议）是同步网络中的各个计算机时间的一种协议。配置NTP可以使计算机的时钟同步到国际标准时间UTC（Universal Time Coordinated，世界协调时），保证数据库服务端的各主机上的系统时间同步。服务端系统时间不同步或时间差异较大可能导致数据库无法正常运行。

**影响：**
无

**检查方法：**

执行如下shell命令，检查ntpd服务是否启动。Active字段返回“active (running)”表示已经启动，返回“inactive (dead)”表示未启动。

```bash
# service ntpd status 2>&1 | grep Active
   Active: inactive (dead)
```

**修复方法：**

在`/etc/ntp.conf`文件中配置合适的NTP服务器，然后执行如下命令重启ntpd服务：

```bash
# service ntpd restart
```

**参考来源：**
无

## 其它配置

### OPENGAUSS.O_6.G_10.R_1：确保backslash_quote参数配置正确

**配置组ID：**
OPENGAUSS.O_6.G_10

**配置组名称:**
其它配置

**规则ID:**
OPENGAUSS.O_6.G_10.R_1

**规则名称:**
确保backslash_quote参数配置正确

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

参数`backslash_quote`控制字符串中是否允许使用`\'`来替代引号。由于历史原因，PostgreSQL接受“\'”的写法，但这种用法可能引发安全风险，如SQL注入攻击。为了避免这种风险，建议配置服务器拒绝带反斜杠转义的引号的查询。推荐使用SQL标准方法，使用一个引号写两遍（`''`）的方法。

**影响：**
无

**检查方法：**

检查`backslash_quote`参数值，如果不为`safe_encoding`或`off`则失败。

```sql
openGauss=# show backslash_quote;
 backslash_quote
-----------------
safe_encoding
(1 row)
```

**修复方法：**

修改参数`backslash_quote`为`safe_encoding`或`off`。

```bash
gs_guc reload -Z datanode -N all -I all -c "backslash_quote=safe_encoding"
```

**参考来源：**
无

### OPENGAUSS.O_6.G_10.R_2：禁止修改系统表结构

**配置组ID：**
OPENGAUSS.O_6.G_10

**配置组名称：**
其它配置

**规则ID：**
OPENGAUSS.O_6.G_10.R_2

**规则名称：**
禁止修改系统表结构

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`allow_system_table_mods`控制是否允许修改系统表的结构。虽然在某些极端情况下，此参数可以帮助恢复受损的数据库，但在生产环境中，修改系统表结构可能会带来严重的安全风险，包括数据丢失和系统不稳定。因此，在生产环境中，应将`allow_system_table_mods`参数设置为`off`。

**影响：**
无

**检查方法：**

检查`allow_system_table_mods`参数值是否为`off`，如果不为`off`则失败。

```sql
openGauss=# show allow_system_table_mods;
 allow_system_table_mods
-------------------------
off
(1 row)
```

**修复方法：**

设置参数`allow_system_table_mods`为`off`，然后重启数据库。设置命令如下：

```bash
gs_guc set -Z datanode -N all -I all -c "allow_system_table_mods=off"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无