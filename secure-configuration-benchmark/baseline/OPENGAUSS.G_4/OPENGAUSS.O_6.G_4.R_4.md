**<font size="5">OPENGAUSS.O_6.G_4.R_4：确保账户自动解锁时间配置正确</font>**

**配置组ID：**
OPENGAUSS.G_4

**配置组名称：**
账号口令管理

**规则ID：**
OPENGAUSS.O_6.G_4.R_4

**规则名称：**
确保账户自动解锁时间配置正确

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`password_lock_time`用于指定帐户被锁定后自动解锁的时间。参数单位为天，支持浮点数据类型，整数部分表示天数，小数部分可以换算成时、分、秒。参数值为0表示密码验证失败时，自动锁定功能不生效。为防止口令被尝试暴力破解，要求此参数设置为非0值。

**影响：**
无

**检查方法：**

检视`password_lock_time`参数配置，如果值为0则失败。

```sql
openGauss=# show password_lock_time;
 password_lock_time
--------------------
 1d
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "password_lock_time=1"
```

**参考来源：**
无