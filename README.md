# Mybatis-
1.创建SqlSessionFactory对象，并利用config.xml进行初始化。
a.InputStream is=Resources.getResourcesAsStream（）;
b.SqlSessionFactory	ssf=new SqlSessionFactoryBuilder().build(is);
2.编写confin.xml配置文件用于SqlSessionFactory的初始化。
a.配置<envriments default="默认配置环境">
b.配置<envriment id="配置环境元素标识名">
c.配置<transactionManager type="JDBC" />事务处理方式
d.配置<dataSource type="POOLED"> 数据库属性及配置信息
e.配置Sql映射路径	

3.打开会话
SqlSession sqlSession=ssf.open();
4.编写sql.xml文件
a.配置命名空间
b.配置结果集（返回的javabean类、列名与类属性名的对应关系）
c.配置SQL语句（指明使用的的结果集、定义元素标识名）
