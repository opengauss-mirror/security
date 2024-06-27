**<font size="5">OPENGAUSS.O_6.G_1.R_8：确保除服务端节点外无host条目使用trust认证</font>**

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