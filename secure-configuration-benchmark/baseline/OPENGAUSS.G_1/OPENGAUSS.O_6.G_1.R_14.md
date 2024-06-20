**<font size="5">OPENGAUSS.O_6.G_1.R_14：确保服务端使能SSL连接</font>**

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