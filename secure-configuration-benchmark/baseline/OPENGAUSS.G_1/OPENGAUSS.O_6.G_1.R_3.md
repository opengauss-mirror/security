**<font size="5">OPENGAUSS.O_6.G_1.R_3：确保数据库实例的最大连接数配置正确</font>**

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