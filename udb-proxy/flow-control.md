# sql限流


## 进入sql限流

在数据库代理页面代理信息的最右侧，是sql限流模版，点击编辑按钮，即可进入sql限流设置页面
![image](/images/flow-control-1.png)

在页面左上角有创建模版按钮，点击出现创建限流模版弹框
![image](/images/flow-control-2.png)

## 创建限流模版

在限流模版页面可以针对SELECT、UPDATE、INSERT、DELETE 四种类型的SQL语句设置限流
![image](/images/flow-control-3.png)

我们可以根据实际的业务场景，输入相应的SQL语句，系统会自动将变量（"hello world"）替换成占位符，以适配传入的参数
![image](/images/flow-control-4.png)

在配置限流阈值后，点击确定，可以看到列表页面已经将规则添加进去了
![image](/images/flow-control-5.png)

## 操作限流模版

在创建好限流模版后，可以对限流阈值进行修改，点击限流数值右侧的编辑按钮，可在上侧小弹出框设置阈值
![image](/images/flow-control-6.png)

对限流模版可以进行关闭和启用，操作右侧开关状的小按钮可对限流模版进行关闭和启用操作
![image](/images/flow-control-7.png)

限流模版也可以进行删除操作，删除后不会保留
![image](/images/flow-control-8.png)