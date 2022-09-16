# 主从库权重


## 添加从库到代理中

在创建数据库代理时未开启"从库统一开启"按钮，或者在代理创建后又创建了新的从库。此时需要将从库添加到代理中。

在主从库选项卡中，每个未代理从库左侧都有一个加号，点击后，会将此从库添加到代理中，并重新计算读权重。
![image](/images/read-weight-2.png)

## 从代理中删除从库

在主从库选项卡中，每个已代理从库左侧会有一个小标签，点击后，会将此从库从代理中移除，并重新计算读权重。其中主库是无法移除的。
![image](/images/read-weight-3.png)

## 设置权重策略

在主从库读权重右侧有一个编辑按钮。点击此按钮可以修改读权重策略。
![image](/images/read-weight-4.png)

权重策略包含4种策略：主从库均衡、主库为主、从库均衡、自定义
![image](/images/read-weight-5.png)

主从库均衡：是将请求流量平均分配到主库和从库中，此时每个代理节点的读权重会自动根据节点数量重新进行计算
![image](/images/read-weight-6.png)
![image](/images/read-weight-10.png)

主库为主：是将请求流量全部分配到主库，此时从库的读权重全部变成0%
![image](/images/read-weight-7.png)
![image](/images/read-weight-11.png)

从库均衡：是将请求流量全部分配到从库，此时主库的读权重全部变成0%
![image](/images/read-weight-8.png)
![image](/images/read-weight-12.png)

自定义：可以自由设置主从库请求流量的权重比例，需要所有主从库权重累计为100%
![image](/images/read-weight-9.png)
![image](/images/read-weight-13.png)

