**<font size="5">OPENGAUSS.O_6.G_10.R_2：禁止修改系统表结构</font>**

**配置组ID：**
OPENGAUSS.O_6.G_10

**配置组名称：**
其它配置

**规则ID：**
OPENGAUSS.O_6.G_10.R_2

**规则名称：**
禁止修改系统表结构

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`allow_system_table_mods`控制是否允许修改系统表的结构。虽然在某些极端情况下，此参数可以帮助恢复受损的数据库，但在生产环境中，修改系统表结构可能会带来严重的安全风险，包括数据丢失和系统不稳定。因此，在生产环境中，应将`allow_system_table_mods`参数设置为`off`。

**影响：**
无

**检查方法：**

检查`allow_system_table_mods`参数值是否为`off`，如果不为`off`则失败。

```sql
openGauss=# show allow_system_table_mods;
 allow_system_table_mods
-------------------------
off
(1 row)
```

**修复方法：**

设置参数`allow_system_table_mods`为`off`，然后重启数据库。设置命令如下：

```bash
gs_guc set -Z datanode -N all -I all -c "allow_system_table_mods=off"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无