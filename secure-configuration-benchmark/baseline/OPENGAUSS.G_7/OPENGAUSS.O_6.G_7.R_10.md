**<font size="5">OPENGAUSS.O_6.G_7.R_10：确保开启用户登录时日志记录功能</font>**

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_10

**规则名称：**
确保开启用户登录时日志记录功能

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_connections`用于记录每次尝试连接到服务器的日志，以及成功完成客户端连接认证的日志。

**影响：**

- 开启`log_connections`可以记录所有用户登录尝试的日志，帮助管理员分析潜在的恶意连接或连接问题。
- 但同时，由于会记录所有的连接尝试，可能会导致日志文件增长迅速，增加磁盘存储压力。

**检查方法：**

通过执行以下SQL命令来检查`log_connections`参数值是否为`on`，如果不为`on`则失败。

```sql
openGauss=# show log_connections;
 log_connections
-----------------
 off
(1 row)
```

**修复方法：**

设置参数`log_connections`为`on`。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_connections=on"
```

**参考来源：**
无