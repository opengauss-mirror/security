**<font size="5">OPENGAUSS.O_6.G_1.R_12：确保没有host条目的用户指定为all</font>**

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_12

**规则名称:**
确保没有host条目的用户指定为all

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

host条目配置user为all表示允许所有用户连接到数据库。推荐host条目的user取值仅为需要连接数据库的用户。

**影响:**
如果用户需要连接数据库，但`pg_hba.conf`中没有添加对该用户的配置会导致连接失败。

**检查方法:**

通过如下shell命令检查`pg_hba.conf`配置中是否存在用户指定为all的条目，其中`${GAUSSDATA}`为DN的数据目录。此检查需要人工确认哪些是服务端节点IP和本地环回IP（如127.0.0.1和::1），需确保除服务端节点IP和本地环回IP外无host条目的用户指定为all。

```bash
grep -P '^[^#]*host(ssl|nossl)?\s+\S+\s+[Aa][Ll][Ll]' ${GAUSSDATA}/pg_hba.conf
```

**修复方法:**

除服务端内部连接外，根据业务需要将配置文件`pg_hba.conf`中host、hostssl对应用户为all的条目修改为需要连接数据库的用户。

**参考来源:**
无