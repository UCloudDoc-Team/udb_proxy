# 安全组说明

数据库代理已支持安全组功能。 若用户账号已开通安全组功能，则数据库代理会自动适配安全组相关功能。

注：如果当前账号没有开通安全组，则可忽略此章节

## 查看账号是否开通安全组
在控制台找到网络模块，点击进入私有网络 UVPC 
![img.png](/images/udb-proxy-secgroup2.png)

若能在私有网络页面上的标签页选项卡中查看到安全组标签页，则说明当前账号已经开启了安全组功能
![img.png](/images/udb-proxy-secgroup3.png)


## 数据库代理的安全组
在[开启数据库代理](/udb_proxy/manage/operator)后，
数据库代理会自动创建一个代理的安全组，其安全组名称以代理ID作为开头。 在其内部绑定了当前代理的资源，此安全组会存在默认的规则。

通过操作数据库代理的安全组规则，可以实现管理数据库代理可以被哪些IP访问。
安全组详细说明和具体操作请见[安全组操作文档](https://docs.ucloud.cn/vpc/introduction/secgroup)


## 安全组规则
除了创建代理自身的安全组外，还会为当前代理的MySQL所处的安全组添加放行数据库代理IP的规则。
每个数据库代理节点会在安全组中添加一条规则，以便于对节点进行管理

规则的优先级为0，以用来允许MySQL和数据库代理之间的通信。
![img.png](/images/udb-proxy-secgroup4.png)


## 使用示例

首先创建MySQL实例，并确保MySQL已加入到安全组当中
![img.png](/images/udb-proxy-secgroup5.png)
![img.png](/images/udb-proxy-secgroup6.png)

[开启数据库代理](/udb_proxy/manage/operator)后回到安全组页面，会发现多出一个以代理ID作为开头的安全组
其入站规则为默认规则
![img.png](/images/udb-proxy-secgroup7.png)
点击MySQL的安全组详情，可以看到安全组多了一条规则
![img.png](/images/udb-proxy-secgroup8.png)
![img.png](/images/udb-proxy-secgroup9.png)
如果想禁止某个IP通过代理访问数据库的话，可以在代理的安全组添加拒绝规则
![img.png](/images/udb-proxy-secgroup10.png)
在实际生产中，如果想让数据库只能由代理访问，不允许通过其他途径访问的话，我们可以设置一个高优先级的拒绝规则拒绝所有IP段，并放行组内(数据库之间)的网络
![img.png](/images/udb-proxy-secgroup11.png)
如下展示了在数据库中添加了拒绝规则前后直连MySQL数据库的情况
![img.png](/images/udb-proxy-secgroup12.png)
同时，我们通过代理进行连接，可以直接连接到数据库
![img.png](/images/udb-proxy-secgroup13.png)


具体安全组相关详细操作参考[安全组操作文档](https://docs.ucloud.cn/vpc/guide/secgroup)

