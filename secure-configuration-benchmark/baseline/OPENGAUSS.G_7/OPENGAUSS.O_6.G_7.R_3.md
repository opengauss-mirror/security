**<font size="5">OPENGAUSS.O_6.G_7.R_3：确保日志文件权限配置正确</font>**

**配置组ID：**
OPENGAUSS.G_7

**配置组名称：**
错误报告和日志配置

**规则ID：**
OPENGAUSS.O_6.G_7.R_3

**规则名称：**
确保日志文件权限配置正确

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

当开启参数`logging_collector`时，可以使用参数`log_file_mode`设置服务器日志文件的权限。因为日志文件中可能含有用户数据，所以日志文件访问必须受到限制，以防止日志信息泄露或被篡改。

**影响：**
无

**检查方法：**

检查`log_file_mode`参数值是否为`0600`，如果不是则失败。

```sql
openGauss=# show log_file_mode;
 log_file_mode
---------------
 0600
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "log_file_mode=0600"
```

**参考来源：**
无