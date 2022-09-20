# 权重管理


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

