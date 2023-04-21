# SQL限流
能在面对流量高峰时限制住某些请求的请求数量，往往是保护后端数据库的重要手段。  
通过数据库代理的SQL限流功能，可以及时限制某类SQL的并发请求，在极端情况下保障数据库的正常工作，避免过载。  
如下列举了一些常见的场景：  
1. 缓存穿透或者业务接口被攻击，导致某个SQL请求并发量暴增。
2. SQL获取的数据庞大，过量请求会导致数据库性能下降
3. 未正确设置索引或SQL过于复杂，占用大量数据库CPU资源


## 进入SQL限流

在数据库代理页面代理信息的右侧，是SQL限流模板，点击编辑按钮，即可进入SQL限流设置页面
![image](/images/flow-control-10.png)

在页面左上角有创建模板按钮，点击出现创建限流模板弹框
![image](/images/flow-control-2.png)

## 创建限流模板

在限流模板页面可以针对SELECT、UPDATE、INSERT、DELETE 四种类型的SQL语句设置限流
![image](/images/flow-control-3.png)

我们可以根据实际的业务场景，输入相应的SQL语句，系统会自动将变量（"hello world"）替换成占位符，以适配传入的参数
![image](/images/flow-control-4.png)

在配置限流阈值后，点击确定，可以看到列表页面已经将规则添加进去了
![image](/images/flow-control-5.png)

## 更新限流模板阈值

在创建好限流模板后，可以对限流阈值进行修改，点击限流数值右侧的编辑按钮，可在上侧小弹出框设置阈值
![image](/images/flow-control-6.png)

## 关闭和启用限流模板

对限流模板可以进行关闭和启用，操作右侧开关状的小按钮可对限流模板进行关闭和启用操作
![image](/images/flow-control-7.png)

## 删除限流模板

限流模板也可以进行删除操作，删除后不会保留
![image](/images/flow-control-8.png)