**<font size="5">OPENGAUSS.O_6.G_5.R_6：确保撤销普通用户非必须的管理权限</font>**

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_6

**规则名称：**
确保撤销普通用户非必须的管理权限

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

普通用户指用于执行普通业务操作的非管理员用户。作为普通用户，不应该拥有超出其正常权限范围的管理权限，例如创建角色权限（CREATEROLE）、创建数据库权限（CREATEDB）、审计权限（AUDITADMIN）、监控权限（MONADMIN）、运维权限（OPRADMIN）、安全策略权限（POLADMIN）等。在满足正常业务需求的前提下，为了确保普通用户权限最小化，应撤销普通用户非必须的管理权限。

**影响：**
无

**检查方法：**

以下列举的是常用的管理权限，其他管理权限的检查方法类似，请根据需要进行排查。

检查拥有CREATEROLE权限的普通用户

```sql
SELECT rolname FROM pg_roles WHERE rolcreaterole = true AND rolsuper = false;
```

检查拥有CREATEDB权限的普通用户

```sql
SELECT rolname FROM pg_roles WHERE rolcreatedb = true AND rolsuper = false;
```

检查拥有AUDITADMIN权限的普通用户

```sql
SELECT rolname FROM pg_roles WHERE rolauditadmin = true AND rolsuper = false;
```

检查拥有MONADMIN权限的普通用户

```sql
SELECT rolname FROM pg_roles WHERE rolmonitoradmin = true AND rolsuper = false;
```

检查拥有OPRADMIN权限的普通用户

```sql
SELECT rolname FROM pg_roles WHERE roloperatoradmin = true AND rolsuper = false;
```

检查拥有POLADMIN权限的普通用户

```sql
SELECT rolname FROM pg_roles WHERE rolpolicyadmin = true AND rolsuper = false;
```

**修复方法：**

撤销CREATEROLE权限

```sql
ALTER ROLE <role_name> NOCREATEROLE;
```

撤销CREATEDB权限

```sql
ALTER ROLE <role_name> NOCREATEDB;
```

撤销AUDITADMIN权限

```sql
ALTER ROLE <role_name> NOAUDITADMIN;
```

撤销MONADMIN权限

```sql
ALTER ROLE <role_name> NOMONADMIN;
```

撤销OPRADMIN权限

```sql
ALTER ROLE <role_name> NOOPRADMIN;
```

撤销POLADMIN权限

```sql
ALTER ROLE <role_name> NOPOLADMIN;
```

**参考来源：**
无