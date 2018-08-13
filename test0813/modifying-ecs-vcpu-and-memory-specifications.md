# Modifying ECS vCPU and Memory Specifications<a name="EN-US_TOPIC_0013771092"></a>

## Scenarios<a name="en-us_topic_0013859511_section14602858172718"></a>

If the ECS specifications do not meet service requirements, you can modify the ECS specifications, including vCPUs and memory. Certain ECSs allow you to change their types when you modify their specifications.

Specifications can be modified between general-purpose \(S1, C1, C2, or M1\) and H1 ECSs and from XEN to KVM ECSs.

-   If you want to change a general-purpose ECS to an H1 ECS, manually configure the source ECS, install the required driver on it, and modify the specifications. For details, see section [Changing a General-Purpose ECS to an H1 ECS](changing-a-general-purpose-ecs-to-an-h1-ecs.md).
-   If you want to change an H1 ECS to a general-purpose ECS, perform the operations provided in this section.
-   Before changing a XEN ECS to a KVM ECS, manually install the required driver on the ECS. Otherwise, the ECS will be unavailable after the modification is performed. For example, starting the OS will fail.

    For details, see sections [Changing a XEN ECS to a KVM ECS \(Windows\)](changing-a-xen-ecs-to-a-kvm-ecs-(windows).md) and [Changing a XEN ECS to a KVM ECS \(Linux\)](changing-a-xen-ecs-to-a-kvm-ecs-(linux).md).

-   For instructions about how to modify the specifications of other ECSs, see this section.

> ![](public_sys-resources/icon-note.gif) **NOTE:** 

