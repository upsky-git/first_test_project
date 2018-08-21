# Configuring Redirection<a name="en-us_topic_0066088957"></a>

You can redirect all requests for one bucket to another bucket or URL by configuring  **Redirect requests**  in the  **Static Website Hosting**  dialog box.

## Prerequisites<a name="section11221613153921"></a>

All of the website files required by the static website have been uploaded to the specified bucket.

If the   website files are   **Cold** storage class, restored them first.  For more information, see  [Restoring a Cold File on OBS](restoring-a-cold-file-on-obs.md).

> ![](public_sys-resources/icon-notice.gif) **NOTICE:** 

> To ensure that a hosted static website can be accessed by all users, set anonymous users to be able to access static website files in the bucket. The configuration of static website hosting takes effect within two minutes after the configuration.

## Procedure<a name="section11587693153957"></a>

1.  Log in to OBS Console.
2.  In the bucket list, click the target bucket to go to the  **Summary**  page.
3.  In the navigation tree on the left, click  **Static Website Hosting**.
4.  Click the  **Static Website Hosting** card, and select **Redirect requests**. In the **Redirect To** text box, enter a bucket access domain name or a URL. [Figure 1](#fig8414705193626)  displays this page.

    **Figure  1**  Redirection<a name="fig8414705193626"></a>
    ![](figures/redirection.png "Redirection")

5.  Click  **OK**.
6.  In the bucket list, click the bucket to which requests for the static website are redirected.
7.  **Optional:** To ensure that a hosted static website can be accessed by all users, configure the following policy so that all static website files in the bucket can be accessed publicly.

    1.  In the navigation tree on the left, click  **Object**.
    2.  Click the target object and click  **Object ACL**.
    3.  In  **Object ACL** \> **Public Permissions** \> **Anonymous Users**, click  **Edit**  to set an object read permission for anonymous users. This option is selected in  [Figure 2](#en-us_topic_0045853755_fig18480152193315).

        **Figure  2**  Setting an object read permission for anonymous users<a name="en-us_topic_0045853755_fig18480152193315"></a>
        ![](figures/setting-an-object-read-permission-for-anonymous-users.png "Setting an object read permission for anonymous users")

    4.  Click  **Save**  to save the permission setting.
    If the bucket contains only static website files, configure the public read policy for the bucket so that all files in the bucket can be accessed publicly.

    1.  Choose  **Permissions** \> **Bucket Policy**.
    2.  Click the  **Public Read** card to allow all objects in the bucket to be accessible publicly. This option is selected in [Figure 3](#en-us_topic_0045853755_fig15186794193556).

        **Figure  3**  Configuring the public read permission<a name="en-us_topic_0045853755_fig15186794193556"></a>
        ![](figures/configuring-the-public-read-permission.png "Configuring the public read permission")

8.  Verify the configuration. Input the access domain name of the bucket in the web browser and press  **Enter**. The bucket or URL to which requests are redirected will be displayed.

    > ![](public_sys-resources/icon-note.gif) **NOTE:** 

    > In some conditions, you may need to clear the browser cache before the expected results are displayed.


