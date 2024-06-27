**<font size="5">OPENGAUSS.O_6.G_6.R_8：确保审计优先策略配置正确</font>**

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_8

**规则名称：**
确保审计优先策略配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

控制审计日志的保存策略，以空间还是时间限制为优先策略。

**影响：**

空间策略可以保证审计日志磁盘占用的上限，但是不保证历史审计日志存留；时间限制策略保证特定时间段审计日志的保留，可能日志占用空间会变大。

**检查方法：**

检查`audit_resource_policy`参数值是否为`on`，如果不为`on`则失败。

```sql
openGauss=# show audit_resource_policy;
audit_resource_policy
-----------------------
on
(1 row)
```

**修复方法：**

修改参数`audit_resource_policy`为`on`(空间优先)。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_resource_policy = on"
```

**参考来源:**
无