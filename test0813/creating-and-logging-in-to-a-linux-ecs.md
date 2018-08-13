# Creating and Logging In to a Linux ECS<a name="EN-US_TOPIC_0092494193"></a>

## Scenarios<a name="section119581947203612"></a>

ECSs are more cost-effective than physical servers. Within minutes, you can obtain ECS resources from the public cloud. ECS resources are flexible and on-demand. This section describes how to create an ECS.

[Step 1: Create an ECS](#section761474661113)

[Step 2: Log In to the ECS](#section105801931112415)

## Step 1: Create an ECS<a name="section761474661113"></a>

1.  Log in to the management console.
2.  Click ![](figures/en-us_image_0070749810.png) in the upper left corner and select the desired region and project.
3.  Under **Computing**, click **Elastic Cloud Server**.
4.  Click **Create ECS**.

    The ECS creation page is displayed.

    > ![](public_sys-resources/icon-note.gif) **NOTE:** 

    > SAP High-Performance Analytic Appliance \(HANA\) is a high-performance real-time data computing platform based on memory computing technologies. The public cloud provides high-performance IaaS services that comply with SAP HANA requirements. These services include applying for HANA ECSs and public IP addresses as well as installing and configuring SAP HANA. Such services facilitate applications on the public cloud platform of resources required by SAP HANA, improving the efficiency of user operations, reducing operation costs, and enhancing user experience.

    > HANA ECSs are dedicated for SAP HANA. If you have deployed SAP HANA on cloud servers, you can create HANA ECSs.

    > For more information about HANA ECS application scenarios and creation methods, see *SAP HANA User Guide*.

5.  Confirm the region.

    If the region is incorrect, click ![](figures/en-us_image_0092504858.png) in the upper left corner of the page for correction.

6.  Select an AZ.

    An AZ is a physical region where power and networks are physically isolated. AZs in the same region can communicate with each other over an intranet.

    -   To enhance application availability, create ECSs in different AZs.
    -   To shorten network latency, create ECSs in the same AZ.
7.  Set **Specifications**.

    The public cloud provides various ECS types for different application scenarios. You can view released ECS types and specifications in the list. Alternatively, you can enter a flavor name \(such as **c3**\) to search for the desired specification.

    **Latest generations** show the types and specifications of newly released ECSs, and **All generations** show the types and specifications of all ECSs provided by the public cloud.

    > ![](public_sys-resources/icon-note.gif) **NOTE:** 

    > -   Before selecting an ECS type, learn the introduction and notes on each type of ECSs. For details, see section [Instances and Application Scenarios](instances-and-application-scenarios.md).
    > -   **Local Disk**: specifies the local storage of the physical host where the ECS is deployed. Only Hard Disk Driver \(HDD\) disks are supported. If the ECS of the selected type \(such as **Disk-intensive**\) uses local disks, the system automatically attaches the local disks to the ECS and displays the information of the local disks.

        For example, if **Local Disk** is **3 x 1800 GB \(HDD\)**, three HDDs are attached to the ECS and the capacity of each HDD is 1800 GB.

8.  Set **DeH**.

    DeH refers to physical host resources dedicated for a specified user. You can deploy ECSs on DeHs for better isolation, security, and performance of your ECSs. You can continue to use your existing server software licenses of ECSs on DeHs to reduce costs.

    If you are required to use DeH resources, click **Configure now**. Otherwise, click **Do not configure**. For more details, see *Dedicated Host User Guide*.

9.  Click **Image**.

    -   Public image

        A public image is a standard, widely used image. It contains an OS and preinstalled public applications and is available to all users. You can configure the applications or software in the public image as needed.

        For more information about public images, see [Public Images Introduction](https://docs.otc.t-systems.com/ims_dld/index.html).

    -   Private image

        A private image is an image available only to the user who creates it. It contains an OS, preinstalled public applications, and the user's private applications. Using a private image to create ECSs removes the need to configure multiple ECSs repeatedly.

        You can also select an encrypted image. For details, see *Image Management Service User Guide*.

        If you have used a CSBS backup to create a private image \(full-ECS image\), you can use the full-ECS image. However, the EVS disk in the image does not support disk creation using a data disk image, and disk attributes \(such as SCSI/VBD and data encryption\) cannot be modified. For more details about how to use CSBS backups to create images, see section "Using Backups to Create Images" in *Cloud Server Backup Service User Guide* and section "Creating a Full-ECS Image Using a CSBS Backup" in *Image Management Service User Guide*.

    -   Shared image

        A shared image is a private image shared by another user.

    -   Marketplace image

        The Marketplace is a store where you can purchase third-party images that have the OS, application environment, and software pre-installed. You can use the images to deploy websites and application development environments with a few clicks, and no additional configuration operation is required.

        If you use a Marketplace image, after you click **Marketplace Image**, the system displays Marketplace images for you to select. For example, if the image product is **name1 \(test\_001\)**, **name1** is the image name, and **test\_001** is the product name. You can search for your desired Marketplace image by image name or product name. Alternatively, you can click the image name to view more information about the product. For more information about Marketplace images, see [Marketplace User Guide \(for Tenants\)](https://docs.otc.t-systems.com/en-us/usermanual/marketplace/en-us_topic_0056831005.html).

    > ![](public_sys-resources/icon-note.gif) **NOTE:** 

    > To obtain the image that is used for creating an FPGA-accelerated ECS, click [here](https://docs.otc.t-systems.com/en-us/public/learnmore.html) and contact customer service.

10. \(Optional\) Set **License Type**.

    **License Type** specifies a license type for using an OS or software on the public cloud platform. If the image you selected is free of charge, this parameter is unavailable. If the image you selected is charged, this parameter is available.

    -   Use license from the system

        Allows you to use the license provided by the public cloud platform. Obtaining the authorization of such a license is charged.

    -   Bring your own license \(BYOL\)

        Allows you to use your existing OS license. In such a case, you do not need to apply for a license again.

    For more details, see section [License Type](license-type.md).

11. Set **Disk**.

    A disk can be a system disk or a data disk. You can create multiple data disks for an ECS and customize their disk sizes. The system disk size of a P1 or P2 ECS must be greater than or equal to 15 GB. It is recommended that the system disk size be greater than 40 GB.

    -   System Disk

        If the image based on which an ECS is created is not encrypted, the system disk of the ECS is not encrypted. In addition, **Unencrypted** is displayed for the system disk on the page. If the image based on which an ECS is created is encrypted, the system disk of the ECS is automatically encrypted. For details, see section [\(Optional\) Encryption-related parameters](#en-us_topic_0021831611_li126651425205814).

    -   Data Disk

        You can create multiple data disks for an ECS and configure sharing and encryption for each data disk.

        -   **SCSI**: indicates that the device type of the data disk is SCSI. For more information about SCSI disks and the ECSs that can be attached with SCSI disks, see section [Storage](storage.md).
        -   **Share**: indicates that the EVS disk is shared. Such an EVS disk can be attached to multiple ECSs.
        -   **Encryption**: indicates that the data disk is encrypted. For details, see section [\(Optional\) Encryption-related parameters](#en-us_topic_0021831611_li126651425205814).
        -   **Create Disk from Data Disk Image**: If you have created a data image on the **Image Management Service** page, when using a Windows or Linux image to create an ECS, you can use a data disk image to create a disk for the ECS.

            Click **Create Disk from Data Disk Image**. In the dialog box that is displayed, select your data image.

            > ![](public_sys-resources/icon-note.gif) **NOTE:** 

            > -   One data disk image can be used only for one data disk.
            > -   When you use a data disk image to create a disk, **SCSI**, **Share**, and **Encryption** are unavailable.
            > -   For instructions about how create a data image, see *Image Management Service User Guide*.
    -   \(Optional\) Encryption-related parameters

        To enable encryption, click **Create Xrole** to grant KMS access rights to EVS. If you have rights granting permission, grant the KMS access rights to EVS. If you do not have the permission, contact the user having the security administrator rights to grant the KMS access rights. For details, see section [Who Can Use the Encryption Feature?](who-can-use-the-encryption-feature.md)

        -   **Encrypted**: indicates that the EVS disk has been encrypted.
        -   **Create Xrole**: grants KMS access rights to EVS to obtain KMS keys. After the rights are granted, follow-up operations do not require granting rights again.
        -   **KMS Key Name**: specifies the name of the key used by the encrypted EVS disk. By default, the name is **evs/default**.
        -   **Xrole Name: EVSAccessKMS**: specifies that rights have been granted to EVS to obtain KMS keys for encrypting or decrypting EVS disks.
        -   **KMS Key ID**: specifies the ID of the key used by the encrypted data disk.
    For details about the disk types supported by the ECS, see section [Storage](storage.md). For more information about EVS disks, see *Elastic Volume Service User Guide*.

12. Set network parameters, including **VPC**, **Security Group**, **NIC**, and **EIP**.

    When you use VPC for the first time, the system automatically creates a VPC for you, including the security group and NIC.**Table 1** Parameter descriptions

    <a name="en-us_topic_0021831611_table177515118613"></a><table><thead align="left"><tr id="en-us_topic_0021831611_row77701911564"><th class="cellrowborder" valign="top" width="28.09%" id="mcps1.2.3.1.1"><p id="en-us_topic_0021831611_p1770911964"><a name="en-us_topic_0021831611_p1770911964"></a><a name="en-us_topic_0021831611_p1770911964"></a>Parameter</p>
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
<div class="note" id="en-us_topic_0021831611_note1277114114617"><a name="en-us_topic_0021831611_note1277114114617"></a><a name="en-us_topic_0021831611_note1277114114617"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="en-us_topic_0021831611_p19771121111619"><a name="en-us_topic_0021831611_p19771121111619"></a><a name="en-us_topic_0021831611_p19771121111619"></a>DHCP must be enabled in the VPC to which the ECS belongs.</p>
</div></div>
</td>
</tr>
<tr id="en-us_topic_0021831611_row577219111164"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0021831611_p1177111111069"><a name="en-us_topic_0021831611_p1177111111069"></a><a name="en-us_topic_0021831611_p1177111111069"></a>Security Group</p>
</td>
<td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0021831611_p1277141117616"><a name="en-us_topic_0021831611_p1277141117616"></a><a name="en-us_topic_0021831611_p1277141117616"></a>Controls instance access within or between security groups by defining access rules. This enhances instance security.</p>
<p id="en-us_topic_0021831611_p27711711460"><a name="en-us_topic_0021831611_p27711711460"></a><a name="en-us_topic_0021831611_p27711711460"></a>When creating an ECS, you can select multiple (recommended not more than five) security groups. In such a case, the access rules of all the selected security groups apply on the ECS.</p>
<div class="note" id="en-us_topic_0021831611_note1977210113613"><a name="en-us_topic_0021831611_note1977210113613"></a><a name="en-us_topic_0021831611_note1977210113613"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="en-us_topic_0021831611_p37711211261"><a name="en-us_topic_0021831611_p37711211261"></a><a name="en-us_topic_0021831611_p37711211261"></a>Before initializing an ECS, ensure that the security group rule in the outbound direction meets the following requirements:</p>
<a name="en-us_topic_0021831611_ul20772111565"></a><a name="en-us_topic_0021831611_ul20772111565"></a><ul id="en-us_topic_0021831611_ul20772111565"><li id="en-us_topic_0021831611_li207711811763"><a name="en-us_topic_0021831611_li207711811763"></a><a name="en-us_topic_0021831611_li207711811763"></a><strong id="en-us_topic_0021831611_b842352706151144"><a name="en-us_topic_0021831611_b842352706151144"></a><a name="en-us_topic_0021831611_b842352706151144"></a>Protocol</strong>:&nbsp;<strong id="en-us_topic_0021831611_b842352706103935"><a name="en-us_topic_0021831611_b842352706103935"></a><a name="en-us_topic_0021831611_b842352706103935"></a>TCP</strong></li><li id="en-us_topic_0021831611_li18771011361"><a name="en-us_topic_0021831611_li18771011361"></a><a name="en-us_topic_0021831611_li18771011361"></a><strong id="en-us_topic_0021831611_b842352706151147"><a name="en-us_topic_0021831611_b842352706151147"></a><a name="en-us_topic_0021831611_b842352706151147"></a>Port Range</strong>:&nbsp;<strong id="en-us_topic_0021831611_b842352706103938"><a name="en-us_topic_0021831611_b842352706103938"></a><a name="en-us_topic_0021831611_b842352706103938"></a>80</strong></li><li id="en-us_topic_0021831611_li1777281119612"><a name="en-us_topic_0021831611_li1777281119612"></a><a name="en-us_topic_0021831611_li1777281119612"></a><strong id="en-us_topic_0021831611_b842352706151150"><a name="en-us_topic_0021831611_b842352706151150"></a><a name="en-us_topic_0021831611_b842352706151150"></a>Remote End</strong>:&nbsp;<strong id="en-us_topic_0021831611_b842352706103941"><a name="en-us_topic_0021831611_b842352706103941"></a><a name="en-us_topic_0021831611_b842352706103941"></a>169.254.0.0/16</strong></li></ul>
<p id="en-us_topic_0021831611_p187721211266"><a name="en-us_topic_0021831611_p187721211266"></a><a name="en-us_topic_0021831611_p187721211266"></a>If you use the default security group rule in the outbound direction, the preceding requirements are met, and the ECS can be initialized. The default security group rule in the outbound direction is as follows:</p>
<a name="en-us_topic_0021831611_ul1177210113610"></a><a name="en-us_topic_0021831611_ul1177210113610"></a><ul id="en-us_topic_0021831611_ul1177210113610"><li id="en-us_topic_0021831611_li977215111663"><a name="en-us_topic_0021831611_li977215111663"></a><a name="en-us_topic_0021831611_li977215111663"></a><strong id="en-us_topic_0021831611_b842352706151159"><a name="en-us_topic_0021831611_b842352706151159"></a><a name="en-us_topic_0021831611_b842352706151159"></a>Protocol</strong>:&nbsp;<strong id="en-us_topic_0021831611_b842352706103944"><a name="en-us_topic_0021831611_b842352706103944"></a><a name="en-us_topic_0021831611_b842352706103944"></a>ANY</strong></li><li id="en-us_topic_0021831611_li207721711961"><a name="en-us_topic_0021831611_li207721711961"></a><a name="en-us_topic_0021831611_li207721711961"></a><strong id="en-us_topic_0021831611_b84235270615122"><a name="en-us_topic_0021831611_b84235270615122"></a><a name="en-us_topic_0021831611_b84235270615122"></a>Port Range</strong>:&nbsp;<strong id="en-us_topic_0021831611_b842352706103947"><a name="en-us_topic_0021831611_b842352706103947"></a><a name="en-us_topic_0021831611_b842352706103947"></a>ANY</strong></li><li id="en-us_topic_0021831611_li1277281111619"><a name="en-us_topic_0021831611_li1277281111619"></a><a name="en-us_topic_0021831611_li1277281111619"></a><strong id="en-us_topic_0021831611_b84235270615125"><a name="en-us_topic_0021831611_b84235270615125"></a><a name="en-us_topic_0021831611_b84235270615125"></a>Remote End</strong>:&nbsp;<strong id="en-us_topic_0021831611_b842352706103950"><a name="en-us_topic_0021831611_b842352706103950"></a><a name="en-us_topic_0021831611_b842352706103950"></a>0.0.0.0/16</strong></li></ul>
</div></div>
</td>
</tr>
<tr id="en-us_topic_0021831611_row137721911863"><td class="cellrowborder" valign="top" width="28.09%" headers="mcps1.2.3.1.1 "><p id="en-us_topic_0021831611_p1477216119610"><a name="en-us_topic_0021831611_p1477216119610"></a><a name="en-us_topic_0021831611_p1477216119610"></a>NIC</p>
</td>
<td class="cellrowborder" valign="top" width="71.91%" headers="mcps1.2.3.1.2 "><p id="en-us_topic_0021831611_p157811012104"><a name="en-us_topic_0021831611_p157811012104"></a><a name="en-us_topic_0021831611_p157811012104"></a>Includes primary and extension NICs. You can add multiple expansion NICs to an ECS and specify IP addresses for them (including primary NICs).</p>
<div class="note" id="en-us_topic_0021831611_note12675133715182"><a name="en-us_topic_0021831611_note12675133715182"></a><a name="en-us_topic_0021831611_note12675133715182"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="en-us_topic_0021831611_p1276713295354"><a name="en-us_topic_0021831611_p1276713295354"></a><a name="en-us_topic_0021831611_p1276713295354"></a>If you specify an IP address when creating multiple ECSs in a batch:</p>
<a name="en-us_topic_0021831611_ul976785115352"></a><a name="en-us_topic_0021831611_ul976785115352"></a><ul id="en-us_topic_0021831611_ul976785115352"><li id="en-us_topic_0021831611_li16767165113354"><a name="en-us_topic_0021831611_li16767165113354"></a><a name="en-us_topic_0021831611_li16767165113354"></a>This IP address serves as the start IP address.</li><li id="en-us_topic_0021831611_li197678512354"><a name="en-us_topic_0021831611_li197678512354"></a><a name="en-us_topic_0021831611_li197678512354"></a>Ensure that the IP addresses required by the ECSs are within the subnet, consecutive, and available.</li><li id="en-us_topic_0021831611_li3767251123519"><a name="en-us_topic_0021831611_li3767251123519"></a><a name="en-us_topic_0021831611_li3767251123519"></a>This subnet cannot duplicate a subnet with a specified start IP address.</li></ul>
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
<a name="en-us_topic_0021831611_ul1877310112619"></a><a name="en-us_topic_0021831611_ul1877310112619"></a><ul id="en-us_topic_0021831611_ul1877310112619"><li id="en-us_topic_0021831611_li147738113620"><a name="en-us_topic_0021831611_li147738113620"></a><a name="en-us_topic_0021831611_li147738113620"></a><strong id="en-us_topic_0021831611_b53157916203523"><a name="en-us_topic_0021831611_b53157916203523"></a><a name="en-us_topic_0021831611_b53157916203523"></a>Do not use</strong><p id="en-us_topic_0021831611_p53893496203526"><a name="en-us_topic_0021831611_p53893496203526"></a><a name="en-us_topic_0021831611_p53893496203526"></a>Without an EIP, the ECS cannot access the Internet and is used only in the private network or cluster.</p>
</li><li id="en-us_topic_0021831611_li12773111112611"><a name="en-us_topic_0021831611_li12773111112611"></a><a name="en-us_topic_0021831611_li12773111112611"></a><strong id="en-us_topic_0021831611_b38711502203537"><a name="en-us_topic_0021831611_b38711502203537"></a><a name="en-us_topic_0021831611_b38711502203537"></a>Automatically assign</strong><p id="en-us_topic_0021831611_p35521867203540"><a name="en-us_topic_0021831611_p35521867203540"></a><a name="en-us_topic_0021831611_p35521867203540"></a>The system automatically assigns an EIP for the ECS. The EIP provides exclusive bandwidth that is configurable.</p>
</li><li id="en-us_topic_0021831611_li1677314113617"><a name="en-us_topic_0021831611_li1677314113617"></a><a name="en-us_topic_0021831611_li1677314113617"></a><strong id="en-us_topic_0021831611_b46736267203554"><a name="en-us_topic_0021831611_b46736267203554"></a><a name="en-us_topic_0021831611_b46736267203554"></a>Specify</strong><p id="en-us_topic_0021831611_p54115073203557"><a name="en-us_topic_0021831611_p54115073203557"></a><a name="en-us_topic_0021831611_p54115073203557"></a>An existing EIP is assigned for the ECS. When using an existing EIP, you cannot create ECSs in batches.</p>
</li></ul>
</td>
</tr>
</tbody>
</table>

13. Set **Login Mode**.

    The login mode is **Key pair**, which allows you to use a key pair for login authentication. You can select an existing key pair, or click **View Key Pair** and create a desired one.

    > ![](public_sys-resources/icon-note.gif) **NOTE:** 

    > If you use an existing key pair, make sure that you have saved the key file locally. Otherwise, logging in to the ECS will fail.

14. Configure **Auto Recovery**.

    Once a physical host accommodating ECSs breaks down, the ECSs with automatic recovery enabled automatically migrate to a functional host. This minimizes user service interruption. These ECSs will restart in this process. If automatic recovery is not enabled, the affected users must wait for the system administrator to recover ECSs when the physical host becomes faulty. For more information about automatic recovery, see section [Automatically Recovering ECSs](automatically-recovering-ecss.md).

    > ![](public_sys-resources/icon-note.gif) **NOTE:** 

    > -   KVM ECSs do not support automatic recovery.
    > -   XEN ECSs do not support automatic recovery if one of the following resources is used:
        -   Local disk
        -   Passthrough FPGA card
        -   Passthrough InfiniBand NIC
15. Configure **Advanced Settings**.

    To use functions listed in **Advanced Settings**, click **Configure now**. Otherwise, click **Do not configure**.

    -   File Injection

        Enables the ECS to automatically inject a script file or other files into a specified directory on an ECS when you create the ECS. This configuration is optional.

        For example, if you activate user **root** permission using script file injection, you can log in to the ECS as user **root**.

        For details about file injection, see section [Injecting Files into ECSs](injecting-files-into-ecss.md).

    -   User Data Injection

        Enables the ECS to automatically inject user data when the ECS starts for the first time. This configuration is optional.

        For example, if you activate user **root** permission using user data injection, you can log in to the ECS as user **root**.

        For detailed operations, see section [Injecting User Data into ECSs](injecting-user-data-into-ecss.md).

    -   ECS Group

        An ECS group applies the anti-affinity policy to the ECSs in it so that the ECSs can be distributed on different hosts. This configuration is optional. For instructions about how to create an ECS group, see section [Creating an ECS Group](creating-an-ecs-group.md).

    -   Tag

        Tags an ECS, facilitating ECS identification and management. This configuration is optional. You can add up to 10 tags to an ECS.

        > ![](public_sys-resources/icon-note.gif) **NOTE:** 

        > Tags added during ECS creation will also be added to the created EIP and EVS disks \(including the system disk and data disks\) of the ECS. If the ECS uses an existing EIP, the tags will not be added to the EIP.

        > After creating the ECS, you can view the tags on the pages providing details about the ECS, EIP, and EVS disks.

        For detailed operations, see section [Tags](tags.md).

    -   Agency Name

        This configuration is optional. An agency is created by the tenant administrator in IAM and provides a temporary credential for an ECS to access cloud services. If you have created an agency in IAM, you can select the agency name from the drop-down list and obtain specified operation permissions.

16. Set **ECS Name**.

    The name can be customized but must comply with the following naming rules: Can contain only letters, digits, underscores \(\_\), hyphens \(-\), and periods \(.\).

    If you want to create multiple ECSs at a time, the system automatically sequences these ECSs.

17. Configure the number of ECSs to be created.

    After the configuration, click **Price Calculator** to view the ECS configuration fee.

18. Click **Create Now**.
19. On the ECS specification confirmation page, confirm the ECS specifications and click **Submit**.

    After the ECS is created, you can view information about it on the **Elastic Cloud Server** page.


> ![](public_sys-resources/icon-note.gif) **NOTE:** 

> Creating an ECS takes several minutes. You can check the creation progress by viewing the ECS creation status. For details, see section [Viewing ECS Creation Statuses](viewing-ecs-creation-statuses.md).

## Step 2: Log In to the ECS<a name="section105801931112415"></a>

You can log in to a Linux ECS using either VNC or SSH key provided on the public cloud.

<a name="fig51588342172524"></a>
**Figure 1** Linux ECS login modes
![](figures/linux-ecs-login-modes.png "Linux ECS login modes")

1.  Log in to the management console.
2.  Under **Computing**, click **Elastic Cloud Server**.
3.  Select the ECS you want to log in to.
4.  Select a login method and log in to the ECS.
    -   VNC

        For details, see [Login Using VNC](login-using-vnc.md).

    -   SSH key

        When you log in to the ECS using the SSH key, you need to bind an EIP to the ECS.

        For details, see section [Login Using an SSH Key](login-using-an-ssh-key.md).


## Follow-up Procedure<a name="section255541813811"></a>

-   After an ECS with automatic recovery enabled is created, you can check whether this function has been enabled by viewing **Failed Tasks**. For details, see section [Viewing Failed Tasks](viewing-failed-tasks.md).
-   If you have added a data disk during ECS creation, you must initialize the data disk after logging in to the ECS.

    For details, see section [Initializing EVS Data Disks](initializing-evs-data-disks.md).

-   Certain ECSs require the installation of a driver after you log in to them. For details about available ECS types as well as their functions and usage, see section "Notes" in [Instances and Application Scenarios](instances-and-application-scenarios.md).

