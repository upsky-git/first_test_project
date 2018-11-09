# Linux系统如何安装PAM并设置口令复杂度策略？<a name="ZH-CN_TOPIC_0113390723"></a>

本章节介绍在Linux系统中如何安装PAM并设置口令复杂度策略。

## 安装PAM<a name="section11359864211745"></a>

如果当前系统中未安装PAM（Pluggable Authentication Modules），就无法为系统提供口令复杂度策略检测功能。

若弹性云服务器的操作系统为Debian或Ubuntu，请以管理员用户在命令行终端执行命令**apt-get install libpam-cracklib**进行安装。

>![](public_sys-resources/icon-note.gif) **说明：**   
>CentOS、Fedora、EulerOS系统默认安装了PAM并默认启动。  

## 设置口令复杂度策略<a name="section15343589211814"></a>

为了确保系统的安全性，建议设置的口令复杂度策略为：口令最小长度不小于8，至少包含大写字母、小写字母、数字和特殊字符中的三种。

>![](public_sys-resources/icon-note.gif) **说明：**   
>以下配置为基础的安全要求，如需其他更多的安全配置，请执行以下命令获取Linux帮助信息。  
>-   基于Red Hat 7.0的CentOS、Fedora、EulerOS系统  
>    **man pam\_pwquality**  
>-   其他Linux系统  
>    **man pam\_cracklib**  

-   CentOS、Fedora、EulerOS操作系统

1.  执行以下命令，编辑文件“/etc/pam.d/system-auth“。

    **vi /etc/pam.d/system-auth**

2.  找到文件中的以下内容。
    -   基于Red Hat 7.0的CentOS、Fedora、EulerOS系统：

        password    requisite     pam\_pwquality.so try\_first\_pass retry=3 type=

    -   其他CentOS、Fedora、EulerOS系统：

        password    requisite     pam\_cracklib.so try\_first\_pass retry=3 type=


