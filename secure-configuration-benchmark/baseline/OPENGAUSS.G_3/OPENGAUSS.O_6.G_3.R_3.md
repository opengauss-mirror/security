**<font size="5">OPENGAUSS.O_6.G_3.R_3：确保账户登录失败尝试次数配置正确</font>**

**配置组ID：**
OPENGAUSS.G_3

**配置组名称：**
安全认证配置

**规则ID：**
OPENGAUSS.O_6.G_3.R_3

**规则名称：**
确保账户登录失败尝试次数配置正确

**级别：**
要求

**规则背景说明：**

通过参数`failed_login_attempts`配置帐户登录失败尝试次数可以防止口令被暴力破解。参数`failed_login_attempts`默认值为10，表示连续认证失败次数超过10次后，帐户将被自动锁定。

**影响：**

配置参数`failed_login_attempts`为非0时，当连续认证失败次数超过此参数值后，帐户将被自动锁定。

**检查方法：**

检查`failed_login_attempts`参数值配置，如果参数为0则配置失败。

```sql
openGauss=# show failed_login_attempts;
 failed_login_attempts
-----------------------
 10
(1 row)
```

**修复方法：**

配置`failed_login_attempts`为大于0小于或等于1000的整数值，建议保持默认值10。

```bash
gs_guc reload -Z datanode -N all -I all -c "failed_login_attempts=10"
```

**参考来源：**
无