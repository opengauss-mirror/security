**<font size="5">OPENGAUSS.O_6.G_9.R_1：确保文件权限掩码配置正确</font>**

**配置组ID:**
OPENGAUSS.G_9

**配置组名称:**
运行环境配置

**规则ID:**
OPENGAUSS.O_6.G_9.R_1

**规则名称:**
确保文件权限掩码配置正确

**级别:**
要求

**规则背景说明:**

在Linux运行环境中，创建文件的默认权限可通过文件权限掩码umask配置。为防止数据库文件被其他用户访问或篡改，应确保umask配置为0077，以确保只有数据库运行用户具有访问权限。umask值一般在`/etc/bashrc`、`/etc/profile`、`$HOME/.bash_profile`或`$HOME/.bashrc`中设置。

**影响:**
umask如果设置不合理，可能导致新建文件权限过小或过大，从而影响业务正常运行或导致安全风险。

**检查方法:**

执行umask命令，查询设置值。

```bash
$ umask
0077
```

**修复方法:**

步骤1：以`$HOME/.bashrc`文件为例，通过vi命令编辑文件，配置umask为0077。

```bash
umask 0077
```

步骤2：执行source $HOME/.bashrc使环境变量生效。

```bash
source $HOME/.bashrc
```

**参考来源：**
无