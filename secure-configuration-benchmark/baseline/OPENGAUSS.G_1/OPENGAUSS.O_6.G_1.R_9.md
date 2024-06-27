**<font size="5">OPENGAUSS.O_6.G_1.R_9：确保没有host条目使用md5认证</font>**

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_9

**规则名称:**
确保没有host条目使用md5认证

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

md5认证方式存在安全风险，可能导致密码被破解，应采用更安全的sha256认证或证书认证方式。保留md5认证方式是为了兼容开源社区工具，但在生产环境中禁止使用md5认证。

**影响:**
无

**检查方法:**

通过如下shell命令检查`pg_hba.conf`配置中是否存在md5认证条目，其中`${GAUSSDATA}`为DN的数据目录。

```bash
grep -P '^[^#]*host(ssl|nossl)?\s+.+[Mm][Dd][5]\s*$' ${GAUSSDATA}/pg_hba.conf
```

**修复方法:**

为客户端host项配置认证方式为sha256。例如，配置用户`user1`通过IP为`192.168.0.1`的客户端连接数据库`db1`，认证方式为sha256，配置命令如下。

```bash
gs_guc reload -Z datanode -N all -I all -h "host db1 user1 192.168.0.1/32 sha256"
```

**参考来源:**
无