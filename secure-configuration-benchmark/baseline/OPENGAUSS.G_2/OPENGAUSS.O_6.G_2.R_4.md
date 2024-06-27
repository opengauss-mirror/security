**<font size="5">OPENGAUSS.O_6.G_2.R_4：确保数据目录权限最小化</font>**

**配置组ID:**
OPENGAUSS.G_2

**配置组名称:**
文件目录安全

**规则ID:**
OPENGAUSS.O_6.G_2.R_4

**规则名称:**
确保数据目录权限最小化

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

数据目录包含了用户数据文件，为了防止数据文件被恶意篡改或破坏给客户的数据信息安全造成威胁，此目录应该受到保护，不允许非数据库安装用户访问。

**影响:**
无

**检查方法:**

执行如下 shell 命令，如果返回数据目录则失败。

```bash
find ${GAUSSDATA} -prune \( ! -user ${GAUSSUSER} -o ! -group ${GAUSSGROUP} -o -perm /g=rwx,o=rwx \)
```

其中 `${GAUSSDATA}` 为 DN 的 data 目录，用户可通过 GUC 参数 `data_directory` 查询 DN 的 data 目录。环境变量 `${GAUSSUSER}` 和 `${GAUSSGROUP}` 需要配置为数据库的安装用户和用户组。

**修复方法:**

```bash
chmod 0700 ${GAUSSDATA}
```

其中 `${GAUSSDATA}` 为 DN 的 data 目录。

**参考来源：**
无