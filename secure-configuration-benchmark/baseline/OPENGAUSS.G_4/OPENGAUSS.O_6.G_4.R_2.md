**<font size="5">OPENGAUSS.O_6.G_4.R_2：确保密码加密方式配置正确</font>**

**配置组ID:**
OPENGAUSS.G_4

**配置组名称:**
账号口令管理

**规则ID:**
OPENGAUSS.O_6.G_4.R_2

**规则名称:**
确保密码加密方式配置正确

**级别:**
要求

**相关要求：**
无

**规则背景说明:**

参数`password_encryption_type`用于配置数据库采用何种加密方式对用户密码进行加密存储。参数支持3种配置方式：

- 0：采用md5方式对密码加密
- 1：采用sha256和md5两种方式分别对密码加密
- 2：采用sha256方式对密码加密

md5方式已经证明不安全，不应该配置，保留仅为兼容开源第三方工具。应该配置为sha256方式（默认配置）。

**影响:**
无

**检查方法:**

检查`password_encryption_type`参数配置，如果为0或1则失败。

```sql
openGauss=# show password_encryption_type;
 password_encryption_type
--------------------------
 2
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "password_encryption_type=2"
```

**参考来源：**
无