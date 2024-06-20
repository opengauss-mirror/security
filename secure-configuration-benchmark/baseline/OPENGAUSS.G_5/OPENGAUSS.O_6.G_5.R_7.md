**<font size="5">OPENGAUSS.O_6.G_5.R_7：禁止PUBLIC角色执行SECURITY DEFINER类型的函数</font>**

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_7

**规则名称：**
禁止PUBLIC角色执行SECURITY DEFINER类型的函数

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

在创建函数时声明`SECURITY DEFINER`表示函数以创建它的用户权限执行，如果使用不当会导致函数执行者借助创建者的权限执行越权操作，所以一定确保这样的函数不被滥用。为了安全考虑，禁止`PUBLIC`角色执行`SECURITY DEFINER`类型的函数。另外需要说明的是，`SECURITY DEFINER`和`AUTHID DEFINER`的功能相同。

**影响：**
禁止`PUBLIC`角色执行`SECURITY DEFINER`类型的函数后，如果其他用户需要执行此函数需要单独授予相应权限，否则会因权限不足导致执行失败。

**检查方法：**

执行如下SQL语句，查询非在`pg_catalog`模式下定位为`SECURITY DEFINER`类型的函数。

```sql
SELECT a.proname, b.nspname 
FROM pg_proc a, pg_namespace b 
WHERE a.pronamespace=b.oid 
AND b.nspname <> 'pg_catalog' 
AND a.prosecdef='t';
```

如果上述语句返回非空，则执行下面的SQL语句检查`PUBLIC`角色是否拥有此函数的执行权限，其中函数需要明确参数类型，必要时还需要在函数名前添加所在模式名前缀。如果返回`true`表示`PUBLIC`角色拥有此函数的执行权限，则检查结果失败。

```sql
SELECT CAST(has_function_privilege('public', 'function_name([arg_type][, ...])', 'EXECUTE') AS TEXT);
```

**修复方法：**

执行如下SQL语句撤销`PUBLIC`角色执行函数的权限，其中函数需要明确参数类型，必要时还需要在函数名前添加所在模式名前缀。

```sql
REVOKE EXECUTE ON FUNCTION function_name([arg_type][, ...]) FROM PUBLIC;
```

**参考来源：**
无