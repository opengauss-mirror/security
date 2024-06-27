**<font size="5">OPENGAUSS.O_6.G_7.R_14：确保关闭解析树调试打印开关</font>**

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