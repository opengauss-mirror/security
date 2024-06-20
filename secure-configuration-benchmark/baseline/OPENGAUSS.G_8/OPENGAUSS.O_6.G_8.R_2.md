**<font size="5">OPENGAUSS.O_6.G_8.R_2：确保开启归档模式</font>**

**配置组ID：**
OPENGAUSS.G_8

**配置组名称：**
备份配置

**规则ID：**
OPENGAUSS.O_6.G_8.R_2

**规则名称：**
确保开启归档模式

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`archive_mode`用于设置是否开启归档模式，该参数通常只建议当`wal_level`参数设置为`archive`时使用。当`wal_level`参数设置为`minimal`时，`archive_mode`参数无法使用。如果设置`archive_mode`参数为`on`，需要同时设置`archive_command`参数以指定归档WAL日志的命令。

**影响：**

- 开启归档模式后需要规划归档日志占用的磁盘空间。
- 在日志归档过程中可能会对数据库性能产生影响。

**检查方法：**

1. 先检查`wal_level`参数是否为`archive`。
2. 如果`wal_level`为`archive`，则检查`archive_mode`参数值是否为`on`。
3. 如果`wal_level`配置为`hot_standby`，则无需检查`archive_mode`。

```sql
openGauss=# show wal_level;
wal_level
-----------
hot_standby
(1 row)

openGauss=# show archive_mode;
archive_mode
------------
off
(1 row)
```

**修复方法：**

当`wal_level`参数为`archive时`，设置参数`archive_mode`为`on`，同时设置`archive_command`为归档WAL日志的命令，`archive_command`参数的值仅供参考，其中`--remove-destination`选项作用为拷贝前如果目标文件已存在，会先删除已存在的目标文件，然后执行拷贝操作。

```bash
gs_guc reload -Z datanode -N all -I all -c "archive_mode=on"
gs_guc reload -Z datanode -N all -I all -c "archive_command='cp --remove-destination %p /mnt/server/archive/%f'"
```

**参考来源:**
无