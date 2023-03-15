# SQL路由
常规情况下，数据库代理提供的读写分离功能可以有效利用从库，从而提高整个数据库系统的吞吐能力。  
但在某些情况下，我们也希望将SQL路由到指定的数据库执行，以满足我们业务上的要求。  
如下列举出一些场景：
1. 查询语句想要规避主从延迟，将语句路由到主库以保证数据的实时性
2. 将数据统计、复杂计算的查询语句路由到负载权重较低的从库，从而使其和实时业务数据库分离

## 进入SQL路由

在数据库代理页面代理信息的最右侧，是SQL路由功能，点击编辑按钮，即可进入SQL路由设置页面
![image](/images/sql-router-1.png)

在SQL路由页面左上角，有创建路由按钮，点击出现创建SQL路由弹框
![image](/images/sql-router-2.png)

## 创建SQL路由规则
在SQL路由设置页面可以针对SELECT类型的SQL语句设置限流
![image](/images/sql-router-3.png)

我们可以根据实际的业务场景，输入相应的SQL语句，系统会自动将变量（"hello world"）替换成占位符，以适配传入的参数
![image](/images/sql-router-4.png)

根据实际的业务需要，我们可以选择将该条SQL语句路由到主库/从库/自定义数据库上面，其中自定义可以多选
![image](/images/sql-router-5.png)

点击确定，可以在列表中看到规则已经添加进去
![image](/images/sql-router-6.png)

## 修改路由类型
在创建好SQL路由规则后，可以对路由规则进行修改，点击右侧修改路由类型按钮
![image](/images/sql-router-7.png)

点击后，在弹出框中修改路由类型即可
![image](/images/sql-router-8.png)

## 删除路由规则
SQL路由规则可以删除，点击右侧删除按钮后点击确定，即可删除
![image](/images/sql-router-9.png)