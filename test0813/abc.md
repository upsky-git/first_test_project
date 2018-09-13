## Use Restrictions<a name="section31714110141539"></a>

-   Linux
    -   The image that is used to create ECSs must have Cloud-Init installed.

    -   The user data to be injected must be less than or equal to 32 KB.
    -   If user data is uploaded as text, the data can contain only ASCII characters. If user data is uploaded using a file, the file can contain any characters and the file size cannot exceed 32 KB.
    -   The image that is used to create ECSs must be a public image, a private image created based on a public image, or a private image with Cloud-Init installed.
    -   The format of the customized scripts must comply with user data script specifications.
    -   DHCP must be enabled on the VPC network, and port 80 must be enabled for the security group in the outbound direction.
    -   Select the key pair login mode. When the password login mode is selected, the user data injection function is restricted.

-   Windows
    -   The image that is used to create ECSs must have Cloudbase-Init installed.
    -   The user data to be injected must be less than or equal to 32 KB.
    -   User data uploaded as text can contain only ASCII characters. User data uploaded as a file can contain any characters.
    -   The image that is used to create ECSs must be a public image, a private image created based on a public image, or a private image with Cloudbase-Init installed.
    -   DHCP must be enabled on the VPC network, and port 80 must be enabled for the security group in the outbound direction.
