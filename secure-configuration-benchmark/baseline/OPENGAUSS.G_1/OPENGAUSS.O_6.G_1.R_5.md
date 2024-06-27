**<font size="5">OPENGAUSS.O_6.G_1.R_5：确保系统管理员使用的连接数配置正确</font>**

**配置组ID:**
OPENGAUSS.G_1

**配置组名称:**
连接配置

**规则ID:**
OPENGAUSS.O_6.G_1.R_5

**规则名称:**
确保系统管理员使用的连接数配置正确

**级别:**
要求

**相关要求:**
无

**规则背景说明:**

参数`sysadmin_reserved_connections`表示预留给数据库系统管理员的最少连接数，为系统管理员预留连接通道，避免连接被普通用户或恶意用户占用导致管理员无法连接。此参数值必须小于`max_connections`的值。

**影响:**
无

**检查方法:**

```sql
openGauss=# show sysadmin_reserved_connections;
sysadmin_reserved_connections
-------------------------------
3
(1 row)
```

**修复方法:**

修改参数`sysadmin_reserved_connections`为3，然后重启数据库。

```bash
gs_guc set -Z datanode -N all -I all -c "sysadmin_reserved_connections=3"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无