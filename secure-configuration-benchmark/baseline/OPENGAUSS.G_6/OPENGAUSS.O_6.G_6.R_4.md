**<font size="5">OPENGAUSS.O_6.G_6.R_4：确保开启用户锁定和解锁审计</font>**

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_4

**规则名称：**
确保开启用户锁定和解锁审计

**级别：**
要求

**相关要求：**
无

**规则背景说明:**

参数`audit_user_locked`决定是否对数据库用户的锁定和解锁操作记录审计日志。

**影响:**
无

**检查方法:**

检查`audit_user_locked`参数值是否为1，如果不为1则失败。

```sql
openGauss=# show audit_user_locked;
 audit_user_locked
-------------------
 1
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_user_locked = 1"
```

**参考来源：**
无