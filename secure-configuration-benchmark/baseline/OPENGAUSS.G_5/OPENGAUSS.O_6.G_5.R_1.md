**<font size="5">OPENGAUSS.O_6.G_5.R_1：禁止PUBLIC角色拥有pg_authid系统表的权限</font>**

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_1

**规则名称：**
禁止PUBLIC角色拥有pg_authid系统表的权限

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`pg_catalog`模式下的`pg_authid`系统表中包含了数据库中所有的角色信息。由于所有用户会继承`PUBLIC`角色的权限，为了防止敏感信息泄露或被更改，`PUBLIC`角色不允许拥有`pg_authid`系统表的任何权限。

**影响：**
无

**检查方法：**

执行如下SQL语句，如果查询结果显示不为空则失败。

```sql
SELECT relname,relacl FROM pg_class WHERE relname = 'pg_authid' AND CAST(relacl AS TEXT) LIKE '%,=%}';
```

**修复方法：**

```sql
REVOKE ALL ON pg_authid FROM PUBLIC;
```

**参考来源：**
无