> -   To obtain the virtualization type of an ECS, see [Background](#section15710213610).
> -   Before changing XEN to KVM, make sure that the ECS has been correctly configured. Otherwise, the ECS will be unavailable after the modification is performed.

## Background<a name="section15710213610"></a>

To obtain the virtualization type of an ECS, perform the following operations:

1.  On the page providing details about the ECS, view the ECS specifications.

<a name="fig14561414141716"></a>    
    **Figure 1** Viewing ECS specifications
    ![](figures/viewing-ecs-specifications.png "Viewing ECS specifications")

2.  Check the specifications tables in section [Instances and Application Scenarios](instances-and-application-scenarios.md) for the virtualization type.

## Notes<a name="en-us_topic_0013859511_section57753505172833"></a>

-   If ECS specifications are downgraded, the ECS performance is deteriorated.
-   Certain ECSs do not support specifications modification currently. For details about available ECS types as well as their functions and usage, see section "Notes" in [Instances and Application Scenarios](instances-and-application-scenarios.md).

## Step 1: Modify Specifications<a name="section997143905215"></a>

The following section provides only general operations for modifying specifications. For instructions about how to change a general-purpose ECS to an H1 ECS, see section [Changing a General-Purpose ECS to an H1 ECS](changing-a-general-purpose-ecs-to-an-h1-ecs.md). For instructions about how to change a XEN ECS to a KVM ECS, see sections [Changing a XEN ECS to a KVM ECS \(Windows\)](changing-a-xen-ecs-to-a-kvm-ecs-(windows).md) and [Changing a XEN ECS to a KVM ECS \(Linux\)](changing-a-xen-ecs-to-a-kvm-ecs-(linux).md).

1.  Log in to the management console.
2.  Click ![](figures/en-us_image_0096401244.png) in the upper left corner and select the desired region and project.
3.  Under **Computing**, click **Elastic Cloud Server**.
4.  In the ECS list, view the status of the target ECS.

    If the ECS is not in **Stopped** state, click **More** in the **Operation** column and select **Stop**.

5.  Click **More** in the **Operation** column and select **Modify Specifications**.
6.  In the **Modify Specifications** dialog box, select the new ECS type, vCPU, and memory specifications.

<a name="fig873240105215"></a>    
    **Figure 2** Modifying vCPU and memory specifications
    ![](figures/modifying-vcpu-and-memory-specifications.png "Modifying vCPU and memory specifications")

7.  \(Optional\) Set **DeH**.

    If the ECS is created on a DeH, the system allows you to change the DeH.

    To do so, select the target DeH from the drop-down list. If no DeH is available in the drop-down list, remaining DeH resources are insufficient and cannot be used to create the ECS with specifications modified.

8.  \(Optional\) Select the check box.
    -   If a general-purpose ECS is changed to an H1 ECS, manually configure the ECS based on the instructions provided in section [Changing a General-Purpose ECS to an H1 ECS](changing-a-general-purpose-ecs-to-an-h1-ecs.md). After the configuration, select the check box and confirm the operation.
    -   If a XEN ECS is changed to a KVM ECS, manually configure the ECS based on the instructions provided in section [Changing a XEN ECS to a KVM ECS \(Windows\)](changing-a-xen-ecs-to-a-kvm-ecs-(windows).md) or [Changing a XEN ECS to a KVM ECS \(Linux\)](changing-a-xen-ecs-to-a-kvm-ecs-(linux).md). After the configuration, select the check box and confirm the operation.
9.  Click **OK**.
10. On the **Modify ECS Specification** page, confirm the modified vCPU and memory specifications and click **Submit**.
11. Check whether the specifications have been modified.

    After modifying the specifications, you can check whether the specifications have been modified in **Error**.

    1.  Check whether **Error** is displayed on the management console. For details, see section [Viewing Failed Tasks](viewing-failed-tasks.md).
        -   If yes, go to step [11.b](#li6253192246).
        -   If no, the specifications have been modified.
    2.  Click the error and check whether the target specifications modification task is included by ECS name/ID, operation time, or task.
        -   If yes, the specifications modification failed. See section [Follow-up Procedure](#section9461027528) for failure causes.
        -   If no, the specifications have been modified.

## Step 2: Check Disk Attachment<a name="section88041642132813"></a>

After specifications are modified, disk attachment may fail. Therefore, check disk attachment after specifications modification. If disks are properly attached, the specifications modification is successful.

-   Windows ECSs
    1.  Check whether the number of disks displayed on the **Computer** page after specifications modification is the same as that before specifications modifications.

        -   If yes, the disks are properly attached. No further action is required.
        -   If no, an error has occurred in disk attachment. In such a case, go to [2](#en-us_topic_0100593628_li1476865113179).
        An example is provided as follows:

        Before the specifications modification, there is one system disk and two data disks attached to an ECS running Windows Server 2008.

<a name="en-us_topic_0100593628_fig21898319615"></a>        
        **Figure 3** Disk attachment before specifications modification
        ![](figures/disk-attachment-before-specifications-modification.png "Disk attachment before specifications modification")

        After the specifications are modified, check disk attachment.

<a name="en-us_topic_0100593628_fig577522321219"></a>        
        **Figure 4** Disk attachment after specifications modification
        ![](figures/disk-attachment-after-specifications-modification.png "Disk attachment after specifications modification")

        Only one system disk is displayed. Data disks failed to attach after the specifications modification.

    2.  Set the affected disks to be online.
        1.  Click **Start** in the task bar. In the displayed **Start** menu, right-click **Computer** and choose **Manage** from the shortcut menu.

            The **Server Manager** page is displayed.

        2.  In the navigation pane on the left, choose **Storage** \> **Disk Management**.

            The **Disk Management** pane is displayed.

        3.  In the left pane, the disk list is displayed. Right-click the affected disk and choose **Online** from the shortcut menu to make it online.

<a name="en-us_topic_0100593628_fig2680331163510"></a>            
            **Figure 5** Making the disk online
            ![](figures/making-the-disk-online.png "Making the disk online")

    3.  On the **Computer** page, check whether the number of disks is the same as that before the specifications modification.

        -   If yes, no further action is required.
        -   If no, contact customer service.
<a name="en-us_topic_0100593628_fig746964620392"></a>        
        **Figure 6** Disk attachment after disk online
        ![](figures/disk-attachment-after-disk-online.png "Disk attachment after disk online")

-   Linux ECSs
    1.  Log in to the ECS as user **root**.
    2.  Run the following command to view the disks attached before specifications modification:

        **fdisk -l** **| grep 'Disk /dev/'**

<a name="en-us_topic_0120890833_fig10595124010458"></a>        
        **Figure 7** Viewing disks attached before specifications modification
        ![](figures/viewing-disks-attached-before-specifications-modification.png "Viewing disks attached before specifications modification")

        As shown in [Figure 7](#en-us_topic_0120890833_fig10595124010458), the ECS has three disks attached, **/dev/vda**, **/dev/vdb**, and **/dev/vdc**.

    3.  Run the following command to view disks attached after specifications modification:

        **df -h****| grep '/dev/'**

<a name="en-us_topic_0120890833_fig692535712437"></a>        
        **Figure 8** Viewing disks attached after specifications modification
        ![](figures/viewing-disks-attached-after-specifications-modification.png "Viewing disks attached after specifications modification")

        As shown in [Figure 8](#en-us_topic_0120890833_fig692535712437), the ECS has only one disk attached, **/dev/vda**.

    4.  Check whether the number of disks obtained in [2](#en-us_topic_0120890833_li218141135312) is the same as that obtained in [3](#en-us_topic_0120890833_li161843557534).
        -   If yes, the specifications have been modified. No further action is required.
        -   If no, the disk attachment failed. In such a case, go to [5](#en-us_topic_0120890833_li1478325211557).
    5.  Run the **mount** command to attach the affected disks.

        An example is provided as follows:

        **mount /dev/vbd1 /mnt/vbd1**

        In the preceding command, **/dev/vbd1** is the disk to be attached, and **/mnt/vbd1** is the path for disk attachment.

        > ![](public_sys-resources/icon-notice.gif) **NOTICE:** 

        > Ensure that **/mnt/vbd1** is empty. Otherwise, the attachment will fail.

    6.  Run the following commands to check whether the numbers of disks before and after specifications modification are the same:

        **fdisk -l** **| grep 'Disk /dev/'**

        **df -h****| grep '/dev/'**

        -   If yes, no further action is required.
        -   If no, contact customer service.
<a name="en-us_topic_0120890833_fig722411124917"></a>        
        **Figure 9** Checking the number of disks attached
        ![](figures/checking-the-number-of-disks-attached.png "Checking the number of disks attached")

        As shown in [Figure 9](#en-us_topic_0120890833_fig722411124917), the disks attached to the ECS after specifications modification are **/dev/vda**, **/dev/vdb**, **/dev/vdc**, which are the same as those before specifications modification.


## Follow-up Procedure<a name="section9461027528"></a>

Perform the following operations in the event of a specifications modification failure:

1.  Log in to the management console.
2.  Under **Management & Deployment**, click **Cloud Trace Service**.
3.  In the navigation pane on the left, choose **Cloud Trace Service** \> **Trace List**.
4.  In the **Trace Name** column, locate the **resizeServer** event by resource ID.

    The resource ID is the ID of the ECS on which the specifications modification failed.

5.  Click **View Trace** in the **Operation** column to view the failure cause.

    If the fault cannot be rectified based on logs, contact technical support.


-   **[Changing a General-Purpose ECS to an H1 ECS](changing-a-general-purpose-ecs-to-an-h1-ecs.md)**  

-   **[Changing a XEN ECS to a KVM ECS \(Windows\)](changing-a-xen-ecs-to-a-kvm-ecs-(windows).md)**  

-   **[Changing a XEN ECS to a KVM ECS \(Linux\)](changing-a-xen-ecs-to-a-kvm-ecs-(linux).md)**  


