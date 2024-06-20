**<font size="5">OPENGAUSS.O_6.G_7.R_6：确保单个日志文件最大容量配置正确</font>**

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_6

**规则名称：**
确保单个日志文件最大容量配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_rotation_size`用于设置单个日志文件的最大容量。当日志文件达到该最大容量时，服务器将自动创建新的日志文件，以避免日志文件过大导致管理困难。

**影响：**

- 如果`log_rotation_size`参数值设置过小，会导致日志文件频繁产生，增加管理难度。
- 如果参数值设置过大，单个日志文件将记录过多的日志，可能导致文件占用空间过大，不利于日志文件管理。

**检查方法：**

检查`log_rotation_size`参数配置，建议配置为默认值`20MB`。

```sql
openGauss=# show log_rotation_size;
 log_rotation_size
-------------------
 20MB
(1 row)
```

**修复方法：**

参数`log_rotation_size`单位为KB，默认值为20MB。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_rotation_size=20MB"
```

**参考来源：**
无