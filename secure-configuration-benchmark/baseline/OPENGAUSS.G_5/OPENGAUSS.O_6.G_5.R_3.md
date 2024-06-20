**<font size="5">OPENGAUSS.O_6.G_5.R_3：禁止将对象的所有权限授予PUBLIC角色</font>**

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_3

**规则名称：**
禁止将对象的所有权限授予PUBLIC角色

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

PUBLIC角色属于任何用户，如果将对象的所有权限授予PUBLIC角色，则任意用户都会继承此对象的所有权限，违背权限最小化原则。为了保障数据库数据的安全，此角色应该拥有尽可能少的权限，应禁止将对象的所有权限授予PUBLIC角色。

**影响：**
无

**检查方法：**

通过如下语句检查表或视图的所有权限是否授予PUBLIC角色，如果结果不为空则失败。

```sql
SELECT relname,relacl FROM pg_class 
WHERE (CAST(relacl AS TEXT) LIKE '%,=arwdDxt/%}' OR CAST(relacl AS TEXT) LIKE '{=arwdDxt/%}') 
AND (CAST(relacl AS TEXT) LIKE '%,=APmiv/%}' OR CAST(relacl AS TEXT) LIKE '{=APmiv/%}');
```

通过如下语句检查模式的所有权限是否授予PUBLIC角色，如果结果不为空则失败。

```sql
SELECT nspname,nspacl FROM pg_namespace 
WHERE (CAST(nspacl AS TEXT) LIKE '%,=UC/%}' OR CAST(nspacl AS TEXT) LIKE '{=UC/%}') 
AND (CAST(nspacl AS TEXT) LIKE '%,=APm/%}' OR CAST(nspacl AS TEXT) LIKE '{=APm/%}');
```

通过如下语句检查函数的所有权限是否授予PUBLIC角色，如果结果不为空则失败。

```sql
SELECT proname,proacl FROM pg_proc 
WHERE (CAST(proacl AS TEXT) LIKE '%,=X/%}' OR CAST(proacl AS TEXT) LIKE '{=X/%}') 
AND (CAST(proacl AS TEXT) LIKE '%,=APm/%}' OR CAST(proacl AS TEXT) LIKE '{=APm/%}');
```

其他数据库对象的权限检查可以参考上述命令进行排查。ACL权限参数说明如下表所示。

| 参数 | 参数说明 |
| --- | --- |
| r | SELECT |
| w | UPDATE |
| a | INSERT |
| d | DELETE |
| D | TRUNCATE |
| x | REFERENCES |
| t | TRIGGER |
| X | EXECUTE |
| U | USAGE |
| C | CREATE |
| c | CONNECT |
| T | TEMPORARY |
| A | ALTER |
| P | DROP |
| m | COMMENT |
| i | INDEX |
| v | VACUUM |
| * | 给前面权限的授权选项 |

**修复方法：**

撤销PUBLIC角色拥有的表或视图的所有权限

```sql
REVOKE ALL ON <OBJECT_NAME> FROM PUBLIC;
```

撤销PUBLIC角色拥有的模式的所有权限

```sql
REVOKE ALL ON SCHEMA <OBJECT_NAME> FROM PUBLIC;
```

撤销PUBLIC角色拥有的函数的所有权限（注意函数对象名称需要包含参数）

```sql
REVOKE ALL ON FUNCTION function_name([arg_type][, ...]) FROM PUBLIC;
```

**参考来源：**
无