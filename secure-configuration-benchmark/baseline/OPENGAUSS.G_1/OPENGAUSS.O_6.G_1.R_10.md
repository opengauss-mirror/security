**<font size="5">OPENGAUSS.O_6.G_1.R_10：确保没有hostnossl条目</font>**

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_10

**规则名称:**
确保没有hostnossl条目

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

`hostnossl`条目指定不使用SSL加密连接，而`host`条目允许SSL和非SSL连接，`hostssl`则只能使用SSL连接。从安全角度考虑，推荐使用SSL加密连接对传输数据加密，避免信息泄露。

**影响:**
无

**检查方法:**

通过如下shell命令检查`pg_hba.conf`配置中是否存在`hostnossl`条目，其中`${GAUSSDATA}`为DN的数据目录。

```bash
grep -P '^[^#]*hostnossl' ${GAUSSDATA}/pg_hba.conf
```

**修复方法:**

将配置文件`pg_hba.conf`中所有`hostnossl`条目改为`host`或`hostssl`。

**参考来源:**
无