**<font size="5">OPENGAUSS.O_6.G_6.R_6：确保开启数据库对象的添加、删除、修改审计</font>**

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_6

**规则名称：**
确保开启数据库对象的添加、删除、修改审计

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`audit_system_object`决定是否对数据库对象的CREATE、DROP、ALTER操作记录审计日志。这些数据库对象包括DATABASE、USER、SCHEMA、TABLE等。该参数的值由20个二进制位的组合求出，每个二进制位代表openGauss Kernel中的一类数据库对象。如果某个二进制位取值为0，则不审计对应数据库对象的CREATE、DROP、ALTER操作；如果取值为1，则审计这些操作。具体每个二进制位代表的审计对象请参考openGauss的官方文档中对`audit_system_object`参数的说明。

**影响：**
无

**检查方法：**

检查`audit_system_object`参数值配置，如果参数值小于默认值12295则失败。

```sql
openGauss=# show audit_system_object;
 audit_system_object
---------------------
 12295
(1 row)
```

**修复方法：**

参数`audit_system_object`参数值设置为12295，表示对DATABASE、SCHEMA、USER、DATA SOURCE、NODE GROUP等数据库对象的DDL操作的审计。用户可根据业务需要开启对更多数据库对象DDL操作的审计。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_system_object = 12295"
```

**参考来源：**
无