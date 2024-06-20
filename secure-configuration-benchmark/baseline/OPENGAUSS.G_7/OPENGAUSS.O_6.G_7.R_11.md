**<font size="5">OPENGAUSS.O_6.G_7.R_11：确保开启用户注销时日志记录功能</font>**

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_11

**规则名称：**
确保开启用户注销时日志记录功能

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_disconnections`用于设置是否记录客户端结束连接的信息，包括在会话结束时在服务器日志中输出一行，并包含会话的持续时间。

**影响：**

- 开启`log_disconnections`参数有助于分析客户端连接的断开情况，包括断开原因和会话持续时间。
- 同时，开启此参数可能会增加日志记录量，需要考虑到磁盘存储和日志管理的成本。

**检查方法：**

检查`log_disconnections`参数的值是否为`on`，如果不为`on`则失败。

```sql
openGauss=# show log_disconnections;
log_disconnections
--------------------
off
(1 row)
```

**修复方法：**

设置参数`log_disconnections`为`on`。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_disconnections=on"
```

**参考来源：**
无