**<font size="5">OPENGAUSS.O_6.G_7.R_15：确保关闭执行计划调试打印开关</font>**

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