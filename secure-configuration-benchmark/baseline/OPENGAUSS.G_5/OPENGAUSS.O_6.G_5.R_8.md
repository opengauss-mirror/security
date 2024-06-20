**<font size="5">OPENGAUSS.O_6.G_5.R_8：确保SECURITY INVOKER类型的函数定义符合预期</font>**

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_8

**规则名称：**
确保SECURITY INVOKER类型的函数定义符合预期

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`SECURITY INVOKER`函数是以调用它的用户的权限来执行，使用不当会导致函数创建者借助执行者的权限执行越权操作，所以在调用非自身创建的这类函数时，一定要先检查函数执行内容，避免造成函数创建者借助执行者的权限执行了越权的操作。

**影响：**
无

**检查方法：**

1、检查普通用户或管理员执行非自身创建的`SECURITY INVOKER`函数，其中`function_name`为被检查函数名称。

```sql
SELECT prosrc FROM pg_proc WHERE proname = 'function_name' AND prosecdef = false;
```

2、检查普通用户或管理员对非自身创建的含有触发器的表执行INSERT/UPDATE/DELETE/TRUNCATE操作，其中table_name为被检查表名。

```sql
SELECT a.prosrc 
FROM pg_proc a 
INNER JOIN PG_TRIGGER c ON a.oid = c.tgfoid 
INNER JOIN PG_CLASS b ON b.oid = c.tgrelid AND b.relname = 'table_name' 
WHERE a.prosecdef = false;
```

**修复方法:**

执行函数前，检查函数执行内容，避免造成函数创建者借助执行者的权限执行了越权的操作。

**参考来源:**
无