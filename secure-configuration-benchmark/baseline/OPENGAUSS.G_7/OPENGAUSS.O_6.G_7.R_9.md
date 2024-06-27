**<font size="5">OPENGAUSS.O_6.G_7.R_9：确保记录产生错误的SQL语句日志级别配置正确</font>**

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