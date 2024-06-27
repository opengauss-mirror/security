**<font size="5">OPENGAUSS.O_6.G_2.R_1：确保数据库安装目录权限最小化</font>**

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_1

**规则名称：**
确保数据库安装目录权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`${GAUSSHOME}` 是 openGauss 的安装目录，为了防止安装目录下的文件被恶意篡改或破坏，此目录应该受到保护，不允许非数据库安装用户访问。正确的权限设置能确保数据库系统的安全性。

**影响：**
无

**检查方法：**

执行如下 shell 命令，如果返回 `${GAUSSHOME}` 目录下的任何文件或目录，则表示权限设置失败。

```bash
find -L ${GAUSSHOME} -prune \( ! -user ${GAUSSUSER} -o ! -group ${GAUSSGROUP} -o -perm /g=rwx,o=rwx \)
```

环境变量 `${GAUSSUSER}` 和 `${GAUSSGROUP}` 需要配置为数据库的安装用户和用户组。

**修复方法:**

```bash
chmod 0700 ${GAUSSHOME}
```

**参考来源:**
无