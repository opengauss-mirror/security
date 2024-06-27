**<font size="5">OPENGAUSS.O_6.G_9.R_2：确保对其他用户隐藏进程信息</font>**

**配置组ID：**
OPENGAUSS.G_9

**配置组名称：**
运行环境配置

**规则ID：**
OPENGAUSS.O_6.G_9.R_2

**规则名称：**
确保对其他用户隐藏进程信息

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

为防止非数据库运行用户通过ps、top等操作系统命令收集数据库运行时的相关进程信息，建议使用`hidepid`选项对其他用户隐藏进程。这样可以确保只有root用户可以查看所有进程，而普通用户只能看到自己的进程。这样可以避免用户进程信息泄露，提升数据库运行环境的安全性。

**影响：**
无

**检查方法：**

通过如下命令检查`/proc`是否配置了`hidepid`选项，如果配置`hidepid=2`则成功，否则失败。

```bash
# mount | grep "proc on /proc" | grep hidepid
proc on /proc type proc (rw,nosuid,nodev,noexec,relatime,hidepid=2)
```

**修复方法：**

使用root用户执行如下`mount`命令，为`/proc`增加`hidepid=2`选项。

```bash
# mount -o remount,rw,nosuid,nodev,noexec,relatime,hidepid=2 /proc
```

编辑`/etc/fstab`文件，增加或修改配置如下，以便在服务器启动时自动启用保护。

```bash
proc /proc proc defaults,nosuid,nodev,noexec,relatime,hidepid=2 0 0
```

**参考来源：**
无