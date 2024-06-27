**<font size="5">OPENGAUSS.O_6.G_3.R_4：确保开启服务端内部Kerberos认证</font>**

**配置组ID：**
OPENGAUSS.G_3
**配置组名称：**
安全认证配置

**规则ID：**
OPENGAUSS.O_6.G_3.R_4

**规则名称：**
确保开启服务端内部Kerberos认证

**级别：**
建议

**相关要求：**
无

**规则背景说明：**

使用`gs_om`工具开启和关闭服务端内部Kerberos认证。如果数据库部署在非安全网络中，通过开启服务端内部Kerberos认证可解决数据库服务端内部节点被仿冒风险。

**影响：**
无

**检查方法：**

可以通过查看DN数据目录下`pg_hba.conf`配置文件，确认服务端内部节点认证方式是否为`gss`，如果为`gss`表示已开启Kerberos认证。执行`cm_ctl query -Cv`查看数据库状态，可以看到Kerberos进程状态。

**修复方法：**

确保数据库处于正常运行状态。首先，执行如下命令停止数据库：

```bash
gs_om -t stop
```

安装server，执行如下命令，其中USER为数据库初始用户，安装服务端，IP1表示主server所在的IP节点，IP2表示备server所在的IP节点。服务端主备IP指定服务端内任意IP即可：

```bash
gs_om -t kerberos -m install -U USER --krb-server IP1 --krb-standby IP2
```

安装client，在服务端内任一节点执行一次命令即可:

```bash
gs_om -t kerberos -m install -U USER --krb-client
```


使环境变量配置生效：

```bash
source ~/.bashrc
```

启动数据库：

```bash
gs_om -t start
```

**参考来源：**
无