3.  添加参数“minlen“、“dcredit“、“ucredit“、“lcredit“、“ocredit“。如果文件中已有这些参数，直接修改参数值即可，参数说明如[表1](#table3580982317524)所示。

    示例：

    password    requisite     pam\_cracklib.so try\_first\_pass retry=3 minlen=9 dcredit=-1 ucredit=-1 lcredit=-1 ocredit=-1 type=

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >“dcredit“、“ucredit“、“lcredit“、“ocredit“中至少有三个需要配置为负数。  

    **表 1**  参数说明

    <a name="table3580982317524"></a>
    <table><thead align="left"><tr id="row958328717524"><th class="cellrowborder" valign="top" width="17.29%" id="mcps1.2.4.1.1"><p id="p689461917524"><a name="p689461917524"></a><a name="p689461917524"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="62.6%" id="mcps1.2.4.1.2"><p id="p2159322817524"><a name="p2159322817524"></a><a name="p2159322817524"></a>说明</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.11%" id="mcps1.2.4.1.3"><p id="p100559071253"><a name="p100559071253"></a><a name="p100559071253"></a>示例</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row6012132717524"><td class="cellrowborder" valign="top" width="17.29%" headers="mcps1.2.4.1.1 "><p id="p3798934417524"><a name="p3798934417524"></a><a name="p3798934417524"></a>minlen</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.6%" headers="mcps1.2.4.1.2 "><p id="p4735357317639"><a name="p4735357317639"></a><a name="p4735357317639"></a>口令最小长度配置项。</p>
    <p id="p5723806217524"><a name="p5723806217524"></a><a name="p5723806217524"></a>PAM默认使用了“credits”，因此最小口令长度需要加1，若需要设置最小口令长度为8，则minlen的值应该设置为9。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.11%" headers="mcps1.2.4.1.3 "><p id="p4195134012528"><a name="p4195134012528"></a><a name="p4195134012528"></a>minlen=9</p>
    </td>
    </tr>
    <tr id="row4538051517524"><td class="cellrowborder" valign="top" width="17.29%" headers="mcps1.2.4.1.1 "><p id="p5194311117524"><a name="p5194311117524"></a><a name="p5194311117524"></a>dcredit</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.6%" headers="mcps1.2.4.1.2 "><p id="p5772198217646"><a name="p5772198217646"></a><a name="p5772198217646"></a>口令数字要求的配置项。</p>
    <p id="p4664242617524"><a name="p4664242617524"></a><a name="p4664242617524"></a>值为负数N时表示至少有N个数字，值为正数时对数字个数没有限制。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.11%" headers="mcps1.2.4.1.3 "><p id="p2069760512538"><a name="p2069760512538"></a><a name="p2069760512538"></a>dcredit=-1</p>
    </td>
    </tr>
    <tr id="row1712865817524"><td class="cellrowborder" valign="top" width="17.29%" headers="mcps1.2.4.1.1 "><p id="p4524406617524"><a name="p4524406617524"></a><a name="p4524406617524"></a>ucredit</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.6%" headers="mcps1.2.4.1.2 "><p id="p4503285617653"><a name="p4503285617653"></a><a name="p4503285617653"></a>口令大写字母要求的配置项。</p>
    <p id="p4089071017524"><a name="p4089071017524"></a><a name="p4089071017524"></a>值为负数N时表示至少有N个大写字母，值为正数时对大写字母个数没有限制。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.11%" headers="mcps1.2.4.1.3 "><p id="p165098212546"><a name="p165098212546"></a><a name="p165098212546"></a>ucredit=-1</p>
    </td>
    </tr>
    <tr id="row3247207317524"><td class="cellrowborder" valign="top" width="17.29%" headers="mcps1.2.4.1.1 "><p id="p1299227117524"><a name="p1299227117524"></a><a name="p1299227117524"></a>lcredit</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.6%" headers="mcps1.2.4.1.2 "><p id="p364272491771"><a name="p364272491771"></a><a name="p364272491771"></a>口令小写字母要求的配置项。</p>
    <p id="p4574103717524"><a name="p4574103717524"></a><a name="p4574103717524"></a>值为负数N时表示至少有N个小写字母，值为正数时对小写字母个数没有限制。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.11%" headers="mcps1.2.4.1.3 "><p id="p6006857312555"><a name="p6006857312555"></a><a name="p6006857312555"></a>lcredit=-1</p>
    </td>
    </tr>
    <tr id="row901615717524"><td class="cellrowborder" valign="top" width="17.29%" headers="mcps1.2.4.1.1 "><p id="p5922014817524"><a name="p5922014817524"></a><a name="p5922014817524"></a>ocredit</p>
    </td>
    <td class="cellrowborder" valign="top" width="62.6%" headers="mcps1.2.4.1.2 "><p id="p5842573817711"><a name="p5842573817711"></a><a name="p5842573817711"></a>特殊字符要求的配置项。</p>
    <p id="p3210264617524"><a name="p3210264617524"></a><a name="p3210264617524"></a>值为负数N时表示至少有N个特殊字符，值为正数时对特殊字符个数没有限制。</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.11%" headers="mcps1.2.4.1.3 "><p id="p3108132212614"><a name="p3108132212614"></a><a name="p3108132212614"></a>ocredit=-1</p>
    </td>
    </tr>
    </tbody>
    </table>


-   Debian、Ubuntu操作系统

1.  执行以下命令，编辑文件“/etc/pam.d/common-password“。

    **vi /etc/pam.d/common-password**

2.  找到文件中的以下内容：

    password    requisite     pam\_cracklib.so retry=3 minlen=8 difok=3

3.  添加参数“minlen“、“dcredit“、“ucredit“、“lcredit“、“ocredit“。如果文件中已有这些参数，直接修改参数值即可，参数说明如[表1](#table3580982317524)所示。

    示例：

    password    requisite     pam\_cracklib.so retry=3 minlen=9 dcredit=-1 ucredit=-1 lcredit=-1 ocredit=-1 difok=3



