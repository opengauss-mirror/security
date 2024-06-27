**<font size="5">OPENGAUSS.O_6.G_3.R_1：确保客户端认证超时时间配置正确</font>**

**配置组ID:**
OPENGAUSS.G_3

**配置组名称:**
安全认证配置

**规则ID:**
OPENGAUSS.O_6.G_3.R_1

**规则名称:**
确保客户端认证超时时间配置正确

**级别:**
建议

**相关要求:**
无

**规则背景说明:**

参数`authentication_timeout`控制完成客户端认证的时间上限，默认为一分钟。如果一个客户端没有在参数设定时间内完成与服务器端的认证，则服务器自动中断与客户端的连接，这样就避免了出问题的客户端无限制地占用连接数。

**影响:**
参数值设置过小可能因超时导致认证失败。

**检查方法:**

检查`authentication_timeout`参数设置，建议设置为1min。

```sql
openGauss=# show authentication_timeout;
 authentication_timeout
------------------------
 1min
(1 row)
```

**修复方法：**

```bash
gs_guc reload -Z datanode -N all -I all -c "authentication_timeout=1min"
```

**参考来源：**
无