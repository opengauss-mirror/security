**<font size="5">OPENGAUSS.O_6.G_6.R_2：确保开启用户登录和注销审计</font>**

**配置组ID：**
OPENGAUSS.G_6

**配置组名称：**
数据库审计

**规则ID：**
OPENGAUSS.O_6.G_6.R_2

**规则名称：**
确保开启用户登录和注销审计

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

参数`audit_login_logout`决定是否对用户登录（包括登录成功和登录失败）和注销操作记录审计日志。如果开启此选项可以追溯有哪些用户曾经登录数据库，何时注销登录，否则无法对用户登录和注销情况进行审计。

**影响：**
无

**检查方法：**

检查`audit_login_logout`参数值是否为7，不为7则失败。

```sql
openGauss=# show audit_login_logout;
 audit_login_logout
--------------------
 7
(1 row)
```

**修复方法：**

修改参数值为7，表示用户登录成功、失败和注销均记录审计日志。

```bash
gs_guc reload -Z datanode -N all -I all -c "audit_login_logout = 7"
```

**参考来源：**
无