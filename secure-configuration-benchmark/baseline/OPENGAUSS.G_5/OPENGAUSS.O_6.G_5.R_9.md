**<font size="5">OPENGAUSS.O_6.G_5.R_9：确保开启三权分立配置</font>**

**配置组ID:**
OPENGAUSS.G_5

**配置组名称:**
权限管理

**规则ID:**
OPENGAUSS.O_6.G_5.R_9

**规则名称:**
确保开启三权分立配置

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

设置参数`enableSeparationOfDuty`为`on`会开启三权分立配置，限制系统管理员的权限，系统管理员不再拥有创建用户或更改用户配置权限，并且不再拥有查看和维护数据库审计日志的权限。当开启三权分立时，建议用户关闭GUC参数`enable_copy_server_files`来控制系统管理员的copy权限，防止系统管理员通过copy命令读取或者修改用户配置文件。三权分立特性的详细说明请 参见相关产品文档。

**影响：**

如需使用三权分立权限管理模型，应在数据库初始化阶段指定，不建议来回切换权限管理模型。特别的，如需从非三权分立切换至三权分立权限管理模型，应重新审视已有用户的权限集合是否合理。

**检查方法：**

检查`enableSeparationOfDuty`参数值是否为`on`，如果不为on则失败。

```sql
openGauss=# show enableSeparationOfDuty;
 enableSeparationOfDuty
------------------------
on
(1 row)
```

**修复方法：**

修改参数`enableSeparationOfDuty`为`on`，然后重启数据库。修改命令如下：

```bash
gs_guc set -Z datanode -N all -I all -c "enableSeparationOfDuty = on"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无