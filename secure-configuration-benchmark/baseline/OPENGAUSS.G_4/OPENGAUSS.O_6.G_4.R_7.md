**<font size="5">OPENGAUSS.O_6.G_4.R_7：账号口令管理：确保配置密码的有效期限</font>**

**配置组ID:**
OPENGAUSS.G_4

**配置组名称:**
账号口令管理

**规则ID:**
OPENGAUSS.O_6.G_4.R_7

**规则名称:**
确保配置密码的有效期限

**级别:**
建议

**相关要求：**
无

**规则背景说明:**

通过`password_effect_time`参数可以配置用户登录密码的有效期，而`password_notify_time`参数则用于配置密码到期前多少天进行提醒。一旦密码达到过期提醒的时间，系统会在用户登录数据库时提示用户修改密码。建议用户定期更新密码，提升密码使用的安全性。

**影响：**

考虑到数据库使用的特殊性及业务连续性，密码过期后用户仍然可以登录数据库，但每次登录时系统都会提示用户修改密码，直至密码被修改为止。

**检查方法：**

检查`password_effect_time`参数配置，如果值为0则失败。

```sql
openGauss=# show password_effect_time;
 password_effect_time
----------------------
 90
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "password_effect_time=90"
```

**参考来源：**
无