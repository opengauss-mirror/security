**<font size="5">OPENGAUSS.O_6.G_8.R_1：确保WAL信息记录级别配置正确</font>**

**配置组ID：**
OPENGAUSS.G_8

**配置组名称：**
备份配置

**规则ID：**
OPENGAUSS.O_6.G_8.R_1

**规则名称：**
确保WAL信息记录级别配置正确

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

WAL（Write Ahead Log）即预写式日志，是数据库用于恢复事务持久性的一种机制。`wal_level`决定了写入WAL的信息量。为了在备机上开启只读查询，`wal_level`需要在主机上设置成`hot_standby`，并且备机设置`hot_standby`参数为`on`。对于分布式环境，不支持设置`hot_standby`为`off`，因此`wal_level`不可设置为`archive`或`minimal`，否则数据库将无法启动。建议设置`wal_level`参数为默认值`hot_standby`。

**影响：**
无

**检查方法：**

检查`wal_level`参数是否为默认值`hot_standby`，如果不是则失败。

```sql
openGauss=# show wal_level;
 wal_level
-----------
 hot_standby
(1 row)
```

**修复方法：**

设置参数`wal_level`值为`hot_standby`，并重启数据库使设置生效。

```bash
gs_guc set -Z datanode -N all -I all -c "wal_level=hot_standby"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无