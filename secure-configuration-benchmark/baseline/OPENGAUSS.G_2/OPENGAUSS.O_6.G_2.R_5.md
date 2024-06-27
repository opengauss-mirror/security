**<font size="5">OPENGAUSS.O_6.G_2.R_5：确保日志归档目录权限最小化</font>**

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_5

**规则名称：**
确保日志归档目录权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`${GAUSSHOME}/archive` 目录为日志归档目录，其中 `${GAUSSHOME}` 为数据库安装目录。当 `wal_level` 参数配置为 `archive` 时，该目录权限应该设置为 `0700` 以确保只允许数据库的安装运行用户访问。

**影响：**
无

**检查方法：**

执行如下 shell 命令，如果返回 `${GAUSSHOME}/archive` 目录则失败。如果 `${GAUSSHOME}/archive` 目录不存在则无需进行检查。

```bash
find ${GAUSSHOME}/archive -prune \( ! -user ${GAUSSUSER} -o ! -group ${GAUSSGROUP} -o -perm /g=rwx,o=rwx \)
```

环境变量 `${GAUSSUSER}` 和 `${GAUSSGROUP}` 需要配置为数据库的安装用户和用户组。

**修复方法：**

```bash
chmod 0700 ${GAUSSHOME}/archive
```

**参考来源：**
无