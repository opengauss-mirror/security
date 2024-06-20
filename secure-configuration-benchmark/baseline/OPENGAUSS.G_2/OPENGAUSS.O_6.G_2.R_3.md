**<font size="5">OPENGAUSS.O_6.G_2.R_3：确保二进制文件目录权限最小化</font>**

**配置组ID：**
OPENGAUSS.G_2

**配置组名称：**
文件目录安全

**规则ID：**
OPENGAUSS.O_6.G_2.R_3

**规则名称：**
确保二进制文件目录权限最小化

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

`${GAUSSHOME}/bin` 目录包含了数据库的二进制文件，其中 `${GAUSSHOME}` 为数据库安装目录。为了防止二进制文件被恶意篡改或破坏给客户信息安全造成威胁，此目录应该受到保护，不允许非数据库安装用户访问。

**影响：**
无

**检查方法：**

执行如下 shell 命令，如果返回 `${GAUSSHOME}/bin` 目录则失败。

```bash
find ${GAUSSHOME}/bin -prune -perm /g=rwx,o=rwx
```

**修复方法：**

```bash
chmod  0700 ${GAUSSHOME}/bin
```

**参考来源：**
无