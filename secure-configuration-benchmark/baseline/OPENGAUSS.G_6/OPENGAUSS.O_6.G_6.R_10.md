**<font size="5">OPENGAUSS.O_6.G_6.R_10：确保单个审计日志文件的最大容量配置正确</font>**

**配置组ID:**
OPENGAUSS.G_6

**配置组名称:**
数据库审计

**规则ID:**
OPENGAUSS.O_6.G_6.R_10

**规则名称:**
确保单个审计日志文件的最大容量配置正确

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

参数`audit_rotation_size`设置单个审计日志文件最大的容量。当审计日志文件达到最大容量时，将自动创建一个新的日志文件。

**影响:**

- 参数值设置过小会导致频繁产生审计日志文件。
- 设置过大会导致单个文件记录日志过多、文件占用空间较大，不利于审计日志文件管理。
- 请不要随意调整此参数，否则可能会导致`audit_resource_policy`参数无法生效。

**检查方法:**

检查`audit_rotation_size`参数值配置，建议配置为10MB。

```sql
openGauss=# show audit_rotation_size;
audit_rotation_size
---------------------
10MB
(1 row)
```

**修复方法:**

修改`audit_rotation_size`参数值10MB。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_rotation_size = 10MB"
```

**参考来源：**
无