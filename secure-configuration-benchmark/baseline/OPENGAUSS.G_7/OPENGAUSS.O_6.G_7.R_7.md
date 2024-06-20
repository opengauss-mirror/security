**<font size="5">OPENGAUSS.O_6.G_7.R_7：确保客户端日志等级配置正确</font>**

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_7

**规则名称：**
确保客户端日志等级配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`client_min_messages`控制按设置的等级将消息发送到客户端。有效的值包括`debug`、`debug5`、`debug4`、`debug3`、`debug2`、`debug1`、`info`、`log`、`notice`、`warning`、`error`、`fatal`、`panic`，其中`debug`和`debug2`等效。每个等级都包括排在他后面的所有级别中的日志。在实际设置过程中，如果设置的级别大于`error`，例如为`fatal`或`panic`，系统会默认将级别转为`error`。

**影响：**

- 日志级别`debug1`~`debug5`主要用于调试，生产环境不建议使用，否则发送给客户端的日志会增多。
- 建议保持默认值`notice`。

**检查方法：**

检查`client_min_messages`参数值，如果为`debug`或`debug1`~`debug5`则配置可能不正确。

```sql
openGauss=# show client_min_messages;
 client_min_messages
---------------------
 notice
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "client_min_messages=notice"
```

**参考来源：**
无