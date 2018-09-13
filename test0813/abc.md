## Step 1: Purchase an ECS<a name="section761474661113"></a>

1.  Log in to the management console.
2.  Click  ![](figures/en-us_image_0070749810.png)  in the upper left corner and select the desired region and project.
3.  Under  **Computing**, click **Elastic Cloud Server**.
4.  Click  **Buy ECS**.

    The ECS purchasing page is displayed.

    >![](public_sys-resources/icon-note.gif) **NOTE:**   
    >SAP High-Performance Analytic Appliance \(HANA\) is a high-performance real-time data computing platform based on memory computing technologies. The public cloud provides high-performance IaaS services that comply with SAP HANA requirements. These services include applying for HANA ECSs and public IP addresses as well as installing and configuring SAP HANA. Such services facilitate applications on the public cloud platform of resources required by SAP HANA, improving the efficiency of user operations, reducing operation costs, and enhancing user experience.  
    >HANA ECSs are dedicated for SAP HANA. If you have deployed SAP HANA on cloud servers, you can purchase HANA ECSs.  
    >For more information about HANA ECS application scenarios and purchasing methods, see  _SAP HANA User Guide_.  

5.  Select a billing mode,  **Yearly/Monthly** or **Pay-per-use**.
    -   In  **Yearly/Monthly** billing mode, purchase an ECS configuration and set **Validity Period**. Then, the system deducts the fees incurred at one time from your account based on the service price.

        >![](public_sys-resources/icon-note.gif) **NOTE:**   
        >The ECSs paid in monthly/yearly mode cannot be deleted. They support only resource unsubscription. If an ECS is no longer used, switch to the  **Elastic Cloud Server** page, click **More** in the **Operation** column of this ECS, and select **Unsubscribe**  to unsubscribe it.  

    -   In  **Pay-per-use** billing mode, after purchasing an ECS configuration, you do not need to set **Validity Period**. Then, the system deducts the fees incurred from your account based on the service duration.

6.  Select a region.

    ECSs in different regions cannot communicate with each other over an intranet. For low network latency and quick resource access, select the nearest region.

7.  Select an AZ.

    An AZ is a physical region where power and networks are physically isolated. AZs in the same region can communicate with each other over an intranet.

    -   To enhance application availability, create ECSs in different AZs.
    -   To shorten network latency, create ECSs in the same AZ.

