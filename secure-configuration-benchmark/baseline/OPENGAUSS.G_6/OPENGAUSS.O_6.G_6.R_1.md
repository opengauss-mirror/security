**<font size="5">OPENGAUSS.O_6.G_6.R_1：确保开启数据库审计功能</font>**

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_1

**规则名称：**
确保开启数据库审计功能

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

审计日志记录是安全事件中事后追溯、定位问题原因及划分事故责任的重要手段。推荐开启数据库审计功能，将参数`audit_enabled`设置为`on`。

**影响：**

审计日志以二进制形式存储于`pg_audit`目录，开启审计功能后会增加磁盘空间占用，并对性能有一定影响。

**检查方法：**

检查`audit_enabled`参数值是否为`on`，不为`on`则失败。

```sql
openGauss=# show audit_enabled;
 audit_enabled
---------------
on
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_enabled = on"
```

**参考来源：**
无