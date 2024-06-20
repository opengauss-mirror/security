**<font size="5">OPENGAUSS.O_6.G_2.R_7：确保pg_hba.conf文件权限最小化</font>**

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_7

**规则名称：**
确保pg_hba.conf文件权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

配置文件`pg_hba.conf`包含了连接数据库的配置信息，如客户端认证方法等。为了防止配置文件被恶意篡改，此文件应该受到保护，仅允许数据库的安装用户访问。

**影响：**
无

**检查方法：**

执行如下shell命令，如果返回`pg_hba.conf`文件路径则失败。

```bash
find ${GAUSSDATA}/pg_hba.conf \( ! -user ${GAUSSUSER} -o ! -group ${GAUSSGROUP} -o -perm /u=x,g=rwx,o=rwx \)
```

其中`${GAUSSDATA}`为DN的data目录，用户可通过GUC参数`data_directory`查询DN的data目录。环境变量`${GAUSSUSER}`和`${GAUSSGROUP}`需要配置为数据库的安装用户和用户组。

**修复方法：**

```bash
chmod 0600 ${GAUSSDATA}/pg_hba.conf
```

其中`${GAUSSDATA}`为DN的data目录。

**参考来源：**
无