**<font size="5">OPENGAUSS.O_6.G_7.R_5：确保单个日志文件最大记录时间配置正确</font>**

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_5

**规则名称：**
确保单个日志文件最大记录时间配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_rotation_age`用于设置单个日志文件最大的日志记录时间。当日志记录时间超过该参数设置的最大值时，服务器将自动创建新的日志文件。正确的配置有助于避免日志文件过于频繁地产生，同时避免单个日志文件过大导致管理不便。

**影响：**

- 如果`log_rotation_age`参数值设置过小，将导致日志文件频繁产生，增加管理难度。
- 如果参数值设置过大，单个日志文件将记录过多的日志，可能导致文件占用空间过大，同样不利于日志文件管理。

**检查方法：**

检查`log_rotation_age`参数配置，建议配置为默认值`1d`（即一天）。

```sql
openGauss=# show log_rotation_age;
 log_rotation_age
------------------
 1d
(1 row)
```

**修复方法：**

参数`log_rotation_age`单位为min，默认值为1d，即1440min。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_rotation_age=1d"
```

**参考来源：**
无