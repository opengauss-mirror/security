**<font size="5">OPENGAUSS.O_6.G_2.R_8：确保日志目录权限最小化</font>**

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_8

**规则名称：**
确保日志目录权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`${GAUSSLOG}`为数据库日志目录，目录下日志文件中包含很多运行信息，为了防止日志文件被恶意篡改或破坏给客户的数据信息安全造成威胁，此目录应该受到保护，不允许非数据库安装用户访问。

**影响：**
无

**检查方法：**

执行如下shell命令，如果返回`${GAUSSLOG}`目录则失败。

```bash
find ${GAUSSLOG} -prune \( ! -user ${GAUSSUSER} -o ! -group ${GAUSSGROUP} -o -perm /g=rwx,o=rwx \)
```

环境变量`${GAUSSUSER}`和`${GAUSSGROUP}`需要配置为数据库的安装用户和用户组。

**修复方法：**

```bash
chmod 0700 ${GAUSSLOG}
```

**参考来源：**
无