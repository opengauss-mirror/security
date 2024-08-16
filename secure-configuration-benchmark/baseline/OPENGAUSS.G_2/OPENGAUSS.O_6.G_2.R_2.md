**<font size="5">OPENGAUSS.O_6.G_2.R_2：确保共享目录权限最小化</font>**

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_2

**规则名称：**
确保共享目录权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`${GAUSSHOME}/share` 目录包含了 openGauss 的共享组件，其中 `${GAUSSHOME}` 为数据库安装目录。为了防止共享组件被恶意篡改或破坏，此目录应该受到保护，不允许非数据库安装用户访问。

**影响：**
无

**检查方法：**

执行如下 shell 命令，如果返回 `${GAUSSHOME}/share` 目录则失败。

```bash
find ${GAUSSHOME}/share -prune -perm /g=rwx,o=rwx
```

**修复方法：**

```bash
chmod  0700 ${GAUSSHOME}/share
```

**参考来源：**
无