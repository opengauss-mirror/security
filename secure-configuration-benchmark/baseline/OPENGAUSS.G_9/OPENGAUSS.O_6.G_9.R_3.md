**<font size="5">OPENGAUSS.O_6.G_9.R_3：确保开启NTP时钟同步</font>**

**配置组ID：**
OPENGAUSS.G_9

**配置组名称：**
运行环境配置

**规则ID：**
OPENGAUSS.O_6.G_9.R_3

**规则名称：**
确保开启NTP时钟同步

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

NTP（Network Time Protocol，网络时间协议）是同步网络中的各个计算机时间的一种协议。配置NTP可以使计算机的时钟同步到国际标准时间UTC（Universal Time Coordinated，世界协调时），保证数据库服务端的各主机上的系统时间同步。服务端系统时间不同步或时间差异较大可能导致数据库无法正常运行。

**影响：**
无

**检查方法：**

执行如下shell命令，检查ntpd服务是否启动。Active字段返回“active (running)”表示已经启动，返回“inactive (dead)”表示未启动。

```bash
# service ntpd status 2>&1 | grep Active
   Active: inactive (dead)
```

**修复方法：**

在`/etc/ntp.conf`文件中配置合适的NTP服务器，然后执行如下命令重启ntpd服务：

```bash
# service ntpd restart
```

**参考来源：**
无