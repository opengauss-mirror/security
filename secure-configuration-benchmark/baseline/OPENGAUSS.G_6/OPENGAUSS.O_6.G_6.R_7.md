**<font size="5">OPENGAUSS.O_6.G_6.R_7：确保开启数据库对象的查询审计</font>**

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_7

**规则名称：**
确保开启数据库对象的查询审计

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`audit_dml_state_select`决定是否对数据库对象的SELECT操作进行审计，默认值为0表示不开启。

**影响：**

开启此选项可以追溯用户对数据库的查询操作，但通常数据库查询操作使用相对频繁，开启此选项后会影响查询性能，并且会导致审计日志记录增加、占用更多磁盘空间。用户可根据业务需要决定是否开启。

**检查方法：**

检查`audit_dml_state_select`参数值是否为1，如果不为1则失败。

```sql
openGauss=# show audit_dml_state_select;
 audit_dml_state_select
------------------------
 0
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_dml_state_select = 1"
```

**参考来源：**
无