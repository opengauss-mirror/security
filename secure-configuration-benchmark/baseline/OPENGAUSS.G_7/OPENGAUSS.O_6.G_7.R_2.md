**<font size="5">OPENGAUSS.O_6.G_7.R_2：确保日志名称配置正确</font>**

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_2

**规则名称：**
确保日志名称配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_filename`设置服务器运行日志文件的名称。建议使用`%`转义字符定义日志文件名称，以便能够自动包含日期和时间信息，从而方便对日志文件进行有效的管理。

**影响：**
无

**检查方法：**

检查`log_filename`参数配置，建议保持默认配置，即使用包含日期和时间信息的格式。

```sql
openGauss=# show log_filename;
          log_filename
--------------------------------
 postgresql-%Y-%m-%d_%H%M%S.log
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "log_filename = 'postgresql-%Y-%m-%d_%H%M%S.log'"
```

**参考来源：**
无