**<font size="5">OPENGAUSS.O_6.G_6.R_3：确保开启数据库启动、停止、恢复和切换审计</font>**

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_3

**规则名称：**
确保开启数据库启动、停止、恢复和切换审计

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`audit_database_process`决定是否对数据库的启动、停止、切换和恢复操作记录审计日志。开启此选项可以追溯数据库的运行状态变化。

**影响：**
无

**检查方法：**

检查`audit_database_process`参数值是否为1，如果不为1则失败。

```sql
openGauss=# show audit_database_process;
 audit_database_process
------------------------
 1
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_database_process = 1"
```

**参考来源：**
无