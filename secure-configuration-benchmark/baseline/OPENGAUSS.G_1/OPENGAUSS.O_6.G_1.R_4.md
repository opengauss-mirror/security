**<font size="5">OPENGAUSS.O_6.G_1.R_4：确保Database的最大连接数配置正确</font>**

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_4

**规则名称:**
确保Database的最大连接数配置正确

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

为了控制访问数据库的会话数量，推荐配置会话数量限制在1024个以内。若设置参数`datconnlimit`为-1，表示不限制连接数据库的会话数量。

**影响:**

参数`datconnlimit`设置过小会影响数据库最大并发连接数，设置过大或不限制可能会由于会话数量超出系统负载能力，影响数据库的可用性。

**检查方法:**

执行如下SQL语句检查是否存在不限制连接数的数据库：

```sql
SELECT datname FROM pg_database WHERE datistemplate = false AND datconnlimit = -1;
```

**修复方法:**

```sql
UPDATE pg_database SET datconnlimit=<CONN_LIMIT_VALUE> WHERE datname=<DATABASE_NAME>;
```

其中`<CONN_LIMIT_VALUE>`表示设置的数据库允许的最大会话连接数，`<DATABASE_NAME>`为数据库名称。

**参考来源:**
无