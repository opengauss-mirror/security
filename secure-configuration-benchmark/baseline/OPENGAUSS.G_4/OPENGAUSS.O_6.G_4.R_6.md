**<font size="5">OPENGAUSS.O_6.G_4.R_6：账号口令管理：确保配置用户的有效期限</font>**

**配置组ID:**
OPENGAUSS.G_4

**配置组名称:**
账号口令管理

**规则ID:**
OPENGAUSS.O_6.G_4.R_6

**规则名称:**
确保配置用户的有效期限

**级别:**
建议

**相关要求：**
无

**规则背景说明:**

创建用户或角色时，使用`VALID BEGIN`关键字设置用户的有效开始时间，`VALID UNTIL`关键字设置用户的有效结束时间。如果忽略这两个关键字，则用户或角色将长期有效。数据库服务端各节点的用户过期时间以各节点操作系统的时钟为依据。为确保服务端各节点的时间一致性，建议在安装部署数据库时使用NTP（网络时间协议）。若忽略这一配置，可能存在各节点登录帐户过期时间不一致的风险。因此，建议根据业务需要合理地配置用户或角色的有效期，并及时清理无用的过期用户或角色。

**影响：**

配置用户有效期后，当用户不在有效期限范围内时，将无法与数据库建立连接。

**检查方法：**

通过如下SQL语句检查是否存在未配置有效期的用户，其中，`WHERE`条件中`rolsuper=true`时表示初始用户，无需配置有效期限；以`gs_role`开头的为数据库内置角色，也无需配置有效期限。

```sql
SELECT rolname, rolvalidbegin, rolvaliduntil 
FROM pg_roles 
WHERE rolsuper=false 
AND rolname NOT LIKE 'gs_role%' 
AND (rolvalidbegin IS NULL OR rolvaliduntil IS NULL);
```

**修复方法:**

```sql
ALTER ROLE <role_name> VALID BEGIN 'yyyy-mm-dd' VALID UNTIL 'yyyy-mm-dd';
```

**参考来源:**
无