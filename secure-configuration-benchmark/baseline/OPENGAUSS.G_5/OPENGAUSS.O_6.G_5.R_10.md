**<font size="5">OPENGAUSS.O_6.G_5.R_10：确保取消系统管理员服务端文件COPY权限</font>**

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_10

**规则名称：**
确保取消系统管理员服务端文件COPY权限

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

参数`enable_copy_server_files`允许系统管理员用户执行服务端文件的COPY操作，但远程COPY操作存在越权查看或修改敏感文件的风险。在生产环境下的数据库中，通常不建议打开该配置。该参数的默认值为`off`，表示只允许初始用户执行`COPY FROM FILENAME`或`COPY TO FILENAME`语句。

**影响：**
取消系统管理员的服务端文件COPY权限后，系统管理员将无法进行服务端文件的COPY操作。这一配置对初始用户无影响。

**检查方法：**

检查`enable_copy_server_files`参数值是否为`off`，如果不为off则失败。

```sql
openGauss=# show enable_copy_server_files;
 enable_copy_server_files
--------------------------
off
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "enable_copy_server_files=off"
```

**参考来源：**
无