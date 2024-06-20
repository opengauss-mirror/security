**<font size="5">OPENGAUSS.O_6.G_1.R_7：确保UNIX域套接字的访问权限配置正确</font>**

**配置组ID：**
OPENGAUSS.G_1

**配置组名称：**
连接配置

**规则ID：**
OPENGAUSS.O_6.G_1.R_7

**规则名称：**
确保UNIX域套接字的访问权限配置正确

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`unix_socket_permissions`用于设置UNIX域套接字的访问权限。推荐配置是`0700`（只有当前连接数据库的用户自己可以访问，同组或者其他人都没有权限），满足文件权限最小化要求，避免文件被其他用户访问或篡改而影响套接字通信功能。

**影响：**
无

**检查方法：**

检查`unix_socket_permissions`参数配置值是否为`0700`，如果不是则失败。

```sql
openGauss=# show unix_socket_permissions;
 unix_socket_permissions
-------------------------
0700
(1 row)
```

**修复方法：**

修改`unix_socket_permissions`参数值为`0700`，然后重启数据库。

```bash
gs_guc set -Z datanode -N all -I all -c "unix_socket_permissions=0700"
gs_om -t stop && gs_om -t start
```

**参考来源：**
无