# Creating a Security Administrator<a name="ZH-CN_TOPIC_0128613060"></a>

This section explains how to create a security administrator to manage the users in your account.

## Procedure<a name="section1825324714490"></a>

1.  Choose  **Management & Deployment** \> **Identity and Access Management**.
2.  At the upper left of the main menu bar, click  **Console**.

    ![](figures/zh-cn_image_0128790270.jpg)

3.  Click the username in the upper right corner and select  **Identity and Access Management**  from the drop-down list.

    ![](figures/zh-cn_image_0128790276.jpg)

4.  In the navigation pane, choose  **User**.
5.  On the  **User** page, click **Create User**.
6.  On the  **Create User** page, enter **Username**.
7.  Select  **Password** for **Credential Type**.

    >![](public_sys-resources/icon-note.gif) **说明：**  
    >-   A password can be used to log in to the management console and enable development tools \(such as APIs, the CLI, and SDK\) that can access cloud services through password authentication. This is the recommended option because the security administrator manages users.  
    >-   Access keys are used to enable development tools \(such as APIs, the CLI, and SDK\) that can access cloud services through key authentication.

8.  In the  **User Groups** area, select **admin**  from the drop-down list.
9.  Click  **Next**.
10. Select  **Set manually** for **Password Type**.

    >![](public_sys-resources/icon-note.gif) **说明：**  
    >A security administrator can log in to the management console and use IAM to manage users. You are advised to select  **Set manually** for **Password Type** when you create a security administrator for your account. If you create a security administrator for another user, you are advised to select **Set at first login** for **Password Type**  instead so that the user can set their own password.

11. Enter the email address, mobile number, password, and confirm password.

    >![](public_sys-resources/icon-note.gif) **说明：**  
    >-   You are advised to enter an email address or mobile number for the security administrator. These will be used as the security administrator's credentials.  
    >-   The password must meet the following requirements:  
    >    It must be 6 to 32 characters long.  
    >    It must contain at least 2 of the following character types: uppercase letters, lowercase letters, digits, and special characters \(!"\#$%&'\(\)\*+,-./:;<=\>?@\[\]^\`\{\_|\}~ and spaces\).  
    >    It cannot be the username or the username spelled backwards. For example, if the username is  **A12345**, the password cannot be **A12345**, **a12345**, **54321A** or **54321a**.  

12. Select  **Require Password Reset** to ensure that the security administrator is forced to change the password the first time the administrator logs in. The **Require Password Reset**  option is selected by default. It is recommended that you retain the default setting to ensure that the security administrator account password is set by the security administrator, preventing password leakage.
13. Click  **OK**.

