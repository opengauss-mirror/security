**<font size="5">OPENGAUSS.O_6.G_10.R_1：确保backslash_quote参数配置正确</font>**

**配置组ID：**
OPENGAUSS.O_6.G_10

**配置组名称:**
其它配置

**规则ID:**
OPENGAUSS.O_6.G_10.R_1

**规则名称:**
确保backslash_quote参数配置正确

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

参数`backslash_quote`控制字符串中是否允许使用`\'`来替代引号。由于历史原因，PostgreSQL接受“\'”的写法，但这种用法可能引发安全风险，如SQL注入攻击。为了避免这种风险，建议配置服务器拒绝带反斜杠转义的引号的查询。推荐使用SQL标准方法，使用一个引号写两遍（`''`）的方法。

**影响：**
无

**检查方法：**

检查`backslash_quote`参数值，如果不为`safe_encoding`或`off`则失败。

```sql
openGauss=# show backslash_quote;
 backslash_quote
-----------------
safe_encoding
(1 row)
```

**修复方法：**

修改参数`backslash_quote`为`safe_encoding`或`off`。

```bash
gs_guc reload -Z datanode -N all -I all -c "backslash_quote=safe_encoding"
```

**参考来源：**
无