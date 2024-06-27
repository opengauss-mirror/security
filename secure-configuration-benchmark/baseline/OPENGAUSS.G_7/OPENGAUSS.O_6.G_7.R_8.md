**<font size="5">OPENGAUSS.O_6.G_7.R_8：确保服务器日志等级配置正确</font>**

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_8

**规则名称：**
确保服务器日志等级配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`log_min_messages`控制按的等级将消息写入到服务器日志。有效的值包括`debug`、`debug5`、`debug4`、`debug3`、`debug2`、`debug1`、`info`、`log`、`notice`、`warning`、`error`、`fatal`、`panic`。其中`debug`和`debug2`等效，每个级别都包含排在他后面的所有级别中的信息。

**影响：**

- 日志级别`debug1`~`debug5`主要用于调试，生产环境不建议使用，否则写入服务器的日志会增多。
- 建议保持默认值`warning`。

**检查方法：**

检查`log_min_messages`参数值，如果为`debug`或`debug1`~`debug5`则配置可能不正确。

```sql
openGauss=# show log_min_messages;
 log_min_messages
------------------
 warning
(1 row)
```

**修复方法：**

设置参数`log_min_messages`为`warning`。

```bash
gs_guc reload -Z datanode -N all -I all -c "log_min_messages=warning"
```

**参考来源：**
无