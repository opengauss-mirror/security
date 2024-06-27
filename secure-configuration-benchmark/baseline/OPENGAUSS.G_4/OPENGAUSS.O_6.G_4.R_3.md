**<font size="5">OPENGAUSS.O_6.G_4.R_3：确保密码不可重用天数配置正确</font>**

**配置组ID：**
OPENGAUSS.G_4

**配置组名称：**
账号口令管理

**规则ID：**
OPENGAUSS.O_6.G_4.R_3

**规则名称：**
确保密码不可重用天数配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

在使用`ALTER USER`或者`ALTER ROLE`修改用户密码时，参数`password_reuse_time`指定是否对新密码进行可重用天数检查。配置此参数后，密码只有超过此设置的时间后才允许被重用。在数据库使用过程中，推荐配置用户密码不可重用天数，以避免用户反复使用相同的密码导致密码被破解。

**影响：**
无

**检查方法：**

检查`password_reuse_time`参数配置，如果值为0则失败。

```sql
openGauss=# show password_reuse_time;
 password_reuse_time
---------------------
 60
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "password_reuse_time=60"
```

**参考来源：**
无