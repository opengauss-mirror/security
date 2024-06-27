**<font size="5">OPENGAUSS.O_6.G_1.R_1：禁止侦听主机上所有IP地址</font>**

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