**<font size="5">OPENGAUSS.O_6.G_7.R_1：确保开启日志收集器</font>**

**配置组ID：**
OPENGAUSS.G_7

**配置组名称:**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_1

**规则名称：**
确保开启日志收集器

**级别：**
要求

**规则背景说明：**

参数`logging_collector`控制开启后端日志收集进程`logger`进行日志收集。该进程捕获发送到`stderr`或`csvlog`的日志消息并写入日志文件。这种记录日志的方法比将日志记录到`syslog`更加有效，因为某些类型的消息在`syslog`的输出中无法显示。

**影响：**

将服务器日志发送到`stderr`时可以不使用`logging_collector`参数，此时日志消息会被发送到服务器的`stderr`指向的空间。这种方法的缺点是日志回滚困难，只适用于较小的日志容量。

**检查方法：**

检查`logging_collector`参数值是否为`on`，如果不为`on`则失败。

```sql
openGauss=# show logging_collector;
 logging_collector
-------------------
 on
(1 row)
```

**修复方法：**

在postgresql.conf配置文件中修改参数`logging_collector`为`on`，然后重启数据库。

```bash
gs_guc set -Z datanode -N all -I all -c "logging_collector=on"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无