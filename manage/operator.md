# 实例管理

## 开启数据库代理
在UCloud控制台，创建好UDB实例之后，点击实例详情进入二级页面。
![image](/images/udb-proxy-operator1.png)

点击数据库代理标签，即可看到立即开通按钮。
![image](/images/udb-proxy-operator2.png)

选择一个合适的代理机型，配置节点数量，并打开从库统一开启按钮，最终勾选右下角单选框后点击确定按钮（点击查看[功能与限制](/udb_proxy/limit/theory?id=功能限制) ）
![image](/images/udb-proxy-operator11.png)

之后会跳入支付页面，在查看订单信息无误之后，点击右侧立即支付按钮。
![image](/images/udb-proxy-operator12.png)

等待一小段时间后，即可看到数据库代理列表页面，可以查看创建的代理，此时代理状态为初始化中。再等待一段时间即可看到代理变为为运行状态。
![image](/images/udb-proxy-operator13.png)
点击左上角的新增代理,可以创建多个代理。一个MySQL集群创建代理数范围在 1 ～10。
![image](/images/udb-proxy-operator19.png)

## 列表页面操作数据库代理 
1.右侧下拉列表选择“关闭”操作。即可关闭数据库代理。
![image](/images/udb-proxy-operator20.png) 
2.右侧下拉列表选择“重启”操作。即可重启数据库代理。
![image](/images/udb-proxy-operator21.png)
3.右侧下拉列表选择“删除”操作。将会彻底删除选择的代理，将不可恢复。
![image](/images/udb-proxy-operator22.png)
4.侧下拉列表选择“续费”操作。续费成功后将立即生效。
![image](/images/udb-proxy-operator23.png)

## 关闭数据库代理
点击代理“详情”进入详情页面，左上角有关闭按钮。
![image](/images/udb-proxy-operator14.png)

点击后，会出现确认弹框。在确定左侧有“是否彻底删除服务”的单选框，若未勾选，则会关闭此代理，之后可以重新开启，若勾选后，则会彻底删除此代理，代理配置将会丢失。
![image](/images/udb-proxy-operator6.png)

在未勾选"是否彻底删除服务"的单选框后，回到代理详情页面，此时代理状态为已关闭，此时可执行启动、删除、续费操作。
![image](/images/udb-proxy-operator15.png)

在勾选"是否彻底删除服务"的单选框后，代理状态会转变成删除中，一段时间后数据库代理会回到没有开启的状态。
![image](/images/udb-proxy-operator8.png)

## 重启数据库代理
点击代理“详情”进入详情页面，页面左上角有重启按钮。点击后，即可重启数据库代理。
![image](/images/udb-proxy-operator16.png)

## 删除数据库代理

### 关闭时删除
点击代理“详情”进入详情页面,在关闭数据库代理时，勾选彻底删除服务单选框，此时点击确定，数据库代理会被删除，一段时间后，数据库代理会回到没有开启的状态。
![image](/images/udb-proxy-operator17.png)


### 关闭后删除
点击代理“详情”进入详情页面,在关闭数据库代理时若未勾选单选框，则在关闭后左上角会出现删除按钮。此时点击删除按钮，一段时间后，数据库代理会回到没有开启的状态。
![image](/images/udb-proxy-operator18.png)
