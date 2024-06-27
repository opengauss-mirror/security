**<font size="5">OPENGAUSS.O_6.G_1.R_6：确保用户的最大连接数配置正确</font>**

**配置组ID：**
OPENGAUSS.G_1

**配置组名称：**
连接配置

**规则ID：**
OPENGAUSS.O_6.G_1.R_6

**规则名称：**
确保用户的最大连接数配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

在openGauss数据库中，不应该允许用户无限制数量的连接。如果用户参数`rolconnlimit`设置为-1，表示允许无限制数量的并发连接。根据业务需求限制不同用户的最大连接数，可避免连接被某个用户全部占用。

**影响：**
当前用户实际连接数超过用户的最大连接数限制后无法创建新连接。

**检查方法：**

执行以下SQL语句检查是否存在不限制连接数的用户，其中以`gs_role`开头的为内置角色不允许连接、无需检查。

```sql
SELECT rolname, rolconnlimit FROM pg_roles WHERE rolname NOT LIKE 'gs_role%' AND rolconnlimit = -1;
```

**修复方法：**

```sql
ALTER ROLE <role_name> CONNECTION LIMIT <connection_num>;
```

其中`<role_name>`表示用户名，`<connection_num>`表示配置的最大连接数。

**参考来源：**
无