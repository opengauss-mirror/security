**<font size="5">OPENGAUSS.O_6.G_7.R_13：确保日志不记录主机名</font>**

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