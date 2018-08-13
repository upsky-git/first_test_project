# Disk-intensive ECSs<a name="EN-US_TOPIC_0035470099"></a>

## Overview<a name="section28296694191148"></a>

D1 ECSs are developed based on the XEN virtualization platform, use local storage, and provide high network performance. They are designed for applications requiring sequential read/write on ultra-large datasets in local storage \(such as distributed Hadoop computing\) as well as large-scale parallel data processing and log processing.

Compared with D1 ECSs, D2 ECSs are developed based on KVM virtualization, use local storage, and provide high storage performance and intranet bandwidth. They are designed for distributed Hadoop computing, large data warehouse, distributed file system, data processing, and log processing.

## Specifications<a name="section31415995191246"></a>

**Table 1** D1 ECS specifications

<a name="table59257344174423"></a><table><thead align="left"><tr id="row67000459174423"><th class="cellrowborder" valign="top" width="9.24%" id="mcps1.2.8.1.1"><p id="p25123811163327"><a name="p25123811163327"></a><a name="p25123811163327"></a>ECS Type</p>
</th>
<th class="cellrowborder" valign="top" width="11.379999999999999%" id="mcps1.2.8.1.2"><p id="p21762790163327"><a name="p21762790163327"></a><a name="p21762790163327"></a>vCPUs</p>
</th>
<th class="cellrowborder" valign="top" width="13.26%" id="mcps1.2.8.1.3"><p id="p17955537163327"><a name="p17955537163327"></a><a name="p17955537163327"></a>Memory (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="10.870000000000001%" id="mcps1.2.8.1.4"><p id="p45112397163327"><a name="p45112397163327"></a><a name="p45112397163327"></a>Flavor</p>
</th>
<th class="cellrowborder" valign="top" width="19.830000000000002%" id="mcps1.2.8.1.5"><p id="p75344124810"><a name="p75344124810"></a><a name="p75344124810"></a>Virtualization Type</p>
</th>
<th class="cellrowborder" valign="top" width="13.38%" id="mcps1.2.8.1.6"><p id="p4272187174423"><a name="p4272187174423"></a><a name="p4272187174423"></a>Local Disks (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="22.040000000000003%" id="mcps1.2.8.1.7"><p id="p15774111519558"><a name="p15774111519558"></a><a name="p15774111519558"></a>Hardware</p>
</th>
</tr>
</thead>
<tbody><tr id="row27416694174423"><td class="cellrowborder" rowspan="4" valign="top" width="9.24%" headers="mcps1.2.8.1.1 "><p id="p56951725174434"><a name="p56951725174434"></a><a name="p56951725174434"></a>D1</p>
</td>
<td class="cellrowborder" valign="top" width="11.379999999999999%" headers="mcps1.2.8.1.2 "><p id="p49686988174434"><a name="p49686988174434"></a><a name="p49686988174434"></a>4</p>
</td>
<td class="cellrowborder" valign="top" width="13.26%" headers="mcps1.2.8.1.3 "><p id="p65223080174434"><a name="p65223080174434"></a><a name="p65223080174434"></a>32</p>
</td>
<td class="cellrowborder" valign="top" width="10.870000000000001%" headers="mcps1.2.8.1.4 "><p id="p48578088174434"><a name="p48578088174434"></a><a name="p48578088174434"></a>d1.xlarge</p>
</td>
<td class="cellrowborder" valign="top" width="19.830000000000002%" headers="mcps1.2.8.1.5 "><p id="p45354113482"><a name="p45354113482"></a><a name="p45354113482"></a>XEN</p>
</td>
<td class="cellrowborder" valign="top" width="13.38%" headers="mcps1.2.8.1.6 "><p id="p10096623174423"><a name="p10096623174423"></a><a name="p10096623174423"></a>3 x 1800</p>
</td>
<td class="cellrowborder" rowspan="4" valign="top" width="22.040000000000003%" headers="mcps1.2.8.1.7 "><a name="ul188331858125514"></a><a name="ul188331858125514"></a><ul id="ul188331858125514"><li id="li34276251752"><a name="li34276251752"></a><a name="li34276251752"></a>V3 series<p id="p47386261054"><a name="p47386261054"></a><a name="p47386261054"></a>CPU: Intel&reg; Xeon&reg; Processor E5-2690 v3</p>
<p id="p4734532185814"><a name="p4734532185814"></a><a name="p4734532185814"></a>Memory: 12 x 32 GB</p>
</li><li id="li618923111516"><a name="li618923111516"></a><a name="li618923111516"></a>V4 series<p id="p92718328513"><a name="p92718328513"></a><a name="p92718328513"></a>CPU: Intel&reg; Xeon&reg; Processor E5-2690 v4</p>
<p id="p18448358314"><a name="p18448358314"></a><a name="p18448358314"></a>Memory: 16 x 32 GB</p>
</li></ul>
</td>
</tr>
<tr id="row45572254174423"><td class="cellrowborder" valign="top" headers="mcps1.2.8.1.1 "><p id="p47054939174434"><a name="p47054939174434"></a><a name="p47054939174434"></a>8</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.2 "><p id="p53353701174434"><a name="p53353701174434"></a><a name="p53353701174434"></a>64</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.3 "><p id="p26682544174434"><a name="p26682544174434"></a><a name="p26682544174434"></a>d1.2xlarge</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.4 "><p id="p749214715498"><a name="p749214715498"></a><a name="p749214715498"></a>XEN</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.5 "><p id="p45906110174423"><a name="p45906110174423"></a><a name="p45906110174423"></a>6 x 1800</p>
</td>
</tr>
<tr id="row45340420174423"><td class="cellrowborder" valign="top" headers="mcps1.2.8.1.1 "><p id="p57113348174434"><a name="p57113348174434"></a><a name="p57113348174434"></a>16</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.2 "><p id="p62778471174434"><a name="p62778471174434"></a><a name="p62778471174434"></a>128</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.3 "><p id="p51891399174434"><a name="p51891399174434"></a><a name="p51891399174434"></a>d1.4xlarge</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.4 "><p id="p12496670495"><a name="p12496670495"></a><a name="p12496670495"></a>XEN</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.5 "><p id="p31940638174423"><a name="p31940638174423"></a><a name="p31940638174423"></a>12 x 1800</p>
</td>
</tr>
<tr id="row65058261174423"><td class="cellrowborder" valign="top" headers="mcps1.2.8.1.1 "><p id="p46539622174434"><a name="p46539622174434"></a><a name="p46539622174434"></a>36</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.2 "><p id="p11613052174434"><a name="p11613052174434"></a><a name="p11613052174434"></a>256</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.3 "><p id="p1133162174434"><a name="p1133162174434"></a><a name="p1133162174434"></a>d1.8xlarge</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.4 "><p id="p249827204913"><a name="p249827204913"></a><a name="p249827204913"></a>XEN</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.5 "><p id="p1521802174423"><a name="p1521802174423"></a><a name="p1521802174423"></a>24 x 1800</p>
</td>
</tr>
</tbody>
</table>

**Table 2** D2 ECS specifications

<a name="table47541937112515"></a><table><thead align="left"><tr id="row1775413371257"><th class="cellrowborder" valign="top" width="9.43%" id="mcps1.2.8.1.1"><p id="p17228105016252"><a name="p17228105016252"></a><a name="p17228105016252"></a>ECS Type</p>
</th>
<th class="cellrowborder" valign="top" width="11.200000000000001%" id="mcps1.2.8.1.2"><p id="p123165013254"><a name="p123165013254"></a><a name="p123165013254"></a>vCPUs</p>
</th>
<th class="cellrowborder" valign="top" width="13.26%" id="mcps1.2.8.1.3"><p id="p7236185013252"><a name="p7236185013252"></a><a name="p7236185013252"></a>Memory (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="10.86%" id="mcps1.2.8.1.4"><p id="p18237155062514"><a name="p18237155062514"></a><a name="p18237155062514"></a>Flavor</p>
</th>
<th class="cellrowborder" valign="top" width="19.830000000000002%" id="mcps1.2.8.1.5"><p id="p724035017257"><a name="p724035017257"></a><a name="p724035017257"></a>Virtualization Type</p>
</th>
<th class="cellrowborder" valign="top" width="13.56%" id="mcps1.2.8.1.6"><p id="p1624105092519"><a name="p1624105092519"></a><a name="p1624105092519"></a>Local Disks (GB)</p>
</th>
<th class="cellrowborder" valign="top" width="21.86%" id="mcps1.2.8.1.7"><p id="p9205101061511"><a name="p9205101061511"></a><a name="p9205101061511"></a>Hardware</p>
</th>
</tr>
</thead>
<tbody><tr id="row075673742516"><td class="cellrowborder" rowspan="6" valign="top" width="9.43%" headers="mcps1.2.8.1.1 "><p id="p9760548192919"><a name="p9760548192919"></a><a name="p9760548192919"></a>D2</p>
</td>
<td class="cellrowborder" valign="top" width="11.200000000000001%" headers="mcps1.2.8.1.2 "><p id="p3921123262912"><a name="p3921123262912"></a><a name="p3921123262912"></a>4</p>
</td>
<td class="cellrowborder" valign="top" width="13.26%" headers="mcps1.2.8.1.3 "><p id="p243424132914"><a name="p243424132914"></a><a name="p243424132914"></a>32</p>
</td>
<td class="cellrowborder" valign="top" width="10.86%" headers="mcps1.2.8.1.4 "><p id="p1867211213299"><a name="p1867211213299"></a><a name="p1867211213299"></a>d2.xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" width="19.830000000000002%" headers="mcps1.2.8.1.5 "><p id="p975653772517"><a name="p975653772517"></a><a name="p975653772517"></a>KVM</p>
</td>
<td class="cellrowborder" valign="top" width="13.56%" headers="mcps1.2.8.1.6 "><p id="p14756133732515"><a name="p14756133732515"></a><a name="p14756133732515"></a>2 x 1800</p>
</td>
<td class="cellrowborder" rowspan="6" valign="top" width="21.86%" headers="mcps1.2.8.1.7 "><p id="p449920318167"><a name="p449920318167"></a><a name="p449920318167"></a>CPU: Intel&reg; Xeon&reg; Gold 6151 Processor v5</p>
<p id="p676115981618"><a name="p676115981618"></a><a name="p676115981618"></a>Memory: 20 x 32 GB</p>
</td>
</tr>
<tr id="row15756537142510"><td class="cellrowborder" valign="top" headers="mcps1.2.8.1.1 "><p id="p1592183213294"><a name="p1592183213294"></a><a name="p1592183213294"></a>8</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.2 "><p id="p143494102918"><a name="p143494102918"></a><a name="p143494102918"></a>64</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.3 "><p id="p12672172110296"><a name="p12672172110296"></a><a name="p12672172110296"></a>d2.2xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.4 "><p id="p147561837182520"><a name="p147561837182520"></a><a name="p147561837182520"></a>KVM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.5 "><p id="p1275663712258"><a name="p1275663712258"></a><a name="p1275663712258"></a>4 x 1800</p>
</td>
</tr>
<tr id="row14967171717297"><td class="cellrowborder" valign="top" headers="mcps1.2.8.1.1 "><p id="p1492123262911"><a name="p1492123262911"></a><a name="p1492123262911"></a>16</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.2 "><p id="p18434144113294"><a name="p18434144113294"></a><a name="p18434144113294"></a>128</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.3 "><p id="p196727215299"><a name="p196727215299"></a><a name="p196727215299"></a>d2.4xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.4 "><p id="p10967117172915"><a name="p10967117172915"></a><a name="p10967117172915"></a>KVM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.5 "><p id="p169678175293"><a name="p169678175293"></a><a name="p169678175293"></a>8 x 1800</p>
</td>
</tr>
<tr id="row014021416298"><td class="cellrowborder" valign="top" headers="mcps1.2.8.1.1 "><p id="p1392118321294"><a name="p1392118321294"></a><a name="p1392118321294"></a>24</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.2 "><p id="p14434541142917"><a name="p14434541142917"></a><a name="p14434541142917"></a>192</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.3 "><p id="p9672921162913"><a name="p9672921162913"></a><a name="p9672921162913"></a>d2.6xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.4 "><p id="p16140151414292"><a name="p16140151414292"></a><a name="p16140151414292"></a>KVM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.5 "><p id="p181401414112911"><a name="p181401414112911"></a><a name="p181401414112911"></a>12 x 1800</p>
</td>
</tr>
<tr id="row575615372253"><td class="cellrowborder" valign="top" headers="mcps1.2.8.1.1 "><p id="p692123252911"><a name="p692123252911"></a><a name="p692123252911"></a>32</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.2 "><p id="p13434174116295"><a name="p13434174116295"></a><a name="p13434174116295"></a>256</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.3 "><p id="p1667222172917"><a name="p1667222172917"></a><a name="p1667222172917"></a>d2.8xlarge.8</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.4 "><p id="p10756133715250"><a name="p10756133715250"></a><a name="p10756133715250"></a>KVM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.5 "><p id="p1675663717258"><a name="p1675663717258"></a><a name="p1675663717258"></a>16 x 1800</p>
</td>
</tr>
<tr id="row1375619376259"><td class="cellrowborder" valign="top" headers="mcps1.2.8.1.1 "><p id="p2921153211298"><a name="p2921153211298"></a><a name="p2921153211298"></a>60</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.2 "><p id="p1343414182916"><a name="p1343414182916"></a><a name="p1343414182916"></a>540</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.3 "><p id="p7673152132917"><a name="p7673152132917"></a><a name="p7673152132917"></a>d2.15xlarge.9</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.4 "><p id="p207561237112515"><a name="p207561237112515"></a><a name="p207561237112515"></a>KVM</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.8.1.5 "><p id="p13756113742515"><a name="p13756113742515"></a><a name="p13756113742515"></a>24 x 1800</p>
</td>
</tr>
</tbody>
</table>

## Scenarios<a name="section107991967319"></a>

-   Applications

    Disk-intensive ECSs are suitable for applications that require large volumes of data to process, high I/O performance, and rapid data switching and processing.

-   Application scenarios

    Big data computing, network file systems, data processing, MapReduce, Hadoop, and data-intensive computing


## Features of D1 ECSs<a name="section26020975191220"></a>

D1 ECSs have the following features:

-   HDD-based data storage
-   Enhanced SR-IOV network performance. On D1 ECSs, SR-IOV is enabled by default, providing high PPS performance and low network jitter and latency.
-   Up to 24 local disks, 36 vCPUs, and 256 GB memory capacity

## Features of D2 ECSs<a name="section9344849161910"></a>

-   D2 ECSs use local disks to provide high sequential read/write performance and low latency, improving file read/write performance.
-   D2 ECSs provide powerful and stable computing capabilities, ensuring efficient data processing.
-   D2 ECSs with a vCPU/memory ratio of 1:8 process large volumes of data.
-   D2 ECSs provide high intranet performance, including high intranet bandwidth and packet per second \(pps\), meeting requirements for data exchange between ECSs during peak hours.
-   Each D2 ECS supports a maximum configuration of 24 local disks, 60 vCPUs, and 540 GB memory.

## Notes on Using D1 ECSs<a name="section6384580217394"></a>

-   D1 ECSs do not support NIC hot swapping.
-   D1 ECSs do not support modifying specifications.
-   D1 ECSs do not support OS reinstallation or change.
-   D1 ECSs do not support automatic recovery.
-   D1 ECSs support the following OSs:
    -   Windows Server 2016 DataCenter 64bit
    -   Windows Server 2012 Standard 64bit
    -   Windows Server 2012 DataCenter 64bit
    -   Windows Server 2012 R2 DataCenter 64bit
    -   Windows Server 2012 R2 Standard 64bit
    -   Windows Server 2012 R2 Essentials 64bit
    -   Windows Server 2008 R2 DataCenter 64bit
    -   Windows Server 2008 R2 Enterprise 64bit
    -   Windows Server 2008 WEB R2 64bit
    -   Windows Server 2008 R2 Standard 64bit
    -   Windows Server 2008 R2 SP1 Enterprise 64bit
    -   CentOS 7.3 64bit
    -   CentOS 7.2 64bit
    -   CentOS 7.1 64bit
    -   CentOS 7.0 64bit
    -   CentOS 6.8 64bit
    -   CentOS 6.7 64bit
    -   CentOS 6.6 64bit
    -   CentOS 6.5 64bit
    -   CentOS 6.4 64bit
    -   CentOS 6.3 64bit
    -   Debian 8.0 64bit
    -   Debian 8.4 64bit
    -   Debian 8.5 64bit
    -   Debian 8.6 64bit
    -   OpenSUSE 42.2 64bit
    -   Ubuntu Server 16.10 64bit
    -   Ubuntu Server 16.04 64bit
    -   SUSE Linux Enterprise Server 11 SP3 64bit
    -   SUSE Linux Enterprise Server 11 SP4 64bit
    -   SUSE Linux Enterprise Server 12 64bit
    -   SUSE Linux Enterprise Server 12 SP1 64bit
    -   SUSE Linux Enterprise Server 12 SP2 64bit
    -   RedHat Linux Enterprise 6.8 64bit
    -   RedHat Linux Enterprise 7.0 64bit
    -   RedHat Linux Enterprise 7.2 64bit
    -   RedHat Linux Enterprise 7.3 64bit
    -   Fedora 25 64bit
    -   Oracle Enterprise Linux 6.8 64bit
    -   Oracle Enterprise Linux 7.3 64bit
    -   CoreOS 1185.5.0 64bit
    -   EulerOS 2.2 64bit
-   The primary and extension NICs of a D1 ECS have specified application scenarios. For details, see [Table 3](#en-us_topic_0088142885_table47054102151351).**Table 3** Application scenarios of the NICs of a D1 ECS

    <a name="en-us_topic_0088142885_table47054102151351"></a><table><thead align="left"><tr id="en-us_topic_0088142885_row46209555151351"><th class="cellrowborder" valign="top" width="19.61%" id="mcps1.2.4.1.1"><p id="en-us_topic_0088142885_p48417657151351"><a name="en-us_topic_0088142885_p48417657151351"></a><a name="en-us_topic_0088142885_p48417657151351"></a>NIC Type</p>
</th>
<th class="cellrowborder" valign="top" width="34.089999999999996%" id="mcps1.2.4.1.2"><p id="en-us_topic_0088142885_p29516122151351"><a name="en-us_topic_0088142885_p29516122151351"></a><a name="en-us_topic_0088142885_p29516122151351"></a>Application Scenario</p>
</th>
<th class="cellrowborder" valign="top" width="46.300000000000004%" id="mcps1.2.4.1.3"><p id="en-us_topic_0088142885_p41995713151351"><a name="en-us_topic_0088142885_p41995713151351"></a><a name="en-us_topic_0088142885_p41995713151351"></a>Remarks</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0088142885_row40005691151351"><td class="cellrowborder" valign="top" width="19.61%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0088142885_p51986490151351"><a name="en-us_topic_0088142885_p51986490151351"></a><a name="en-us_topic_0088142885_p51986490151351"></a>Primary NIC</p>
</td>
<td class="cellrowborder" valign="top" width="34.089999999999996%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0088142885_p50156190151351"><a name="en-us_topic_0088142885_p50156190151351"></a><a name="en-us_topic_0088142885_p50156190151351"></a>Applies to vertical layer 3 communication.</p>
</td>
<td class="cellrowborder" valign="top" width="46.300000000000004%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0088142885_p36119590151351"><a name="en-us_topic_0088142885_p36119590151351"></a><a name="en-us_topic_0088142885_p36119590151351"></a>N/A</p>
</td>
</tr>
<tr id="en-us_topic_0088142885_row20961270151351"><td class="cellrowborder" valign="top" width="19.61%" headers="mcps1.2.4.1.1 "><p id="en-us_topic_0088142885_p24506901151351"><a name="en-us_topic_0088142885_p24506901151351"></a><a name="en-us_topic_0088142885_p24506901151351"></a>Extension NIC</p>
</td>
<td class="cellrowborder" valign="top" width="34.089999999999996%" headers="mcps1.2.4.1.2 "><p id="en-us_topic_0088142885_p38901992151351"><a name="en-us_topic_0088142885_p38901992151351"></a><a name="en-us_topic_0088142885_p38901992151351"></a>Applies to horizontal layer 2 communication.</p>
</td>
<td class="cellrowborder" valign="top" width="46.300000000000004%" headers="mcps1.2.4.1.3 "><p id="en-us_topic_0088142885_p64053627151351"><a name="en-us_topic_0088142885_p64053627151351"></a><a name="en-us_topic_0088142885_p64053627151351"></a>To improve network performance, you can set the MTU of the extension NIC to <strong id="en-us_topic_0088142885_b842352706143046"><a name="en-us_topic_0088142885_b842352706143046"></a><a name="en-us_topic_0088142885_b842352706143046"></a>8888</strong>.</p>
</td>
</tr>
</tbody>
</table>

-   D1 ECSs can use both local disks and EVS disks to store data. Use restrictions on the two types of storage media are as follows:
    -   Only an EVS disk, not a local disk, can be used as the system disk of a D1 ECS.
    -   Both an EVS disk and a local disk can be used as the data disk of a D1 ECS.
    -   A D1 ECS can be attached with up to 60 disks \(including local disks\).

        > ![](public_sys-resources/icon-note.gif) **NOTE:** 

        > An existing D1 ECS can be attached with up to 24 disks, and the total number of attached disks and NICs is suggested to be at most 25. Otherwise, disks may fail to be attached to the ECS. To attach 60 disks, enable the advanced disk function. For details, see section [Enabling Advanced Disk](enabling-advanced-disk.md).


## Notes on Using D2 ECSs<a name="section1749014919186"></a>

-   D2 ECSs support the following OSs:
    -   CentOS 6.7/6.8/7.2/7.3/7.4 64bit
    -   SUSE Enterprise Linux Server 11 SP3/SP4 64bit
    -   SUSE Enterprise Linux Server 12 SP1/SP2 64bit
    -   Red Hat Enterprise Linux 6.8/7.3 64bit
    -   Windows Server 2008 R2 Enterprise 64bit
    -   Windows Server 2012 R2 Standard 64bit
    -   Windows Server 2016 Standard 64bit
    -   Debian 8.7/9/9.0.0 64bit
    -   EulerOS 2.2 64bit
    -   Fedora 25/26 64bit
    -   OpenSUSE 42.2/42.3 64bit
-   When the physical host where a D2 ECS is deployed becomes faulty, the ECS cannot be migrated.
-   To improve network performance, you can set the NIC MTU to **8888**.
-   D2 ECSs do not support modifying specifications.
-   D2 ECSs do not support local disk snapshot or backup.
-   D2 ECSs do not support OS reinstallation or change.
-   D2 ECSs do not support automatic recovery.
-   D2 ECSs can use both local disks and EVS disks to store data. In addition, they can have EVS disks attached to provide a larger storage size. Use restrictions on the two types of storage media are as follows:
    -   Only an EVS disk, not a local disk, can be used as the system disk of a D2 ECS.
    -   Both an EVS disk and a local disk can be used as the data disk of a D2 ECS.
    -   A D2 ECS can be attached with a maximum of 60 disks \(including VBD, SCSI, and local disks\). Among the 60 disks, the local disks use 2 SCSI controllers, the maximum number of SCSI disks is 30, and the maximum number of VBD disks is 24 \(including the system disk\).

        > ![](public_sys-resources/icon-note.gif) **NOTE:** 

        > An existing D2 ECS can be attached with up to 24 disks \(not including local disks\). To attach 60 disks, enable advanced disk. For details, see section [Enabling Advanced Disk](enabling-advanced-disk.md).

    -   You are advised to use World Wide Names \(WWNs\), but not drive letters in applications to perform operations on local disks to prevent drive letter drift \(low probability\) on Linux. Take local disk attachment as an example:

        If the local disk WWN is wwn-0x50014ee2b14249f6, run the **mount /dev/disk/by-id/wwn-0x50014ee2b14249f6** command.

        > ![](public_sys-resources/icon-note.gif) **NOTE:** 

        > How can I view the local disk WWN?

        > 1.  Log in to the ECS.
        > 2.  Run the following command to view the WWN:

            **ll /dev/disk/by-id**

-   The local disk data of a D2 ECS may be lost due to some reasons, such as host machine breakdown or local disk damage. If the data reliability of your application cannot be ensured, you are strongly advised to use EVS disks to build your ECS.
-   When a D2 ECS is deleted, its local disk data is automatically deleted. Back up the data before deleting such an ECS. Deleting local disk data is time-consuming. Therefore, a D2 ECS requires a longer period of time than other ECSs for releasing resources.
-   Do not store long-term service data in local disks. Instead, back up data in a timely manner and use a high availability data architecture. Store long-term service data in EVS disks.
-   You are not allowed to buy additional local disks. The quantity and capacity of your local disks are determined according to your ECS flavor. For a D2 ECS, if additional local disks are required, buy them when creating the ECS.

