# 创建表

**创建表有两个步骤(与删除表的顺序相反）：**

1）登录控制台，在【表管理】中，创建表的路由信息

2）登录到DRDS中执行"CREATE TABLE"语句

**注意：上述两个操作的顺序必须严格按照先登录控制台创建，再登录DRDS执行 "CREATE TABLE" 语句的顺序**

**1. 进入【表管理】页面**

选择【库管理】-> 【表管理】页面，点击 **【创建表】**

![image.png](https://img1.jcloudcs.com/cms/280ac112-2299-41ad-a324-e024cca0066520180704174109.png)

**2. 创建表路由信息**

**表名称：** 表名称，名称的规则在控制台上有提示

**类型：** 支持“拆分”和“不拆分两种类型”

- 拆分：即该表会实际对应到多个MySQL实例上的多个表

- 不拆分：不对该表进行任何拆分，还是对应1个MySQL实例上的1个表

**拆分字段：** 按照哪个字段进行数据的拆分

**字段类型：** 选择int或者string，后续会开放更多类型的选择

![image.png](https://img1.jcloudcs.com/cms/b10e8a0c-4207-4f8a-a6b8-77c120ddc5c020180704174237.png)

**3. 登录到DRDS中执行"CREATE TABLE"语句**

通过客户端工具链接到DRDS中，执行"CREATE TABLE"语句创建数据表，DRDS会根据前面创建的表的路由信息自动在后端多个MySQL实例上创建实际的表
