**<font size="5">OPENGAUSS.O_6.G_7.R_4：禁止覆盖写入同名日志文件</font>**

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