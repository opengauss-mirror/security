**<font size="5">OPENGAUSS.O_6.G_3.R_2：确保认证加密迭代次数配置正确</font>**

**配置组ID:**
OPENGAUSS.G_3

**配置组名称:**
安全认证配置

**规则ID:**
OPENGAUSS.O_6.G_3.R_2

**规则名称:**
确保认证加密迭代次数配置正确

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

通过`auth_iteration_count`参数配置对认证凭据进行单向哈希时的迭代次数。迭代次数设置过小会降低口令存储的安全性，设置过大会导致创建用户和认证等涉及口令加密的场景性能劣化。请根据实际硬件条件合理设置迭代次数，迭代次数最低应设置为10000次。

**影响:**

参数值设置过大会导致创建用户和认证等涉及口令加密的场景性能劣化，推荐采用默认迭代次数。

**检查方法:**

检查`auth_iteration_count`参数配置，如果小于10000则失败。

```sql
openGauss=# show auth_iteration_count;
 auth_iteration_count
----------------------
 10000
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "auth_iteration_count=10000"
```

**参考来源：**
无