**<font size="5">OPENGAUSS.O_6.G_7.R_12：确保写入服务器日志的详细度配置正确</font>**

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