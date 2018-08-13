# GPU-accelerated ECSs<a name="EN-US_TOPIC_0097289624"></a>

GPU-accelerated ECSs provide outstanding floating-point computing capabilities. They are suitable for scenarios that require real-time, highly concurrent massive computing.

GPU-accelerated ECSs are classified as G series and P series ECSs.

-   P series ECSs are designed for deep learning, scientific computing, and CAE.
-   G series ECSs are suitable for 3D animation rendering and CAD.

## Graphics-accelerated ECSs<a name="section1215117449419"></a>

Graphics-accelerated ECSs are of the G series.

## Overview<a name="section1183983194216"></a>

-   G1 ECSs are based on NVIDIA GRID virtual GPUs and provide economical graphics acceleration. They use NVIDIA Tesla M60 GPUs and support DirectX and OpenGL. The ECSs have a maximum of 4 GB GPU memory and 4,096 x 2,160 resolution, and are used for applications that require high performance in graphics rendering.
-   G2 ECSs are based on NVIDIA Tesla M60 hardware passthrough and provide graphics acceleration and single-precision computing with a maximum of 8 GB GPU memory and 4,096 x 2,160 resolution. They support DirectX, OpenGL, CUDA, and OpenCL, provide 2,048 CUDA cores, and are used for media editing, 3D rendering, and transcoding.

Select your required GPU-accelerated ECS type and specifications.

## Specifications<a name="section086277124319"></a>

**Table 1** G1 ECS specifications

