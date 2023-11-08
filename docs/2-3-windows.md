#### Windows环境手动部署管理端

Windows环境不支持一键部署管理端，用户需要手动部署。

> ##### 下载安装包[HFish-Windows-amd64](https://hfish.cn-bj.ufileos.com/hfish-3.3.4-windows-amd64.tgz) ##### 

> ##### 在防火墙上放行TCP/4433、TCP/4434端口出入双向流量 ##### 

如需其他蜜罐服务，也需要打开对应端口。

> ##### 安装包解压缩后，运行HFish-Windows-amd64目录下的install.bat ##### 

install.bat脚本会在**当前目录**安装HFish，因此运行脚本前请确保当前目录路径恰当。

> ##### 登陆web界面 ##### 

```
登陆链接：https://[ip]:4433/web/
账号：admin
密码：HFish2021
```

如果管理端的IP是192.168.1.1，则登陆链接为：https://192.168.1.1:4433/web/

URL中/web/路径不能少，

安装完成登录后，在「节点管理」页面中可看到管理端服务器上的默认节点，如下图：

<img src="https://hfish.net/images/image-20210914113134975.png" alt="image-20210914113134975" style="zoom: 25%;" />

`注意事项：`

`1、当前HFish分为两个进程,"hfish"进程为管理进程，负责监测、拉起和升级蜜罐主程序。"管理端"进程为蜜罐主程序进程，其执行蜜罐软件程序。因此，安装时候，请务必按照要求，执行hfish进程；如果直接执行管理端程序，可能会导致程序不稳定，升级失败等情况。`

`2、HFish的windows版数据库文件当前存储在 C:\Users\Public\hfish 目录，重装HFish后，HFish默认自动读取该目录内的配置和数据"。`

`3、如果无妨访问Web管理页面，检查TCP/4433和TCP/4434是否可被访问`

