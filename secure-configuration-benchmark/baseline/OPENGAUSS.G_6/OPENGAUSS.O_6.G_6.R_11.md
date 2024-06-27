**<font size="5">OPENGAUSS.O_6.G_6.R_11：确保所有审计日志文件占用的最大磁盘空间配置正确</font>**

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_11

**规则名称：**
确保所有审计日志文件占用的最大磁盘空间配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`audit_space_limit`设置审计文件所占的最大磁盘空间。当审计文件总量超过最大值时，系统将在数据库日志文件中写入警告信息，并删除最早的审计文件，同时记录审计文件删除信息到审计日志中。

**影响：**

- 设置参数值过大会增加磁盘空间占用。
- 参数值过小则审计日志留存时间变短，可能导致重要日志信息丢失。

**检查方法：**

检查`audit_space_limit`参数值配置。

```sql
openGauss=# show audit_space_limit;
audit_space_limit
-------------------
1GB
(1 row)
```

**修复方法：**

根据实际需要配置参数`audit_space_limit`大小，建议配置不小于1GB。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_space_limit = 1GB"
```

**参考来源：**
无