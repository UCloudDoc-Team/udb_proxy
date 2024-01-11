# 版本管理
数据库代理会随着时间进行功能更新，可通过版本升级将数据库代理的版本升级到最新版以获得最新的功能

## 查看版本

可在数据库代理的列表与详情查看当前版本号

列表
![image](/images/udb-proxy-version-2.png)

详情
![image](/images/udb-proxy-version-1.png)

注：每个版本对应的功能请参考[版本](https://docs.ucloud.cn/udb_proxy/version/version)


## 版本升级

当代理处于可升级的状态时，在详情的版本信息右侧会出现一个升级的按钮
![image](/images/udb-proxy-version-3.png)


点击后，会出现确认弹窗，并显示出可升级到的最新版本
![image](/images/udb-proxy-version-4.png)

点击确定后，代理即处于版本升级中状态

![img.png](/images/udb-proxy-version-5.png)

版本升级中时，不能对数据库代理进行其他操作。
在此时数据库代理的业务功能是正常运行的，依旧可通过数据库代理的ip进行业务使用，不过在升级中使用会出现毫秒级别闪断，请确保业务处于低峰并且业务上有重连机制

## 升级完成

当代理右侧状态处于运行状态时，代理便已升级完成

![img.png](/images/udb-proxy-version-6.png)


