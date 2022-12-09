# 配置管理


## 修改节点配置

在数据库代理中间部分左侧，是代理节点的配置，点击配置右侧编辑按钮。页面会跳转到修改节点配置页面。
![image](/images/proxy-node-1.png)

里面有两种选项，修改节点配置和增加节点数量，选择目标配置，点击确定即可修改。
![img.png](/images/proxy-node-2.png)

## 扩容节点
修改节点数量
![img.png](/images/proxy-node-3.png)

点击确定后，代理状态和节点状态都处于升降级中，在升降级后代理状态会处于已关闭状态，需手动点击启动按钮。
![img.png](/images/proxy-node-4.png)

## 缩容节点
删除某个节点
![img.png](/images/proxy-node-8.png)

点击确定删除后，代理节点进入删除中状态，等待一段时间后删除。
![img.png](/images/proxy-node-9.png)

## 代理节点更新方案

某些情况下，代理节点需要进行更新，可以采取扩缩容节点的方式对代理节点进行更新

注： 针对长连接的情况，还是会断开连接，请在业务低峰期谨慎进行操作

步骤：

记录当前节点的id
![img.png](/images/proxy-node-11.png)

按照原始的节点数量，按照扩容节点的操作，扩充相同数量的节点
![img.png](/images/proxy-node-10.png)

等待节点处于运行状态
![img.png](/images/proxy-node-12.png)

删除原来记录的节点
![img.png](/images/proxy-node-13.png)
