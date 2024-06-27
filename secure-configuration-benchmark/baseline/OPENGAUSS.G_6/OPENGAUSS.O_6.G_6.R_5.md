**<font size="5">OPENGAUSS.O_6.G_6.R_5：确保开启权限授予和回收审计</font>**

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_5

**规则名称：**
确保开启权限授予和回收审计

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`audit_grant_revoke`决定是否对数据库用户权限授予和回收的操作记录审计日志。

**影响：**
无

**检查方法：**

检查`audit_grant_revoke`参数值是否为1，如果不为1则失败。

```sql
openGauss=# show audit_grant_revoke;
audit_grant_revoke
--------------------
1
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_grant_revoke = 1"
```

**参考来源：**
无