8.  Set  **Specifications**.

    The public cloud provides various ECS types for different application scenarios. You can view released ECS types and specifications in the list. Alternatively, you can enter a flavor \(such as **c3**\) or specify vCPUs and memory size to search for the desired flavor.

    **Latest generations** show the types and specifications of newly released ECSs, and **All generations** show the types and specifications of all ECSs provided by the public cloud.

    >![](public_sys-resources/icon-note.gif) **NOTE:**   
    >-   Before selecting an ECS type, learn the introduction and notes on each type of ECSs. For details, see section  [Instances and Application Scenarios](http://support.huaweicloud.com/en-us/productdesc-ecs/en-us_topic_0035470096.html).  
    >-   When purchasing an ECS, you are not allowed to select sold-out CPU and memory resources.  
    >-   **Local Disk**: specifies the local storage of the physical host where the ECS is deployed. Only Hard Disk Driver \(HDD\) disks are supported. If the ECS of the selected type \(such as **Disk-intensive**\) uses local disks, the system automatically attaches the local disks to the ECS and displays the information of the local disks.  
    >    For example, if  **Local Disk** is **3x1,800 GB \(HDD\)**, three HDDs are attached to the ECS and the capacity of each HDD is 1800 GB.  

9.  Click  **Image**.
    -   Public image

        A public image is a standard, widely used image. It contains an OS and preinstalled public applications and is available to all users. You can configure the applications or software in the public image as needed.


    -   Private image

        A private image is an image available only to the user who creates it. It contains an OS, preinstalled public applications, and the user's private applications. Using a private image to create ECSs removes the need to configure multiple ECSs repeatedly.

        You can also select an encrypted image. For details, see  _Image Management Service User Guide_.

        If you have used a CSBS backup to create a private image \(full-ECS image\), you can use the full-ECS image. However, the EVS disk in the image does not support disk creation using a data disk image, and disk attributes \(such as SCSI/VBD and data encryption\) cannot be modified. The ECSs created using a full-ECS image do not support DSS disks. For more details about how to use CSBS backups to create images, see section "Using Backups to Create Images" in  _Cloud Server Backup Service User Guide_  and section "Creating a Full-ECS Image Using a CSBS Backup" in  _Image Management Service User Guide_.

    -   Shared image

        A shared image is a private image shared by another user.

    -   Marketplace image

        The Marketplace is a store where you can purchase third-party images that have the OS, application environment, and software pre-installed. You can use the images to deploy websites and application development environments with a few clicks, and no additional configuration operation is required.

        If you use a Marketplace image, after you click  **Marketplace image**, the system displays Marketplace images for you to select. For example, if the image product is **name1 \(test\_001\)**, **name1** is the image name, and **test\_001** is the product name. You can search for your desired Marketplace image by image name or product name. Alternatively, you can click the image name to view more information about the product. 


10. Set  **Disk**.

    Disks are classified as EVS disks and DSS disks based on whether the storage resources used by the disks are exclusive. DSS disks allow you to use exclusive storage resources.

    -   If you have applied for a storage pool on the DSS page, click the  **DSS**  tab and create disks in the obtained storage pool.
    -   If you have not applied for an exclusive storage pool, click the  **Disks**  tab and create EVS disks that use public storage resources.

        >![](public_sys-resources/icon-note.gif) **NOTE:**   
        >-   When you use DSS resources to create a disk, the disk type must be the same as that of the requested storage pool. For example, both are of high I/O type.  
        >-   For more information about DSS, see  _Dedicated Distributed Storage Service User Guide_.  


    A disk can be a system disk or a data disk. When creating an ECS, you can add up to 24 disks with customized sizes to it. After the ECS is created, you can add up to 60 disks to such a newly created ECS. The system disk size of a P1 or P2 ECS must be greater than or equal to 15 GB. It is recommended that the system disk size be greater than 40 GB.

    -   System Disk

        If the image based on which an ECS is created is not encrypted, the system disk of the ECS is not encrypted. In addition,  **Unencrypted** is displayed for the system disk on the page. If the image based on which an ECS is created is encrypted, the system disk of the ECS is automatically encrypted. For details, see section [\(Optional\) Encryption-related parameters](#en-us_topic_0021831611_li126651425205814).

    -   Data Disk

        You can create multiple data disks for an ECS and configure sharing and encryption for each data disk.

        -   **SCSI**: indicates that the device type of the data disk is SCSI. For more information about SCSI disks and the ECSs that can be attached with SCSI disks, see section [Storage](http://support.huaweicloud.com/en-us/productdesc-ecs/en-us_topic_0030828256.html).
        -   **Share**: indicates that the EVS disk is shared. Such an EVS disk can be attached to multiple ECSs.
        -   **Encryption**: indicates that the data disk is encrypted. For details, see section [\(Optional\) Encryption-related parameters](#en-us_topic_0021831611_li126651425205814).
        -   **Create Disk from Data Disk Image**: If you have created a data image on the **Image Management Service**  page, when using a Windows or Linux image to create an ECS, you can use a data disk image to create a disk for the ECS.

            Click  **Create Disk from Data Disk Image**. In the dialog box that is displayed, select your data image.

            >![](public_sys-resources/icon-note.gif) **NOTE:**   
            >-   One data disk image can be used only for one data disk.  
            >-   When you use a data disk image to create a disk,  **SCSI**, **Share**, and **Encryption**  are unavailable.  
            >-   For instructions about how create a data image, see  _Image Management Service User Guide_.  


    -   <a name="en-us_topic_0021831611_li126651425205814"></a>\(Optional\) Encryption-related parameters

        To enable encryption, click  **Create Xrole** to grant KMS access rights to EVS. If you have rights granting permission, grant the KMS access rights to EVS. If you do not have the permission, contact the user having the security administrator rights to grant the KMS access rights. For details, see section  [Who Can Use the Encryption Feature?](https://support.huaweicloud.com/en-us/ecs_faq/en-us_topic_0047272493.html)

        -   **Encrypted**: indicates that the EVS disk has been encrypted.
        -   **Create Xrole**: grants KMS access rights to EVS to obtain KMS keys. After the rights are granted, follow-up operations do not require granting rights again.
        -   **KMS Key Name**: specifies the name of the key used by the encrypted EVS disk. By default, the name is **evs/default**.
        -   **Xrole Name: EVSAccessKMS**: specifies that rights have been granted to EVS to obtain KMS keys for encrypting or decrypting EVS disks.
        -   **KMS Key ID**: specifies the ID of the key used by the encrypted data disk.


    For details about the disk types supported by the ECS, see section  [Storage](http://support.huaweicloud.com/en-us/productdesc-ecs/en-us_topic_0030828256.html). For more information about EVS disks, see _Elastic Volume Service User Guide_.

    >![](public_sys-resources/icon-note.gif) **NOTE:**   
    >If you detach the system disk purchased when you buy a yearly/monthly ECS and want to continue using it as a system disk, you can only attach it to the original ECS. If you want to use it as a data disk, you can attach it to any ECS.  
    >If you detach the non-shared data disk purchased when you buy a yearly/monthly ECS and want to attach it again, you can only attach it to the original ECS as a data disk.  
    >The data disk purchased when you buy a yearly/monthly ECS does not support separate renewal, unsubscription, automatic service renewal, conversion to pay-per-use payment, and release.  

11. Configure automatic backup.

    After automatic backup is enabled, the system automatically backs up the ECS based on the preset backup policy.

    1.  Select  **Enable**.
    2.  Configure  **Backup Policy**.

        In the drop-down list, select a backup policy. Alternatively, you can click  **Manage Backup Policy** and set the backup policy on the Cloud Server Backup Service \(CSBS\) page. If you have not created any backup policy but have selected **Enable**, the system will use the default backup policy, as shown in [Figure 1](#en-us_topic_0021831611_fig180165311591).

        **Figure  1**  Default backup policy<a name="en-us_topic_0021831611_fig180165311591"></a>  
        ![](figures/default-backup-policy.png "default-backup-policy")


    For more information about ECS backup, see  _Cloud Server Backup Service User Guide_.

12. Set network parameters, including  **VPC**, **Security Group**, **NIC**, and **EIP**.

    When you use VPC for the first time, the system automatically creates a VPC for you, including the security group and NIC.

    **Table  1**  Parameter descriptions

    <a name="en-us_topic_0021831611_table177515118613"></a>
    <table><thead align="left"><tr id="en-us_topic_0021831611_row77701911564"><th class="cellrowborder" valign="top" width="28.09%" id="mcps1.2.3.1.1"><p id="en-us_topic_0021831611_p1770911964"><a name="en-us_topic_0021831611_p1770911964"></a><a name="en-us_topic_0021831611_p1770911964"></a>Parameter</p>
    </th>
    <th class="cellrowborder" valign="top" width="71.91%" id="mcps1.2.3.1.2"><p id="en-us_topic_0021831611_p1077041115617"><a name="en-us_topic_0021831611_p1077041115617"></a><a name="en-us_topic_0021831611_p1077041115617"></a>Description</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="en-us_topic_0021831611_row1577116111867"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0021831611_p1077012116611"><a name="en-us_topic_0021831611_p1077012116611"></a><a name="en-us_topic_0021831611_p1077012116611"></a>VPC</p>
    </td>
    <td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0021831611_p077011113612"><a name="en-us_topic_0021831611_p077011113612"></a><a name="en-us_topic_0021831611_p077011113612"></a>Provides a network, including subnet and security group, for an ECS.</p>
    <p id="en-us_topic_0021831611_p197701511963"><a name="en-us_topic_0021831611_p197701511963"></a><a name="en-us_topic_0021831611_p197701511963"></a>You can select an existing VPC, or click <strong id="en-us_topic_0021831611_en-us_topic_0013859510_b842352706115630"><a name="en-us_topic_0021831611_en-us_topic_0013859510_b842352706115630"></a><a name="en-us_topic_0021831611_en-us_topic_0013859510_b842352706115630"></a>View VPC</strong> and create a desired one.</p>
    <p id="en-us_topic_0021831611_p177051116614"><a name="en-us_topic_0021831611_p177051116614"></a><a name="en-us_topic_0021831611_p177051116614"></a>For more information about VPC, see <em id="en-us_topic_0021831611_en-us_topic_0013859510_i84235269714525"><a name="en-us_topic_0021831611_en-us_topic_0013859510_i84235269714525"></a><a name="en-us_topic_0021831611_en-us_topic_0013859510_i84235269714525"></a>Virtual Private Cloud User Guide</em>.</p>
    <div class="note" id="en-us_topic_0021831611_note1277114114617"><a name="en-us_topic_0021831611_note1277114114617"></a><a name="en-us_topic_0021831611_note1277114114617"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="en-us_topic_0021831611_p19771121111619"><a name="en-us_topic_0021831611_p19771121111619"></a><a name="en-us_topic_0021831611_p19771121111619"></a>Ensure that DHCP is enabled in the VPC to which the ECS belongs.</p>
    </div></div>
    </td>
    </tr>
    <tr id="en-us_topic_0021831611_row577219111164"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0021831611_p1177111111069"><a name="en-us_topic_0021831611_p1177111111069"></a><a name="en-us_topic_0021831611_p1177111111069"></a>Security Group</p>
    </td>
    <td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0021831611_p1277141117616"><a name="en-us_topic_0021831611_p1277141117616"></a><a name="en-us_topic_0021831611_p1277141117616"></a>Controls ECS access within or between security groups by defining access rules. This enhances ECS security.</p>
    <p id="en-us_topic_0021831611_p27711711460"><a name="en-us_topic_0021831611_p27711711460"></a><a name="en-us_topic_0021831611_p27711711460"></a>When creating an ECS, you can select multiple (recommended not more than five) security groups. In such a case, the access rules of all the selected security groups apply on the ECS.</p>
    <p id="en-us_topic_0021831611_p167718112619"><a name="en-us_topic_0021831611_p167718112619"></a><a name="en-us_topic_0021831611_p167718112619"></a>Security group rules determine ECS access and usage. For instructions about how to configure a security group rule, see section <a href="http://support.huaweicloud.com/en-us/usermanual-vpc/en-us_topic_0030969470.html" target="_blank" rel="noopener noreferrer">Adding a Security Group Rule</a>. The following section describes common protocols and ports. Enable them as needed.</p>
    <a name="en-us_topic_0021831611_ul196112491217"></a><a name="en-us_topic_0021831611_ul196112491217"></a><ul id="en-us_topic_0021831611_ul196112491217"><li>Port 80: used to view web pages by default through HTTP.</li><li>Port 443: used to view web pages through HTTPS.</li><li>ICMP: pings ECSs to check their communication statuses.</li><li>Port 22: reserved for logging in to a Linux ECS using SSH.</li><li>Port 3389: reserved for logging in to a Windows ECS using SSH.</li></ul>
    <div class="note" id="en-us_topic_0021831611_note1977210113613"><a name="en-us_topic_0021831611_note1977210113613"></a><a name="en-us_topic_0021831611_note1977210113613"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="en-us_topic_0021831611_p37711211261"><a name="en-us_topic_0021831611_p37711211261"></a><a name="en-us_topic_0021831611_p37711211261"></a>Before initializing an ECS, ensure that the security group rule in the outbound direction meets the following requirements:</p>
    <a name="en-us_topic_0021831611_ul20772111565"></a><a name="en-us_topic_0021831611_ul20772111565"></a><ul id="en-us_topic_0021831611_ul20772111565"><li><strong id="en-us_topic_0021831611_b842352706151144"><a name="en-us_topic_0021831611_b842352706151144"></a><a name="en-us_topic_0021831611_b842352706151144"></a>Protocol</strong>:&nbsp;<strong id="en-us_topic_0021831611_b842352706103935"><a name="en-us_topic_0021831611_b842352706103935"></a><a name="en-us_topic_0021831611_b842352706103935"></a>TCP</strong></li><li><strong id="en-us_topic_0021831611_b842352706151147"><a name="en-us_topic_0021831611_b842352706151147"></a><a name="en-us_topic_0021831611_b842352706151147"></a>Port Range</strong>:&nbsp;<strong id="en-us_topic_0021831611_b842352706103938"><a name="en-us_topic_0021831611_b842352706103938"></a><a name="en-us_topic_0021831611_b842352706103938"></a>80</strong></li><li><strong id="en-us_topic_0021831611_b842352706151150"><a name="en-us_topic_0021831611_b842352706151150"></a><a name="en-us_topic_0021831611_b842352706151150"></a>Remote End</strong>:&nbsp;<strong id="en-us_topic_0021831611_b842352706103941"><a name="en-us_topic_0021831611_b842352706103941"></a><a name="en-us_topic_0021831611_b842352706103941"></a>169.254.0.0/16</strong></li></ul>
    <p id="en-us_topic_0021831611_p187721211266"><a name="en-us_topic_0021831611_p187721211266"></a><a name="en-us_topic_0021831611_p187721211266"></a>If you use the default security group rule in the outbound direction, the preceding requirements are met, and the ECS can be initialized. The default security group rule in the outbound direction is as follows:</p>
    <a name="en-us_topic_0021831611_ul1177210113610"></a><a name="en-us_topic_0021831611_ul1177210113610"></a><ul id="en-us_topic_0021831611_ul1177210113610"><li><strong id="en-us_topic_0021831611_b842352706151159"><a name="en-us_topic_0021831611_b842352706151159"></a><a name="en-us_topic_0021831611_b842352706151159"></a>Protocol</strong>:&nbsp;<strong id="en-us_topic_0021831611_b842352706103944"><a name="en-us_topic_0021831611_b842352706103944"></a><a name="en-us_topic_0021831611_b842352706103944"></a>ANY</strong></li><li><strong id="en-us_topic_0021831611_b84235270615122"><a name="en-us_topic_0021831611_b84235270615122"></a><a name="en-us_topic_0021831611_b84235270615122"></a>Port Range</strong>:&nbsp;<strong id="en-us_topic_0021831611_b842352706103947"><a name="en-us_topic_0021831611_b842352706103947"></a><a name="en-us_topic_0021831611_b842352706103947"></a>ANY</strong></li><li><strong id="en-us_topic_0021831611_b84235270615125"><a name="en-us_topic_0021831611_b84235270615125"></a><a name="en-us_topic_0021831611_b84235270615125"></a>Remote End</strong>:&nbsp;<strong id="en-us_topic_0021831611_b842352706103950"><a name="en-us_topic_0021831611_b842352706103950"></a><a name="en-us_topic_0021831611_b842352706103950"></a>0.0.0.0/16</strong></li></ul>
    </div></div>
    </td>
    </tr>
    <tr id="en-us_topic_0021831611_row137721911863"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0021831611_p1477216119610"><a name="en-us_topic_0021831611_p1477216119610"></a><a name="en-us_topic_0021831611_p1477216119610"></a>NIC</p>
    </td>
    <td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0021831611_p157811012104"><a name="en-us_topic_0021831611_p157811012104"></a><a name="en-us_topic_0021831611_p157811012104"></a>Includes primary and extension NICs. You can add multiple expansion NICs to an ECS and specify IP addresses for them (including primary NICs).</p>
    <div class="note" id="en-us_topic_0021831611_note12675133715182"><a name="en-us_topic_0021831611_note12675133715182"></a><a name="en-us_topic_0021831611_note12675133715182"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="en-us_topic_0021831611_p1276713295354"><a name="en-us_topic_0021831611_p1276713295354"></a><a name="en-us_topic_0021831611_p1276713295354"></a>If you specify an IP address when creating multiple ECSs in a batch:</p>
    <a name="en-us_topic_0021831611_ul976785115352"></a><a name="en-us_topic_0021831611_ul976785115352"></a><ul id="en-us_topic_0021831611_ul976785115352"><li>This IP address serves as the start IP address.</li><li>Ensure that the IP addresses required by the ECSs are within the subnet, consecutive, and available.</li><li>This subnet cannot duplicate a subnet with a specified start IP address.</li></ul>
    </div></div>
    <p id="en-us_topic_0021831611_p677214116612"><a name="en-us_topic_0021831611_p677214116612"></a><a name="en-us_topic_0021831611_p677214116612"></a><strong id="en-us_topic_0021831611_en-us_topic_0013859510_b842352706162014"><a name="en-us_topic_0021831611_en-us_topic_0013859510_b842352706162014"></a><a name="en-us_topic_0021831611_en-us_topic_0013859510_b842352706162014"></a>MTU Settings</strong>: optional</p>
    <p id="en-us_topic_0021831611_p9772151120611"><a name="en-us_topic_0021831611_p9772151120611"></a><a name="en-us_topic_0021831611_p9772151120611"></a>If your ECS is of M2, large-memory, H1, or D1 type, you can click <strong id="en-us_topic_0021831611_en-us_topic_0013859510_b13255495416231"><a name="en-us_topic_0021831611_en-us_topic_0013859510_b13255495416231"></a><a name="en-us_topic_0021831611_en-us_topic_0013859510_b13255495416231"></a>MTU Settings</strong> to configure the maximum transmission unit (MTU) for a to-be-added extension NIC for improving network performance.</p>
    <p id="en-us_topic_0021831611_p37723110610"><a name="en-us_topic_0021831611_p37723110610"></a><a name="en-us_topic_0021831611_p37723110610"></a>An MTU can only be a number, ranging from 1280 to 8888.</p>
    </td>
    </tr>
    <tr id="en-us_topic_0021831611_row197745111616"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0021831611_p18772911367"><a name="en-us_topic_0021831611_p18772911367"></a><a name="en-us_topic_0021831611_p18772911367"></a>EIP</p>
    </td>
    <td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0021831611_p1177313116612"><a name="en-us_topic_0021831611_p1177313116612"></a><a name="en-us_topic_0021831611_p1177313116612"></a>A static public IP address bound to an ECS in a VPC. Using the EIP, the ECS provides services externally.</p>
    <p id="en-us_topic_0021831611_p77731111963"><a name="en-us_topic_0021831611_p77731111963"></a><a name="en-us_topic_0021831611_p77731111963"></a>The following options are provided:</p>
    <a name="en-us_topic_0021831611_ul1877310112619"></a><a name="en-us_topic_0021831611_ul1877310112619"></a><ul id="en-us_topic_0021831611_ul1877310112619"><li><strong id="en-us_topic_0021831611_b53157916203523"><a name="en-us_topic_0021831611_b53157916203523"></a><a name="en-us_topic_0021831611_b53157916203523"></a>Do not use</strong><p id="en-us_topic_0021831611_p53893496203526"><a name="en-us_topic_0021831611_p53893496203526"></a><a name="en-us_topic_0021831611_p53893496203526"></a>Without an EIP, the ECS cannot access the Internet and is used only in the private network or cluster.</p>
    </li><li><strong id="en-us_topic_0021831611_b38711502203537"><a name="en-us_topic_0021831611_b38711502203537"></a><a name="en-us_topic_0021831611_b38711502203537"></a>Automatically assign</strong><p id="en-us_topic_0021831611_p35521867203540"><a name="en-us_topic_0021831611_p35521867203540"></a><a name="en-us_topic_0021831611_p35521867203540"></a>The system automatically assigns an EIP for the ECS. The EIP provides exclusive bandwidth that is configurable.</p>
    </li><li><strong id="en-us_topic_0021831611_b46736267203554"><a name="en-us_topic_0021831611_b46736267203554"></a><a name="en-us_topic_0021831611_b46736267203554"></a>Specify</strong><p id="en-us_topic_0021831611_p54115073203557"><a name="en-us_topic_0021831611_p54115073203557"></a><a name="en-us_topic_0021831611_p54115073203557"></a>An existing EIP is assigned for the ECS. When using an existing EIP, you cannot create ECSs in batches.</p>
    </li></ul>
    </td>
    </tr>
    <tr id="en-us_topic_0021831611_row57741211062"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0021831611_p17774111066"><a name="en-us_topic_0021831611_p17774111066"></a><a name="en-us_topic_0021831611_p17774111066"></a>Specifications</p>
    </td>
    <td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.3.1.2 "><a name="en-us_topic_0021831611_ul818114761516"></a><a name="en-us_topic_0021831611_ul818114761516"></a><ul id="en-us_topic_0021831611_ul818114761516"><li>When changes occur on a network using static BGP, network configurations cannot be promptly adjusted to ensure optimal user experience.</li><li>When changes occur on a network using dynamic BGP, network configurations can be promptly adjusted using the specified routing protocol, ensuring network stability and optimal user experience.</li></ul>
    </td>
    </tr>
    <tr id="en-us_topic_0021831611_row877412111069"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0021831611_p1077411111611"><a name="en-us_topic_0021831611_p1077411111611"></a><a name="en-us_topic_0021831611_p1077411111611"></a>Bandwidth Type</p>
    </td>
    <td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0021831611_p7774111560"><a name="en-us_topic_0021831611_p7774111560"></a><a name="en-us_topic_0021831611_p7774111560"></a>This parameter is mandatory if <strong id="en-us_topic_0021831611_b84235270694054"><a name="en-us_topic_0021831611_b84235270694054"></a><a name="en-us_topic_0021831611_b84235270694054"></a>EIP</strong>&nbsp;is set to&nbsp;<strong id="en-us_topic_0021831611_b84235270694057"><a name="en-us_topic_0021831611_b84235270694057"></a><a name="en-us_topic_0021831611_b84235270694057"></a>Automatically assign</strong>.</p>
    <a name="en-us_topic_0021831611_ul14774111113611"></a><a name="en-us_topic_0021831611_ul14774111113611"></a><ul id="en-us_topic_0021831611_ul14774111113611"><li><strong id="en-us_topic_0021831611_b842352706164039"><a name="en-us_topic_0021831611_b842352706164039"></a><a name="en-us_topic_0021831611_b842352706164039"></a>Exclusive</strong>: The bandwidth can be used by only one EIP.</li><li><strong id="en-us_topic_0021831611_b842352706212221"><a name="en-us_topic_0021831611_b842352706212221"></a><a name="en-us_topic_0021831611_b842352706212221"></a>Shared</strong>: The bandwidth can be used by multiple EIPs.<div class="note" id="en-us_topic_0021831611_note1377431117612"><a name="en-us_topic_0021831611_note1377431117612"></a><a name="en-us_topic_0021831611_note1377431117612"></a><span class="notetitle"> NOTE: </span><div class="notebody"><a name="en-us_topic_0021831611_ul1577411113612"></a><a name="en-us_topic_0021831611_ul1577411113612"></a><ul id="en-us_topic_0021831611_ul1577411113612"><li>A bandwidth can be shared between limited number of EIPs. If the number of EIPs cannot meet service requirement, switch to a higher shared bandwidth or apply to expand the EIP quota of the existing bandwidth.</li><li>EIPs that are charged yearly/monthly do not support shared bandwidths.</li><li>When a shared bandwidth that is charged yearly/monthly expires, the system automatically deletes the bandwidth and creates an exclusive bandwidth charged by traffic for the EIPs sharing the deleted bandwidth.</li></ul>
    </div></div>
    </li></ul>
    </td>
    </tr>
    <tr id="en-us_topic_0021831611_row8775611762"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0021831611_p16774161115610"><a name="en-us_topic_0021831611_p16774161115610"></a><a name="en-us_topic_0021831611_p16774161115610"></a>Billing Mode</p>
    </td>
    <td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0021831611_p177516119614"><a name="en-us_topic_0021831611_p177516119614"></a><a name="en-us_topic_0021831611_p177516119614"></a>This parameter is mandatory if <strong id="en-us_topic_0021831611_en-us_topic_0013859510_b84235270604234"><a name="en-us_topic_0021831611_en-us_topic_0013859510_b84235270604234"></a><a name="en-us_topic_0021831611_en-us_topic_0013859510_b84235270604234"></a>EIP</strong>&nbsp;is set to&nbsp;<strong id="en-us_topic_0021831611_en-us_topic_0013859510_b84235270604238"><a name="en-us_topic_0021831611_en-us_topic_0013859510_b84235270604238"></a><a name="en-us_topic_0021831611_en-us_topic_0013859510_b84235270604238"></a>Automatically assign</strong>.</p>
    <p id="en-us_topic_0021831611_p1377520111868"><a name="en-us_topic_0021831611_p1377520111868"></a><a name="en-us_topic_0021831611_p1377520111868"></a>It indicates the bandwidth billing mode of the purchased EIP, which includes the following options:</p>
    <a name="en-us_topic_0021831611_ul47753111965"></a><a name="en-us_topic_0021831611_ul47753111965"></a><ul id="en-us_topic_0021831611_ul47753111965"><li><strong id="en-us_topic_0021831611_en-us_topic_0013859510_b84235270694336"><a name="en-us_topic_0021831611_en-us_topic_0013859510_b84235270694336"></a><a name="en-us_topic_0021831611_en-us_topic_0013859510_b84235270694336"></a>Bandwidth</strong>: You are charged by the purchased bandwidth.</li><li><strong id="en-us_topic_0021831611_en-us_topic_0013859510_b8423527069456"><a name="en-us_topic_0021831611_en-us_topic_0013859510_b8423527069456"></a><a name="en-us_topic_0021831611_en-us_topic_0013859510_b8423527069456"></a>Traffic</strong>: You are charged based on the actual traffic you have used.</li></ul>
    </td>
    </tr>
    </tbody>
    </table>

13. Set  **Login Mode**.

    **Key pair** is recommended because it features higher security than **Password**. If you select **Password**, ensure that the password meets complexity requirements listed in [Table 2](#en-us_topic_0021831611_table18635520143711)  to prevent malicious attacks.

    -   Key pair

        A key pair is used for ECS login authentication. You can select an existing key pair, or click  **View Key Pair**  and create a desired one.

        >![](public_sys-resources/icon-note.gif) **NOTE:**   
        >If you use an existing key pair, make sure that you have saved the key file locally. Otherwise, logging in to the ECS will fail.  

    -   Password

        A username and its initial password are used for ECS login authentication.

        The initial password of user  **root** is used for authentication in Linux, while that of user **Administrator** is used for authentication in Windows. The passwords must meet the requirements described in [Table 2](#en-us_topic_0021831611_table18635520143711).

        **Table  2**  Password complexity requirements

        <a name="en-us_topic_0021831611_table18635520143711"></a>
        <table><thead align="left"><tr id="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_row925712618958"><th class="cellrowborder" valign="top" width="18%" id="mcps1.2.4.1.1"><p id="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p1162970218958"><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p1162970218958"></a><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p1162970218958"></a>Parameter</p>
        </th>
        <th class="cellrowborder" valign="top" width="65%" id="mcps1.2.4.1.2"><p id="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p248177818958"><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p248177818958"></a><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p248177818958"></a>Requirement</p>
        </th>
        <th class="cellrowborder" valign="top" width="17%" id="mcps1.2.4.1.3"><p id="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p6680635518958"><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p6680635518958"></a><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p6680635518958"></a>Example Value</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_row4260571318958"><td class="cellrowborder" valign="top" width="18%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p2851073918958"><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p2851073918958"></a><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p2851073918958"></a>Password</p>
        </td>
        <td class="cellrowborder" valign="top" width="65%" headers="mcps1.2.4.1.2 "><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_ul5961106018958"></a><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_ul5961106018958"></a><ul id="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_ul5961106018958"><li>Consists of 8 characters to 26 characters.</li><li>Contains at least three of the following character types:<a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_ul24583583181022"></a><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_ul24583583181022"></a><ul id="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_ul24583583181022"><li>Uppercase letters</li><li>Lowercase letters</li><li>Numerals</li><li>Special characters:<p id="en-us_topic_0021831611_en-us_topic_0035643949_p8770135812533"><a name="en-us_topic_0021831611_en-us_topic_0035643949_p8770135812533"></a><a name="en-us_topic_0021831611_en-us_topic_0035643949_p8770135812533"></a>$!@%-_=+[</p>
        <p id="en-us_topic_0021831611_en-us_topic_0035643949_p4326629155311"><a name="en-us_topic_0021831611_en-us_topic_0035643949_p4326629155311"></a><a name="en-us_topic_0021831611_en-us_topic_0035643949_p4326629155311"></a>]:./^,{}?</p>
        </li></ul>
        </li><li>Cannot contain the username or the username in reverse.</li><li>Cannot contain more than two characters in the same sequence as they appear in the username. (This requirement applies only to Windows ECSs.)</li></ul>
        </td>
        <td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p6481855218958"><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p6481855218958"></a><a name="en-us_topic_0021831611_en-us_topic_0035643949_en-us_topic_0021426802_p6481855218958"></a>Test12!@</p>
        </td>
        </tr>
        </tbody>
        </table>

        >![](public_sys-resources/icon-note.gif) **NOTE:**   
        >The system does not automatically change the password for logging in to an ECS on a regular basis. It is recommended that you change your password regularly for security.  

