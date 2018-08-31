# 新节点7<a name="ZH-CN_TOPIC_0128729320"></a>

## 问题描述<a name="section10235653141311"></a>

采用XEN虚拟化技术的Linux弹性云服务器，发生kdump时系统卡住无响应，不能自动重启恢复。例如，用户执行命令**echo c\>/proc/sysrq-trigger**主动触发kdump功能，Linux弹性云服务器卡住，如[图1](#fig1529410182516)所示。

**图 1**  触发kdump功能<a name="fig1529410182516"></a>  
![](figures/触发kdump功能.png "触发kdump功能")

>![](public_sys-resources/icon-note.gif) **说明：**   
>一般情况下，公有云提供的公共镜像已禁用kdump功能。使用公共镜像创建的弹性云服务器不存在该问题。  

## 可能原因<a name="section11577101171411"></a>

-   部分版本的Linux内核与XEN虚拟化平台不适配。
-   内核不支持soft\_rest的弹性云服务器，开启kdump服务时，弹性云服务器在dump时会卡死。

## 处理方法<a name="section85651919262"></a>

**方法一：禁用kdump功能**

以CentOS 7.2为例：

1.  强制重启弹性云服务器。
    1.  登录控制台。
    2.  选择“计算 \> 弹性云服务器”。
    3.  在弹性云服务器列表中，勾选卡住的弹性云服务器，并单击“重启”。
    4.  勾选“强制重启”/“强制关机”，确定强制重启/强制关机弹性云服务器云主机。
    5.  单击“确定”。
2.  关闭kdump功能。
    1.  以root帐号登录强制重启后的弹性云服务器。
    2.  执行以下命令，禁用kdump功能。

        **service kdump stop**
