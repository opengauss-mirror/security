**<font size="5">OPENGAUSS.O_6.G_4.R_1：确保开启密码复杂度校验</font>**

**配置组ID：**
OPENGAUSS.G_4

**配置组名称：**
账号口令管理

**规则ID：**
OPENGAUSS.O_6.G_4.R_1

**规则名称：**
确保开启密码复杂度校验

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

为了保证数据库的使用安全，确保开启密码复杂度校验，在创建用户或者修改密码时校验密码复杂度。密码复杂度过低容易被猜解或暴力破解，为了密码安全性考虑，请开启密码复杂度校验。

**影响:**
无

**检查方法:**

检查`password_policy`参数值是否为1，如果不为1则失败。

```sql
openGauss=# show password_policy;
 password_policy
-----------------
 1
(1 row)
```

**修复方法:**

```bash
gs_guc reload -Z datanode -N all -I all -c "password_policy=1"
```

**参考来源:**
无