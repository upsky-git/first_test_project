# 一键重置密码后无法使用新密码登录弹性云服务器<a name="ZH-CN_TOPIC_0105187294"></a>

请根据如下原因逐一进行排查（以Linux操作系统的弹性云服务器为例）：

1.  检查安全组出方向80端口是否放通。
    1.  登录控制台。
    2.  选择需要检查的弹性云服务器，并进入“弹性云服务器”详情页面。
    3.  检查“安全组”中，“出方向”的“80”端口是否放通。

        默认的安全组规则“出方向”为Any 、Any，即端口放通。

2.  检查弹性云服务器VPC的DHCP是否启用。

    选择“网络 \> 虚拟私有云"，打开对应VPC的详情页面，选择“子网”页签，启用DHCP。

    **图 1**  启用DHCP<a name="fig582618286211"></a>  
    ![](figures/启用DHCP.png "启用DHCP")

3.  如果安全组配置、DHCP均正常，但一键重置密码功能仍未生效，请尝试使用原密码登录弹性云服务器。
    -   如果原密码失效，可以进入单用户模式下进行密码重置。
    -   如果原密码有效，可以用原密码登录弹性云服务器后进入操作系统内进一步排查：
        1.  使用原密码登录Linux弹性云服务器。
        2.  执行**curl http://169.254.169.254/openstack/latest/resetpwd\_flag**。

            -   返回为“true”，表示可以一键重置密码。
            -   返回其他，表示不支持重置密码或网络异常。

            ![](figures/zh-cn_image_0110509363.png)


4.  检查是否已安装“CloudResetPwdAgent”。

    1.  检查弹性云服务器的根目录下，是否存在“CloudrResetPwdAgent”目录。
    2.  执行以下命令，确认“CloudResetPwdAgent”的状态不是“unrecognized service”。

        **service cloudResetPwdAgent status**


    如果以上两个条件均不满足，说明当前弹性云服务器没有安装一键重置密码插件，安装方法请参见[安装一键式重置密码插件](https://support.huaweicloud.com/qs-ecs/zh-cn_topic_0068095385.html)。
