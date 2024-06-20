**<font size="5">OPENGAUSS.O_6.G_6.R_12：确保审计日志文件最大数目配置正确</font>**

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_12

**规则名称：**
确保审计日志文件最大数目配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`audit_file_remain_threshold`设置审计日志文件的最大保留数量。当审计文件总数超过指定值时，系统将向数据库日志文件中写入警告信息，并删除最早的审计文件，同时记录审计文件删除信息到审计日志中。

**影响：**

- 设置参数值过大会增加磁盘空间占用。
- 参数值过小则审计日志可记录周期变短，可能导致重要日志信息丢失。
- 随意调整此参数可能会影响`audit_resource_policy`参数的效果。

**检查方法：**

检查`audit_file_remain_threshold`参数值配置，通常建议配置为默认值1024。

```sql
openGauss=# show audit_file_remain_threshold;
 audit_file_remain_threshold
-----------------------------
 1024
(1 row)
```

**修复方法：**

修改`audit_file_remain_threshold`参数值为1048576。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_file_remain_threshold = 1048576"
```

**参考来源：**
无