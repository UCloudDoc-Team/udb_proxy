# 实例管理

## 开启数据库代理
在UCloud控制台，创建好UDB主从节点之后，点击主节点详情到达管理二级页面：
![image](/images/udb-proxy-operator1.png)

点击数据库代理标签，即可看到立即开通按钮。
![image](/images/udb-proxy-operator2.png)

选择一个合适的代理机型，配置节点数量，并打开从库统一开启按钮，最终勾选右下角单选框后点击确定按钮。
![image](/images/udb-proxy-operator3.png)

等待一小段时间后，即可看到数据库代理详细页面，此时代理状态为初始化中。再等待一段时间即可看到代理变为为运行状态
![image](/images/udb-proxy-operator4.png)


## 关闭数据库代理
在数据库代理页面左上角有关闭按钮。
![image](/images/udb-proxy-operator5.png)

点击后，会出现确认弹框。在确定左侧有一个单选框，若未勾选，则会关闭此代理，之后可以重新开启，若勾选后，则会彻底删除此代理，代理配置将会丢失。
![image](/images/udb-proxy-operator6.png)

在未勾选单选框后，回到代理详情页面，此时代理状态为已关闭，此时可执行启动、删除、重启操作
![image](/images/udb-proxy-operator7.png)

在勾选单选框后，代理状态会转变成删除中，一段时间后数据库代理会回到没有开启的状态
![image](/images/udb-proxy-operator8.png)

## 重启数据库代理
在数据库代理页面左上角有重启按钮。点击后，即可重启数据库代理
![image](/images/udb-proxy-operator9.png)

## 删除数据库代理
在关闭数据库代理时若未勾选单选框，则在关闭后左上角会出现删除按钮。此时点击删除按钮，一段时间后，数据库代理会回到没有开启的状态。
![image](/images/udb-proxy-operator10.png)