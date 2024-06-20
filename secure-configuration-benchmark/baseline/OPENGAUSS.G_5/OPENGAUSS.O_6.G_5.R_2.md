**<font size="5">OPENGAUSS.O_6.G_5.R_2：禁止PUBLIC角色在public模式下拥有CREATE权限</font>**

**配置组ID：**
OPENGAUSS.G_5

**配置组名称：**
权限管理

**规则ID：**
OPENGAUSS.O_6.G_5.R_2

**规则名称：**
禁止PUBLIC角色在public模式下拥有CREATE权限

**级别：**
要求

**相关要求：**
无

**规则背景说明：**

如果PUBLIC角色在public模式下拥有CREATE权限，则任何用户都可以在public模式下创建表或者其他数据库对象，这可能导致安全风险，因为其他用户也可以查看和修改这些表和数据库对象。此外，为了解决CVE-2018-1058漏洞问题，应禁止PUBLIC角色在public模式下拥有CREATE权限。

**影响：**
配置后PUBLIC角色在public模式下无CREATE权限。

**检查方法：**

通过如下语句检查PUBLIC角色在public模式下是否拥有CREATE权限，如果返回`true`则表示配置失败。

```sql
SELECT CAST(has_schema_privilege('public','public','CREATE') AS TEXT);
has_schema_privilege
----------------------
false
(1 row)
```

**修复方法：**

```sql
REVOKE CREATE ON SCHEMA public FROM PUBLIC;
```

**参考来源：**
[A Guide to CVE-2018-1058: Protect Your Search Path](https://wiki.postgresql.org/wiki/A_Guide_to_CVE-2018-1058%3A_Protect_Your_Search_Path)