<a name="en-us_topic_0097289625_table1798535042511"></a><table><thead align="left"><tr id="en-us_topic_0097289625_row9154516253"><th class="cellrowborder" valign="top" width="17.31%" id="mcps1.2.8.1.1"><p id="en-us_topic_0097289625_p101575118251"><a name="en-us_topic_0097289625_p101575118251"></a><a name="en-us_topic_0097289625_p101575118251"></a>Flavor</p>
</th>
<th class="cellrowborder" valign="top" width="11.129999999999999%" id="mcps1.2.8.1.2"><p id="en-us_topic_0097289625_p115551142514"><a name="en-us_topic_0097289625_p115551142514"></a><a name="en-us_topic_0097289625_p115551142514"></a>vCPUs</p>
</th>
<th class="cellrowborder" valign="top" width="13.56%" id="mcps1.2.8.1.3"><p id="en-us_topic_0097289625_p131205132520"><a name="en-us_topic_0097289625_p131205132520"></a><a name="en-us_topic_0097289625_p131205132520"></a>Memory (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="12.5%" id="mcps1.2.8.1.4"><p id="en-us_topic_0097289625_p0311351132510"><a name="en-us_topic_0097289625_p0311351132510"></a><a name="en-us_topic_0097289625_p0311351132510"></a>GPUs</p>
</th>
<th class="cellrowborder" valign="top" width="13.81%" id="mcps1.2.8.1.5"><p id="en-us_topic_0097289625_p9472051122515"><a name="en-us_topic_0097289625_p9472051122515"></a><a name="en-us_topic_0097289625_p9472051122515"></a>GPU Memory (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="12.989999999999998%" id="mcps1.2.8.1.6"><p id="en-us_topic_0097289625_p194745114255"><a name="en-us_topic_0097289625_p194745114255"></a><a name="en-us_topic_0097289625_p194745114255"></a>Local Disks</p>
</th>
<th class="cellrowborder" valign="top" width="18.7%" id="mcps1.2.8.1.7"><p id="en-us_topic_0097289625_p547551182516"><a name="en-us_topic_0097289625_p547551182516"></a><a name="en-us_topic_0097289625_p547551182516"></a>Virtualization Type</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0097289625_row144719513251"><td class="cellrowborder" valign="top" width="17.31%" headers="mcps1.2.8.1.1 "><p id="en-us_topic_0097289625_p947551152515"><a name="en-us_topic_0097289625_p947551152515"></a><a name="en-us_topic_0097289625_p947551152515"></a>p1.2xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" width="11.129999999999999%" headers="mcps1.2.8.1.2 "><p id="en-us_topic_0097289625_p162175172514"><a name="en-us_topic_0097289625_p162175172514"></a><a name="en-us_topic_0097289625_p162175172514"></a>8</p>
</td>
<td class="cellrowborder" valign="top" width="13.56%" headers="mcps1.2.8.1.3 "><p id="en-us_topic_0097289625_p862135142512"><a name="en-us_topic_0097289625_p862135142512"></a><a name="en-us_topic_0097289625_p862135142512"></a>64</p>
</td>
<td class="cellrowborder" valign="top" width="12.5%" headers="mcps1.2.8.1.4 "><p id="en-us_topic_0097289625_p116285113259"><a name="en-us_topic_0097289625_p116285113259"></a><a name="en-us_topic_0097289625_p116285113259"></a>1 x P100</p>
</td>
<td class="cellrowborder" valign="top" width="13.81%" headers="mcps1.2.8.1.5 "><p id="en-us_topic_0097289625_p477155119258"><a name="en-us_topic_0097289625_p477155119258"></a><a name="en-us_topic_0097289625_p477155119258"></a>1 x 16</p>
</td>
<td class="cellrowborder" valign="top" width="12.989999999999998%" headers="mcps1.2.8.1.6 "><p id="en-us_topic_0097289625_p27765102515"><a name="en-us_topic_0097289625_p27765102515"></a><a name="en-us_topic_0097289625_p27765102515"></a>1 x 800 GB NVMe</p>
</td>
<td class="cellrowborder" valign="top" width="18.7%" headers="mcps1.2.8.1.7 "><p id="en-us_topic_0097289625_p4778518256"><a name="en-us_topic_0097289625_p4778518256"></a><a name="en-us_topic_0097289625_p4778518256"></a>KVM</p>
</td>
</tr>
<tr id="en-us_topic_0097289625_row1477851132510"><td class="cellrowborder" valign="top" width="17.31%" headers="mcps1.2.8.1.1 "><p id="en-us_topic_0097289625_p07712519257"><a name="en-us_topic_0097289625_p07712519257"></a><a name="en-us_topic_0097289625_p07712519257"></a>p1.4xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" width="11.129999999999999%" headers="mcps1.2.8.1.2 "><p id="en-us_topic_0097289625_p877851142519"><a name="en-us_topic_0097289625_p877851142519"></a><a name="en-us_topic_0097289625_p877851142519"></a>16</p>
</td>
<td class="cellrowborder" valign="top" width="13.56%" headers="mcps1.2.8.1.3 "><p id="en-us_topic_0097289625_p49412517257"><a name="en-us_topic_0097289625_p49412517257"></a><a name="en-us_topic_0097289625_p49412517257"></a>128</p>
</td>
<td class="cellrowborder" valign="top" width="12.5%" headers="mcps1.2.8.1.4 "><p id="en-us_topic_0097289625_p139455110255"><a name="en-us_topic_0097289625_p139455110255"></a><a name="en-us_topic_0097289625_p139455110255"></a>2 x P100</p>
</td>
<td class="cellrowborder" valign="top" width="13.81%" headers="mcps1.2.8.1.5 "><p id="en-us_topic_0097289625_p194125117259"><a name="en-us_topic_0097289625_p194125117259"></a><a name="en-us_topic_0097289625_p194125117259"></a>2 x 16</p>
</td>
<td class="cellrowborder" valign="top" width="12.989999999999998%" headers="mcps1.2.8.1.6 "><p id="en-us_topic_0097289625_p18109145172511"><a name="en-us_topic_0097289625_p18109145172511"></a><a name="en-us_topic_0097289625_p18109145172511"></a>2 x 800 GB NVMe</p>
</td>
<td class="cellrowborder" valign="top" width="18.7%" headers="mcps1.2.8.1.7 "><p id="en-us_topic_0097289625_p710955119257"><a name="en-us_topic_0097289625_p710955119257"></a><a name="en-us_topic_0097289625_p710955119257"></a>KVM</p>
</td>
</tr>
<tr id="en-us_topic_0097289625_row910915118254"><td class="cellrowborder" valign="top" width="17.31%" headers="mcps1.2.8.1.1 "><p id="en-us_topic_0097289625_p1810915192516"><a name="en-us_topic_0097289625_p1810915192516"></a><a name="en-us_topic_0097289625_p1810915192516"></a>p1.8xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" width="11.129999999999999%" headers="mcps1.2.8.1.2 "><p id="en-us_topic_0097289625_p17109185172515"><a name="en-us_topic_0097289625_p17109185172515"></a><a name="en-us_topic_0097289625_p17109185172515"></a>32</p>
</td>
<td class="cellrowborder" valign="top" width="13.56%" headers="mcps1.2.8.1.3 "><p id="en-us_topic_0097289625_p191241751102519"><a name="en-us_topic_0097289625_p191241751102519"></a><a name="en-us_topic_0097289625_p191241751102519"></a>256</p>
</td>
<td class="cellrowborder" valign="top" width="12.5%" headers="mcps1.2.8.1.4 "><p id="en-us_topic_0097289625_p1912425111254"><a name="en-us_topic_0097289625_p1912425111254"></a><a name="en-us_topic_0097289625_p1912425111254"></a>4 x P100</p>
</td>
<td class="cellrowborder" valign="top" width="13.81%" headers="mcps1.2.8.1.5 "><p id="en-us_topic_0097289625_p15141251122513"><a name="en-us_topic_0097289625_p15141251122513"></a><a name="en-us_topic_0097289625_p15141251122513"></a>4 x 16</p>
</td>
<td class="cellrowborder" valign="top" width="12.989999999999998%" headers="mcps1.2.8.1.6 "><p id="en-us_topic_0097289625_p014125120252"><a name="en-us_topic_0097289625_p014125120252"></a><a name="en-us_topic_0097289625_p014125120252"></a>4 x 800 GB NVMe</p>
</td>
<td class="cellrowborder" valign="top" width="18.7%" headers="mcps1.2.8.1.7 "><p id="en-us_topic_0097289625_p71411351112515"><a name="en-us_topic_0097289625_p71411351112515"></a><a name="en-us_topic_0097289625_p71411351112515"></a>KVM</p>
</td>
</tr>
</tbody>
</table>

**Table 2** G2 ECS specifications

<a name="en-us_topic_0035470098_table7775011212929"></a><table><thead align="left"><tr id="en-us_topic_0035470098_row29182590212929"><th class="cellrowborder" valign="top" width="15.341534153415342%" id="mcps1.2.8.1.1"><p id="en-us_topic_0035470098_p12988542163236"><a name="en-us_topic_0035470098_p12988542163236"></a><a name="en-us_topic_0035470098_p12988542163236"></a>ECS Type</p>
</th>
<th class="cellrowborder" valign="top" width="11.111111111111112%" id="mcps1.2.8.1.2"><p id="en-us_topic_0035470098_p45438961163236"><a name="en-us_topic_0035470098_p45438961163236"></a><a name="en-us_topic_0035470098_p45438961163236"></a>vCPUs</p>
</th>
<th class="cellrowborder" valign="top" width="13.451345134513454%" id="mcps1.2.8.1.3"><p id="en-us_topic_0035470098_p56677196163236"><a name="en-us_topic_0035470098_p56677196163236"></a><a name="en-us_topic_0035470098_p56677196163236"></a>Memory (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="14.841484148414844%" id="mcps1.2.8.1.4"><p id="en-us_topic_0035470098_p27450168163236"><a name="en-us_topic_0035470098_p27450168163236"></a><a name="en-us_topic_0035470098_p27450168163236"></a>Flavor</p>
</th>
<th class="cellrowborder" valign="top" width="18.511851185118513%" id="mcps1.2.8.1.5"><p id="en-us_topic_0035470098_p469116389117"><a name="en-us_topic_0035470098_p469116389117"></a><a name="en-us_topic_0035470098_p469116389117"></a>Virtualization Type</p>
</th>
<th class="cellrowborder" valign="top" width="13.561356135613561%" id="mcps1.2.8.1.6"><p id="en-us_topic_0035470098_p8871132163236"><a name="en-us_topic_0035470098_p8871132163236"></a><a name="en-us_topic_0035470098_p8871132163236"></a>GPUs</p>
</th>
<th class="cellrowborder" valign="top" width="13.181318131813184%" id="mcps1.2.8.1.7"><p id="en-us_topic_0035470098_p472154285220"><a name="en-us_topic_0035470098_p472154285220"></a><a name="en-us_topic_0035470098_p472154285220"></a>GPU Memory (GB)</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0035470098_row54750026212929"><td class="cellrowborder" valign="top" width="15.341534153415342%" headers="mcps1.2.8.1.1 "><p id="en-us_topic_0035470098_p5567097212929"><a name="en-us_topic_0035470098_p5567097212929"></a><a name="en-us_topic_0035470098_p5567097212929"></a>Accelerated graphics processing G2</p>
</td>
<td class="cellrowborder" valign="top" width="11.111111111111112%" headers="mcps1.2.8.1.2 "><p id="en-us_topic_0035470098_p48281701212929"><a name="en-us_topic_0035470098_p48281701212929"></a><a name="en-us_topic_0035470098_p48281701212929"></a>8</p>
</td>
<td class="cellrowborder" valign="top" width="13.451345134513454%" headers="mcps1.2.8.1.3 "><p id="en-us_topic_0035470098_p18503669212929"><a name="en-us_topic_0035470098_p18503669212929"></a><a name="en-us_topic_0035470098_p18503669212929"></a>64</p>
</td>
<td class="cellrowborder" valign="top" width="14.841484148414844%" headers="mcps1.2.8.1.4 "><p id="en-us_topic_0035470098_p22402193212929"><a name="en-us_topic_0035470098_p22402193212929"></a><a name="en-us_topic_0035470098_p22402193212929"></a>g2.2xlarge</p>
</td>
<td class="cellrowborder" valign="top" width="18.511851185118513%" headers="mcps1.2.8.1.5 "><p id="en-us_topic_0035470098_p669843811111"><a name="en-us_topic_0035470098_p669843811111"></a><a name="en-us_topic_0035470098_p669843811111"></a>XEN</p>
</td>
<td class="cellrowborder" valign="top" width="13.561356135613561%" headers="mcps1.2.8.1.6 "><p id="en-us_topic_0035470098_p2638370212929"><a name="en-us_topic_0035470098_p2638370212929"></a><a name="en-us_topic_0035470098_p2638370212929"></a>1 x M60</p>
</td>
<td class="cellrowborder" valign="top" width="13.181318131813184%" headers="mcps1.2.8.1.7 "><p id="en-us_topic_0035470098_p18721114214525"><a name="en-us_topic_0035470098_p18721114214525"></a><a name="en-us_topic_0035470098_p18721114214525"></a>8</p>
</td>
</tr>
</tbody>
</table>

## Features<a name="section12506144018439"></a>

-   G1 ECSs have the following features:
    -   NVIDIA M60 GPUs
    -   Graphics acceleration applications
    -   GPU hardware virtualization \(vGPUs\) and GPU passthrough
    -   Application flow identical to common ECSs
    -   Automatic scheduling of G1 ECSs to AZs where NVIDIA M60 GPUs are used
    -   A maximum specification of 1 GB GPU memory and 4,096 x 2,160 resolution for processing graphics and videos
-   G2 ECSs have the following features:
    -   NVIDIA M60 GPUs
    -   Graphics acceleration applications
    -   GPU hardware passthrough
    -   Enhanced SR-IOV network performance and high bandwidths
    -   Automatic scheduling of G2 ECSs to AZs where NVIDIA M60 GPUs are used
    -   A maximum specification of 8 GB GPU memory and 4,096 x 2,160 resolution for processing graphics and videos
    -   DirectX, OpenGL, CUDA, and OpenCL
    -   Up to 2,048 CUDA cores

## Notes on Using G1 ECSs<a name="section17279310134415"></a>

-   G1 ECSs do not support specifications modification.
-   G1 ECSs support the following OSs:
    -   Windows Server 2008
    -   Windows Server 2012
    -   Windows Server 2016
-   If a G1 ECS is created using a private image, install a GPU driver on the ECS after the ECS creation. To download the driver, log in at [http://www.nvidia.com/grid-eval](http://www.nvidia.com/grid-eval), set the NVIDIA GRID version to **4.1**, and select the **GRID for UVP** software package. The operations are as follows:
    1.  Check whether NVIDIA is used for the first time:
        1.  If yes, go to step [2](#en-us_topic_0035470098_li6493917120957).
        2.  If no, go to step [4](#en-us_topic_0035470098_li31331234738).
    2.  Obtain the Product Activation Key \(PAK\) from the email indicating successful registration with NVIDIA.

<a name="en-us_topic_0035470098_fig4249148201328"></a>        
        **Figure 1** PAK
        ![](figures/pak.png "PAK")

    3.  Enter the PAK obtained in step [2](#en-us_topic_0035470098_li6493917120957) on the **Redeem Product Activation Keys** page and click **Redeem**.

<a name="en-us_topic_0035470098_fig66917708201838"></a>        
        **Figure 2** Redeem Product Activation Keys
        ![](figures/redeem-product-activation-keys.png "Redeem Product Activation Keys")

    4.  Specify **Username** and **Password** and click **LOGIN**.

<a name="en-us_topic_0035470098_fig823115144396"></a>        
        **Figure 3** Logging in to the official NVIDIA website
        ![](figures/logging-in-to-the-official-nvidia-website.png "Logging in to the official NVIDIA website")

    5.  Log in at the official NVIDIA website as prompted and choose **Software & Services** \> **Product Information**.

        ![](figures/en-us_image_0111995152.png)

    6.  Click the **Archived Versions** tab.
    7.  Click **NVIDIA GRID** of version **4.1**.
    8.  On the **Product Download** page, click **GRID for UVP**.
-   If you log in to a G1 ECS using a RDP-based remote login tool, such as Windows MSTSC, GPU acceleration will fail. This is because MSTSC replaces the WDDM GPU driver with a non-accelerated remote desktop display driver. Therefore, you must use other methods to log in to the ECS, such as VNC.

    If the remote login function available on the management console fails to meet your service requirements, you must install a suitable remote login tool on the ECS.


## Notes on Using G2 ECSs<a name="section134701740154413"></a>

-   G2 ECSs do not support specifications modification.
-   G2 ECSs support the following OSs:
    -   Windows Server 2008
    -   Windows Server 2012
-   If a G2 ECS is created using a private image, make sure that the GPU driver has been installed during the private image creation. If not, install the driver after creating the ECS.

    To download the GPU driver, log in at [http://www.nvidia.com/Download/index.aspx?lang=en-us](http://www.nvidia.com/Download/index.aspx?lang=en-us). You are advised to select the latest CUDA toolkit version.

    > ![](public_sys-resources/icon-notice.gif) **NOTICE:** 

    > After the GPU driver is installed, run the following command to switch the GPU working mode and restart the ECS \(for example, the GPU driver is installed in **C:\\Program Files\\NVIDIA Corporation\\NVSMI\\nvidia-smi.exe**\):

    > **"C:\\Program Files\\NVIDIA Corporation\\NVSMI\\nvidia-smi.exe" -dm 0**

-   If a G2 ECS is created using a private image, make sure that the SR-IOV driver has been installed during the private image creation. If not, install the driver after creating the ECS.

    To download the SR-IOV driver, log in at [https://downloadcenter.intel.com/search?keyword=Intel++Ethernet+Connections+CD](https://downloadcenter.intel.com/search?keyword=Intel++Ethernet+Connections+CD). You are advised to select version 20.4.1 or later.

    During driver installation, if you encounter the "No Intel adapter found" error, see section [How Can I Handle the Issue that a Windows 7 ECS with an Intel 82599 NIC Installed Reports an Error in SR-IOV Scenarios?](how-can-i-handle-the-issue-that-a-windows-7-ecs-with-an-intel-82599-nic-installed-reports-an-error-i.md) for troubleshooting.

-   If you log in to a G2 ECS using MSTSC, GPU acceleration will fail. This is because MSTSC replaces the WDDM GPU driver with a non-accelerated remote desktop display driver. Therefore, you must use other methods to log in to the ECS, such as VNC.
-   G2 ECSs do not support remote login provided by the public cloud platform. Before logging in to such an ECS using VNC, install the VNC server on the ECS.

## Computing-accelerated ECSs<a name="section972518219465"></a>

Computing-accelerated ECSs are of the P series.

## Overview<a name="section553153824516"></a>

P1 ECSs use NVIDIA Tesla P100 GPUs and provide flexibility, high performance, and cost-effectiveness. These ECSs support GPU Direct for direct communication between GPUs, improving data transmission efficiency. P1 ECSs provide outstanding universal computing capabilities and have strengths in deep learning, graphic databases, high-performance databases, Computational Fluid Dynamics \(CFD\), computing finance, seismic analysis, molecular modeling, and genomics. They are designed for scientific computing.

Compared with P1 ECSs, P2 ECSs use NVIDIA Tesla V100 GPUs, which have improved both single- and double-precision computing capabilities by 50% and offering 112 TFLOPS of deep learning.

## Specifications<a name="section99992153464"></a>

**Table 3** P1 ECS specifications

<a name="en-us_topic_0097289625_table1798535042511"></a><table><thead align="left"><tr id="en-us_topic_0097289625_row9154516253"><th class="cellrowborder" valign="top" width="17.31%" id="mcps1.2.8.1.1"><p id="en-us_topic_0097289625_p101575118251"><a name="en-us_topic_0097289625_p101575118251"></a><a name="en-us_topic_0097289625_p101575118251"></a>Flavor</p>
</th>
<th class="cellrowborder" valign="top" width="11.129999999999999%" id="mcps1.2.8.1.2"><p id="en-us_topic_0097289625_p115551142514"><a name="en-us_topic_0097289625_p115551142514"></a><a name="en-us_topic_0097289625_p115551142514"></a>vCPUs</p>
</th>
<th class="cellrowborder" valign="top" width="13.56%" id="mcps1.2.8.1.3"><p id="en-us_topic_0097289625_p131205132520"><a name="en-us_topic_0097289625_p131205132520"></a><a name="en-us_topic_0097289625_p131205132520"></a>Memory (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="12.5%" id="mcps1.2.8.1.4"><p id="en-us_topic_0097289625_p0311351132510"><a name="en-us_topic_0097289625_p0311351132510"></a><a name="en-us_topic_0097289625_p0311351132510"></a>GPUs</p>
</th>
<th class="cellrowborder" valign="top" width="13.81%" id="mcps1.2.8.1.5"><p id="en-us_topic_0097289625_p9472051122515"><a name="en-us_topic_0097289625_p9472051122515"></a><a name="en-us_topic_0097289625_p9472051122515"></a>GPU Memory (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="12.989999999999998%" id="mcps1.2.8.1.6"><p id="en-us_topic_0097289625_p194745114255"><a name="en-us_topic_0097289625_p194745114255"></a><a name="en-us_topic_0097289625_p194745114255"></a>Local Disks</p>
</th>
<th class="cellrowborder" valign="top" width="18.7%" id="mcps1.2.8.1.7"><p id="en-us_topic_0097289625_p547551182516"><a name="en-us_topic_0097289625_p547551182516"></a><a name="en-us_topic_0097289625_p547551182516"></a>Virtualization Type</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0097289625_row144719513251"><td class="cellrowborder" valign="top" width="17.31%" headers="mcps1.2.8.1.1 "><p id="en-us_topic_0097289625_p947551152515"><a name="en-us_topic_0097289625_p947551152515"></a><a name="en-us_topic_0097289625_p947551152515"></a>p1.2xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" width="11.129999999999999%" headers="mcps1.2.8.1.2 "><p id="en-us_topic_0097289625_p162175172514"><a name="en-us_topic_0097289625_p162175172514"></a><a name="en-us_topic_0097289625_p162175172514"></a>8</p>
</td>
<td class="cellrowborder" valign="top" width="13.56%" headers="mcps1.2.8.1.3 "><p id="en-us_topic_0097289625_p862135142512"><a name="en-us_topic_0097289625_p862135142512"></a><a name="en-us_topic_0097289625_p862135142512"></a>64</p>
</td>
<td class="cellrowborder" valign="top" width="12.5%" headers="mcps1.2.8.1.4 "><p id="en-us_topic_0097289625_p116285113259"><a name="en-us_topic_0097289625_p116285113259"></a><a name="en-us_topic_0097289625_p116285113259"></a>1 x P100</p>
</td>
<td class="cellrowborder" valign="top" width="13.81%" headers="mcps1.2.8.1.5 "><p id="en-us_topic_0097289625_p477155119258"><a name="en-us_topic_0097289625_p477155119258"></a><a name="en-us_topic_0097289625_p477155119258"></a>1 x 16</p>
</td>
<td class="cellrowborder" valign="top" width="12.989999999999998%" headers="mcps1.2.8.1.6 "><p id="en-us_topic_0097289625_p27765102515"><a name="en-us_topic_0097289625_p27765102515"></a><a name="en-us_topic_0097289625_p27765102515"></a>1 x 800 GB NVMe</p>
</td>
<td class="cellrowborder" valign="top" width="18.7%" headers="mcps1.2.8.1.7 "><p id="en-us_topic_0097289625_p4778518256"><a name="en-us_topic_0097289625_p4778518256"></a><a name="en-us_topic_0097289625_p4778518256"></a>KVM</p>
</td>
</tr>
<tr id="en-us_topic_0097289625_row1477851132510"><td class="cellrowborder" valign="top" width="17.31%" headers="mcps1.2.8.1.1 "><p id="en-us_topic_0097289625_p07712519257"><a name="en-us_topic_0097289625_p07712519257"></a><a name="en-us_topic_0097289625_p07712519257"></a>p1.4xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" width="11.129999999999999%" headers="mcps1.2.8.1.2 "><p id="en-us_topic_0097289625_p877851142519"><a name="en-us_topic_0097289625_p877851142519"></a><a name="en-us_topic_0097289625_p877851142519"></a>16</p>
</td>
<td class="cellrowborder" valign="top" width="13.56%" headers="mcps1.2.8.1.3 "><p id="en-us_topic_0097289625_p49412517257"><a name="en-us_topic_0097289625_p49412517257"></a><a name="en-us_topic_0097289625_p49412517257"></a>128</p>
</td>
<td class="cellrowborder" valign="top" width="12.5%" headers="mcps1.2.8.1.4 "><p id="en-us_topic_0097289625_p139455110255"><a name="en-us_topic_0097289625_p139455110255"></a><a name="en-us_topic_0097289625_p139455110255"></a>2 x P100</p>
</td>
<td class="cellrowborder" valign="top" width="13.81%" headers="mcps1.2.8.1.5 "><p id="en-us_topic_0097289625_p194125117259"><a name="en-us_topic_0097289625_p194125117259"></a><a name="en-us_topic_0097289625_p194125117259"></a>2 x 16</p>
</td>
<td class="cellrowborder" valign="top" width="12.989999999999998%" headers="mcps1.2.8.1.6 "><p id="en-us_topic_0097289625_p18109145172511"><a name="en-us_topic_0097289625_p18109145172511"></a><a name="en-us_topic_0097289625_p18109145172511"></a>2 x 800 GB NVMe</p>
</td>
<td class="cellrowborder" valign="top" width="18.7%" headers="mcps1.2.8.1.7 "><p id="en-us_topic_0097289625_p710955119257"><a name="en-us_topic_0097289625_p710955119257"></a><a name="en-us_topic_0097289625_p710955119257"></a>KVM</p>
</td>
</tr>
<tr id="en-us_topic_0097289625_row910915118254"><td class="cellrowborder" valign="top" width="17.31%" headers="mcps1.2.8.1.1 "><p id="en-us_topic_0097289625_p1810915192516"><a name="en-us_topic_0097289625_p1810915192516"></a><a name="en-us_topic_0097289625_p1810915192516"></a>p1.8xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" width="11.129999999999999%" headers="mcps1.2.8.1.2 "><p id="en-us_topic_0097289625_p17109185172515"><a name="en-us_topic_0097289625_p17109185172515"></a><a name="en-us_topic_0097289625_p17109185172515"></a>32</p>
</td>
<td class="cellrowborder" valign="top" width="13.56%" headers="mcps1.2.8.1.3 "><p id="en-us_topic_0097289625_p191241751102519"><a name="en-us_topic_0097289625_p191241751102519"></a><a name="en-us_topic_0097289625_p191241751102519"></a>256</p>
</td>
<td class="cellrowborder" valign="top" width="12.5%" headers="mcps1.2.8.1.4 "><p id="en-us_topic_0097289625_p1912425111254"><a name="en-us_topic_0097289625_p1912425111254"></a><a name="en-us_topic_0097289625_p1912425111254"></a>4 x P100</p>
</td>
<td class="cellrowborder" valign="top" width="13.81%" headers="mcps1.2.8.1.5 "><p id="en-us_topic_0097289625_p15141251122513"><a name="en-us_topic_0097289625_p15141251122513"></a><a name="en-us_topic_0097289625_p15141251122513"></a>4 x 16</p>
</td>
<td class="cellrowborder" valign="top" width="12.989999999999998%" headers="mcps1.2.8.1.6 "><p id="en-us_topic_0097289625_p014125120252"><a name="en-us_topic_0097289625_p014125120252"></a><a name="en-us_topic_0097289625_p014125120252"></a>4 x 800 GB NVMe</p>
</td>
<td class="cellrowborder" valign="top" width="18.7%" headers="mcps1.2.8.1.7 "><p id="en-us_topic_0097289625_p71411351112515"><a name="en-us_topic_0097289625_p71411351112515"></a><a name="en-us_topic_0097289625_p71411351112515"></a>KVM</p>
</td>
</tr>
</tbody>
</table>

**Table 4** P2 ECS specifications

<a name="en-us_topic_0097289625_table12952452949"></a><table><thead align="left"><tr id="en-us_topic_0097289625_row795314521546"><th class="cellrowborder" valign="top" width="15.841584158415841%" id="mcps1.2.8.1.1"><p id="en-us_topic_0097289625_p0450113959"><a name="en-us_topic_0097289625_p0450113959"></a><a name="en-us_topic_0097289625_p0450113959"></a>Flavor</p>
</th>
<th class="cellrowborder" valign="top" width="11.881188118811881%" id="mcps1.2.8.1.2"><p id="en-us_topic_0097289625_p5445413453"><a name="en-us_topic_0097289625_p5445413453"></a><a name="en-us_topic_0097289625_p5445413453"></a>vCPUs</p>
</th>
<th class="cellrowborder" valign="top" width="13.86138613861386%" id="mcps1.2.8.1.3"><p id="en-us_topic_0097289625_p8448141313516"><a name="en-us_topic_0097289625_p8448141313516"></a><a name="en-us_topic_0097289625_p8448141313516"></a>Memory (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="14.851485148514849%" id="mcps1.2.8.1.4"><p id="en-us_topic_0097289625_p24544131854"><a name="en-us_topic_0097289625_p24544131854"></a><a name="en-us_topic_0097289625_p24544131854"></a>GPUs</p>
</th>
<th class="cellrowborder" valign="top" width="13.86138613861386%" id="mcps1.2.8.1.5"><p id="en-us_topic_0097289625_p1345617133510"><a name="en-us_topic_0097289625_p1345617133510"></a><a name="en-us_topic_0097289625_p1345617133510"></a>GPU Memory (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.8.1.6"><p id="en-us_topic_0097289625_p64585138511"><a name="en-us_topic_0097289625_p64585138511"></a><a name="en-us_topic_0097289625_p64585138511"></a>Local Disks</p>
</th>
<th class="cellrowborder" valign="top" width="11.881188118811881%" id="mcps1.2.8.1.7"><p id="en-us_topic_0097289625_p245216136510"><a name="en-us_topic_0097289625_p245216136510"></a><a name="en-us_topic_0097289625_p245216136510"></a>Virtualization Type</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0097289625_row179536521643"><td class="cellrowborder" valign="top" width="15.841584158415841%" headers="mcps1.2.8.1.1 "><p id="en-us_topic_0097289625_p6953852243"><a name="en-us_topic_0097289625_p6953852243"></a><a name="en-us_topic_0097289625_p6953852243"></a>p2.2xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.8.1.2 "><p id="en-us_topic_0097289625_p89530521741"><a name="en-us_topic_0097289625_p89530521741"></a><a name="en-us_topic_0097289625_p89530521741"></a>8</p>
</td>
<td class="cellrowborder" valign="top" width="13.86138613861386%" headers="mcps1.2.8.1.3 "><p id="en-us_topic_0097289625_p3953165219412"><a name="en-us_topic_0097289625_p3953165219412"></a><a name="en-us_topic_0097289625_p3953165219412"></a>64</p>
</td>
<td class="cellrowborder" valign="top" width="14.851485148514849%" headers="mcps1.2.8.1.4 "><p id="en-us_topic_0097289625_p457511455819"><a name="en-us_topic_0097289625_p457511455819"></a><a name="en-us_topic_0097289625_p457511455819"></a>1 x V100</p>
</td>
<td class="cellrowborder" valign="top" width="13.86138613861386%" headers="mcps1.2.8.1.5 "><p id="en-us_topic_0097289625_p1495317521646"><a name="en-us_topic_0097289625_p1495317521646"></a><a name="en-us_topic_0097289625_p1495317521646"></a>1 x 16</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.8.1.6 "><p id="en-us_topic_0097289625_p169538521142"><a name="en-us_topic_0097289625_p169538521142"></a><a name="en-us_topic_0097289625_p169538521142"></a>1 x 800 GB NVMe</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.8.1.7 "><p id="en-us_topic_0097289625_p995317522419"><a name="en-us_topic_0097289625_p995317522419"></a><a name="en-us_topic_0097289625_p995317522419"></a>KVM</p>
</td>
</tr>
<tr id="en-us_topic_0097289625_row295313520410"><td class="cellrowborder" valign="top" width="15.841584158415841%" headers="mcps1.2.8.1.1 "><p id="en-us_topic_0097289625_p1495365216414"><a name="en-us_topic_0097289625_p1495365216414"></a><a name="en-us_topic_0097289625_p1495365216414"></a>p2.4xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.8.1.2 "><p id="en-us_topic_0097289625_p5953152448"><a name="en-us_topic_0097289625_p5953152448"></a><a name="en-us_topic_0097289625_p5953152448"></a>16</p>
</td>
<td class="cellrowborder" valign="top" width="13.86138613861386%" headers="mcps1.2.8.1.3 "><p id="en-us_topic_0097289625_p1995310521448"><a name="en-us_topic_0097289625_p1995310521448"></a><a name="en-us_topic_0097289625_p1995310521448"></a>128</p>
</td>
<td class="cellrowborder" valign="top" width="14.851485148514849%" headers="mcps1.2.8.1.4 "><p id="en-us_topic_0097289625_p15578194512818"><a name="en-us_topic_0097289625_p15578194512818"></a><a name="en-us_topic_0097289625_p15578194512818"></a>2 x V100</p>
</td>
<td class="cellrowborder" valign="top" width="13.86138613861386%" headers="mcps1.2.8.1.5 "><p id="en-us_topic_0097289625_p149536523416"><a name="en-us_topic_0097289625_p149536523416"></a><a name="en-us_topic_0097289625_p149536523416"></a>2 x 16</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.8.1.6 "><p id="en-us_topic_0097289625_p14953115218417"><a name="en-us_topic_0097289625_p14953115218417"></a><a name="en-us_topic_0097289625_p14953115218417"></a>2 x 800 GB NVMe</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.8.1.7 "><p id="en-us_topic_0097289625_p59534521745"><a name="en-us_topic_0097289625_p59534521745"></a><a name="en-us_topic_0097289625_p59534521745"></a>KVM</p>
</td>
</tr>
<tr id="en-us_topic_0097289625_row1295315211419"><td class="cellrowborder" valign="top" width="15.841584158415841%" headers="mcps1.2.8.1.1 "><p id="en-us_topic_0097289625_p19953452149"><a name="en-us_topic_0097289625_p19953452149"></a><a name="en-us_topic_0097289625_p19953452149"></a>p2.8xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.8.1.2 "><p id="en-us_topic_0097289625_p20953205215419"><a name="en-us_topic_0097289625_p20953205215419"></a><a name="en-us_topic_0097289625_p20953205215419"></a>32</p>
</td>
<td class="cellrowborder" valign="top" width="13.86138613861386%" headers="mcps1.2.8.1.3 "><p id="en-us_topic_0097289625_p18953452147"><a name="en-us_topic_0097289625_p18953452147"></a><a name="en-us_topic_0097289625_p18953452147"></a>256</p>
</td>
<td class="cellrowborder" valign="top" width="14.851485148514849%" headers="mcps1.2.8.1.4 "><p id="en-us_topic_0097289625_p1958454514813"><a name="en-us_topic_0097289625_p1958454514813"></a><a name="en-us_topic_0097289625_p1958454514813"></a>4 x V100</p>
</td>
<td class="cellrowborder" valign="top" width="13.86138613861386%" headers="mcps1.2.8.1.5 "><p id="en-us_topic_0097289625_p9953552347"><a name="en-us_topic_0097289625_p9953552347"></a><a name="en-us_topic_0097289625_p9953552347"></a>4 x 16</p>
</td>
<td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.8.1.6 "><p id="en-us_topic_0097289625_p19537525410"><a name="en-us_topic_0097289625_p19537525410"></a><a name="en-us_topic_0097289625_p19537525410"></a>4 x 800 GB NVMe</p>
</td>
<td class="cellrowborder" valign="top" width="11.881188118811881%" headers="mcps1.2.8.1.7 "><p id="en-us_topic_0097289625_p895375215411"><a name="en-us_topic_0097289625_p895375215411"></a><a name="en-us_topic_0097289625_p895375215411"></a>KVM</p>
</td>
</tr>
</tbody>
</table>

## Features<a name="section3303185211460"></a>

-   P1 ECSs have the following features:
    -   NVIDIA Tesla P100 GPUs
    -   9.3 TFLOPS for single precision and 4.7 TFLOPS for double precision
    -   Maximum bandwidth of 10 Gbit/s
    -   16 GB HBM2 GPU memory with a bandwidth of 732 Gbit/s
    -   800 GB NVMe SSD disks for temporary local storage
    -   Comprehensive basic capabilities

        Networks are user-defined, subnets can be divided, and network access policies can be configured as needed. Mass storage is used, elastic capacity expansion as well as backup and restoration are supported to make data more secure. Auto Scaling allows you to add or reduce the number of ECSs quickly.

    -   Flexibility

        Similar to other types of ECSs, P1 ECSs can be provisioned in a few minutes. You can configure specifications as needed. P1 ECSs with two, four, and eight GPUs will be supported later.

    -   Excellent supercomputing ecosystem

        The supercomputing ecosystem allows you to build up a flexible, high-performance, cost-effective computing platform. A large number of HPC applications and deep-learning frameworks can run on P1 ECSs.

-   P2 ECSs have the following features:
    -   NVIDIA Tesla V100 GPUs
    -   14 TFLOPS of single-precision computing, 7 TFLOPS of double-precision computing, and 112 TFLOPS of deep learning
    -   Maximum bandwidth of 12 Gbit/s
    -   16 GB HBM2 GPU memory with a bandwidth of 900 Gbit/s
    -   800 GB NVMe SSD disks for temporary local storage
    -   Comprehensive basic capabilities

        Networks are user-defined, subnets can be divided, and network access policies can be configured as needed. Mass storage is used, elastic capacity expansion as well as backup and restoration are supported to make data more secure. Auto Scaling allows you to add or reduce the number of ECSs quickly.

    -   Flexibility

        Similar to other types of ECSs, P2 ECSs can be provisioned in a few minutes.

    -   Excellent supercomputing ecosystem

        The supercomputing ecosystem allows you to build up a flexible, high-performance, cost-effective computing platform. A large number of HPC applications and deep-learning frameworks can run on P2 ECSs.


## Notes on Using P1 ECSs<a name="section9248201684712"></a>

-   The system disk size of a P1 ECS must be greater than or equal to 15 GB. It is recommended that the system disk size be greater than 40 GB.
-   The local NVMe SSD disks attached to P1 ECSs are dedicated for services that have strict requirements on storage I/O performance, such as deep learning training and HPC. Local disks are attached to the ECSs with specified flavors and cannot be separately bought. In addition, you are not allowed to detach a local disk and attach it to another ECS.

    > ![](public_sys-resources/icon-note.gif) **NOTE:** 

    > Data may be lost on the local NVMe SSD disks attached to P1 ECSs due to a fault, for example, due to a disk or host fault. Therefore, you are suggested to store only temporary data in local NVMe SSD disks. If you store important data in such a disk, securely back up the data.

-   After a P1 ECS is created, you must install the NVIDIA driver for computing acceleration. For details, see section [Installing the NVIDIA GPU Driver and CUDA Toolkit on a P1 ECS](installing-the-nvidia-gpu-driver-and-cuda-toolkit-on-a-p1-ecs.md).
-   P1 ECSs do not support specifications modification.
-   P1 ECSs support the following OSs:
    -   Debian 9.0 64bit
    -   Ubuntu Server 16.04 64bit
    -   CentOS 7.4 64bit
    -   Windows Server 2012 R2 Standard 64bit
-   After you delete a P1 ECS, the data stored in local NVMe SSD disks is automatically cleared.

## Notes on Using P2 ECSs<a name="section1431211109429"></a>

-   The system disk size of a P2 ECS must be greater than or equal to 15 GB. It is recommended that the system disk size be greater than 40 GB.
-   The local NVMe SSD disks attached to P2 ECSs are dedicated for services that have strict requirements on storage I/O performance, such as deep learning training and HPC. Local disks are attached to the ECSs with specified flavors and cannot be separately bought. In addition, you are not allowed to detach a local disk and attach it to another ECS.

    > ![](public_sys-resources/icon-note.gif) **NOTE:** 

    > Data may be lost on the local NVMe SSD disks attached to P2 ECSs due to a fault, for example, due to a disk or host fault. Therefore, you are suggested to store only temporary data in local NVMe SSD disks. If you store important data in such a disk, securely back up the data.

-   If a P2 ECS is created using a private image, make sure that the NVIDIA driver has been installed during the private image creation. If not, install the driver after the P2 ECS is created for computing acceleration. For instructions about how to install the NVIDIA driver, see section [Installing the NVIDIA GPU Driver and CUDA Toolkit on a P2 ECS](installing-the-nvidia-gpu-driver-and-cuda-toolkit-on-a-p2-ecs.md).
-   P2 ECSs do not support specifications modification.
-   P2 ECSs support the following OS:
    -   Ubuntu Server 16.04 64bit
    -   EulerOS 2.2 64bit
-   After you delete a P2 ECS, the data stored in local NVMe SSD disks is automatically cleared.

