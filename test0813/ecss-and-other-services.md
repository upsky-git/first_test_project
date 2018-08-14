# ECSs and Other Services<a name="EN-US_TOPIC_0013771111"></a>

[Figure 1](#fig14853233114016) shows the relationships between ECS and other services.

<a name="fig14853233114016"></a>
**Figure 1** Relationships between ECS and other services
![](figures/relationships-between-ecs-and-other-services.png "Relationships between ECS and other services")

-   Auto Scaling \(AS\)

    Automatically adjusts ECS service resources based on the configured AS policies. This improves resource usage and reduces resource costs.
    
    **ssh** *Username*<>**@**<>*EIP*

-   Elastic Load Balance \(ELB\)

    Automatically distributes traffic to multiple ECSs. This enhances system service and fault tolerance capabilities.

-   Elastic Volume Service \(EVS\)

    Enables you to attach EVS disks to an ECS and expand their capacity.

-   Virtual Private Cloud \(VPC\)

    Enables you to configure internal networks and change network configurations by customizing security groups, VPNs, IP address segments, and bandwidth. This simplifies network management. You can also customize the ECS access rules within a security group and between security groups to strengthen ECS security protection.

-   Image Management Service \(IMS\)

    Enables you to create ECSs using images. This improves the efficiency of ECS creation.

-   Cloud Eye

    Allows you to check the status of monitored service objects after you have obtained an ECS. This can be done without requiring additional plug-ins be installed. [Table 1](#table251255781538) lists the ECS metrics supported by Cloud Eye.

    **Table 1** ECS monitoring metrics

    <a name="table251255781538"></a><table><thead align="left"><tr id="en-us_topic_0030911465_row15175257222846"><th class="cellrowborder" valign="top" width="20.162016201620165%" id="mcps1.2.5.1.1"><p id="en-us_topic_0030911465_p21236279222846"><a name="en-us_topic_0030911465_p21236279222846"></a><a name="en-us_topic_0030911465_p21236279222846"></a>Metric</p>
</th>
<th class="cellrowborder" valign="top" width="33.31333133313332%" id="mcps1.2.5.1.2"><p id="en-us_topic_0030911465_p42417005222846"><a name="en-us_topic_0030911465_p42417005222846"></a><a name="en-us_topic_0030911465_p42417005222846"></a>Description</p>
</th>
<th class="cellrowborder" valign="top" width="26.932693269326936%" id="mcps1.2.5.1.3"><p id="en-us_topic_0030911465_p64622851222846"><a name="en-us_topic_0030911465_p64622851222846"></a><a name="en-us_topic_0030911465_p64622851222846"></a>Formula</p>
</th>
<th class="cellrowborder" valign="top" width="19.591959195919593%" id="mcps1.2.5.1.4"><p id="en-us_topic_0030911465_p67068467222846"><a name="en-us_topic_0030911465_p67068467222846"></a><a name="en-us_topic_0030911465_p67068467222846"></a>Remarks</p>
</th>
</tr>
</thead>
<tbody><tr id="en-us_topic_0030911465_row63836764222846"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p3395365222846"><a name="en-us_topic_0030911465_p3395365222846"></a><a name="en-us_topic_0030911465_p3395365222846"></a>CPU Usage</p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p6589110222846"><a name="en-us_topic_0030911465_p6589110222846"></a><a name="en-us_topic_0030911465_p6589110222846"></a>Indicates the CPU usage (%) of an ECS.</p>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p13045074222846"><a name="en-us_topic_0030911465_p13045074222846"></a><a name="en-us_topic_0030911465_p13045074222846"></a>CPU usage of an ECS/Number of CPU cores in the ECS</p>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p50018093222846"><a name="en-us_topic_0030911465_p50018093222846"></a><a name="en-us_topic_0030911465_p50018093222846"></a>N/A</p>
</td>
</tr>
<tr id="en-us_topic_0030911465_row47509658222846"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p23077113222846"><a name="en-us_topic_0030911465_p23077113222846"></a><a name="en-us_topic_0030911465_p23077113222846"></a>Memory Usage</p>
<p id="en-us_topic_0030911465_p6367428222846"><a name="en-us_topic_0030911465_p6367428222846"></a><a name="en-us_topic_0030911465_p6367428222846"></a></p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p45999697222846"><a name="en-us_topic_0030911465_p45999697222846"></a><a name="en-us_topic_0030911465_p45999697222846"></a>Indicates the memory usage (%) of an ECS.</p>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p15452979222846"><a name="en-us_topic_0030911465_p15452979222846"></a><a name="en-us_topic_0030911465_p15452979222846"></a>Used memory of an ECS/Total memory of the ECS</p>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p43731801222846"><a name="en-us_topic_0030911465_p43731801222846"></a><a name="en-us_topic_0030911465_p43731801222846"></a>This metric is unavailable if the image has no OTC Tools installed.</p>
</td>
</tr>
<tr id="en-us_topic_0030911465_row58041894222846"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p3772951222846"><a name="en-us_topic_0030911465_p3772951222846"></a><a name="en-us_topic_0030911465_p3772951222846"></a>Disk Usage</p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p37173646222846"><a name="en-us_topic_0030911465_p37173646222846"></a><a name="en-us_topic_0030911465_p37173646222846"></a>Indicates the disk usage (%) of an ECS.</p>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p22679847222846"><a name="en-us_topic_0030911465_p22679847222846"></a><a name="en-us_topic_0030911465_p22679847222846"></a>Used capacity of an ECS disk/Total capacity of the ECS disk</p>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p25128347222846"><a name="en-us_topic_0030911465_p25128347222846"></a><a name="en-us_topic_0030911465_p25128347222846"></a>This metric is unavailable if the image has no OTC Tools installed.</p>
</td>
</tr>
<tr id="en-us_topic_0030911465_row24828535222846"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p64954320222846"><a name="en-us_topic_0030911465_p64954320222846"></a><a name="en-us_topic_0030911465_p64954320222846"></a>Disks Read Rate</p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p26808602222846"><a name="en-us_topic_0030911465_p26808602222846"></a><a name="en-us_topic_0030911465_p26808602222846"></a>Indicates the number of bytes read from an ECS per second.</p>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p66019488222846"><a name="en-us_topic_0030911465_p66019488222846"></a><a name="en-us_topic_0030911465_p66019488222846"></a>Total number of bytes read from an ECS disk/Monitoring period</p>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p45978283222846"><a name="en-us_topic_0030911465_p45978283222846"></a><a name="en-us_topic_0030911465_p45978283222846"></a>byte_out = (rd_bytes - last_rd_bytes) /Time difference</p>
</td>
</tr>
<tr id="en-us_topic_0030911465_row11151367222846"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p30845571222846"><a name="en-us_topic_0030911465_p30845571222846"></a><a name="en-us_topic_0030911465_p30845571222846"></a>Disks Write Rate</p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p15463290222846"><a name="en-us_topic_0030911465_p15463290222846"></a><a name="en-us_topic_0030911465_p15463290222846"></a>Indicates the number of bytes written to an ECS per second.</p>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p53157119222846"><a name="en-us_topic_0030911465_p53157119222846"></a><a name="en-us_topic_0030911465_p53157119222846"></a>Total number of bytes written to an ECS disk/Monitoring period</p>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p10759388222846"><a name="en-us_topic_0030911465_p10759388222846"></a><a name="en-us_topic_0030911465_p10759388222846"></a>N/A</p>
</td>
</tr>
<tr id="en-us_topic_0030911465_row29725634222846"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p58966153222846"><a name="en-us_topic_0030911465_p58966153222846"></a><a name="en-us_topic_0030911465_p58966153222846"></a>Disks Read Requests</p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p11529080222846"><a name="en-us_topic_0030911465_p11529080222846"></a><a name="en-us_topic_0030911465_p11529080222846"></a>Indicates the number of read requests sent to an ECS per second.</p>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p10609393222846"><a name="en-us_topic_0030911465_p10609393222846"></a><a name="en-us_topic_0030911465_p10609393222846"></a>Total number of read requests sent to an ECS disk/Monitoring period</p>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p54054474222846"><a name="en-us_topic_0030911465_p54054474222846"></a><a name="en-us_topic_0030911465_p54054474222846"></a>req_out = (rd_req - last_rd_req)/Time difference</p>
</td>
</tr>
<tr id="en-us_topic_0030911465_row16728218222846"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p12808390222846"><a name="en-us_topic_0030911465_p12808390222846"></a><a name="en-us_topic_0030911465_p12808390222846"></a>Disks Write Requests</p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p30846695222846"><a name="en-us_topic_0030911465_p30846695222846"></a><a name="en-us_topic_0030911465_p30846695222846"></a>Indicates the number of write requests sent to an ECS per second.</p>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p51947303222846"><a name="en-us_topic_0030911465_p51947303222846"></a><a name="en-us_topic_0030911465_p51947303222846"></a>Total number of write requests sent to an ECS disk/Monitoring period</p>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p46982038222846"><a name="en-us_topic_0030911465_p46982038222846"></a><a name="en-us_topic_0030911465_p46982038222846"></a>req_in = (wr_req - last_wr_req)/Time difference</p>
</td>
</tr>
<tr id="en-us_topic_0030911465_row20185161222846"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p24385382222846"><a name="en-us_topic_0030911465_p24385382222846"></a><a name="en-us_topic_0030911465_p24385382222846"></a>Inband Incoming Rate</p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p29058915222846"><a name="en-us_topic_0030911465_p29058915222846"></a><a name="en-us_topic_0030911465_p29058915222846"></a>Indicates the number of incoming bytes on an ECS per second.</p>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p66369310222846"><a name="en-us_topic_0030911465_p66369310222846"></a><a name="en-us_topic_0030911465_p66369310222846"></a>Total number of inband incoming bytes on an ECS/Monitoring period</p>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p7205036222846"><a name="en-us_topic_0030911465_p7205036222846"></a><a name="en-us_topic_0030911465_p7205036222846"></a>N/A</p>
</td>
</tr>
<tr id="en-us_topic_0030911465_row64845332222846"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p17980571222846"><a name="en-us_topic_0030911465_p17980571222846"></a><a name="en-us_topic_0030911465_p17980571222846"></a>Inband Outgoing Rate</p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p47140109222846"><a name="en-us_topic_0030911465_p47140109222846"></a><a name="en-us_topic_0030911465_p47140109222846"></a>Indicates the number of outgoing bytes on an ECS per second.</p>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p48614360222846"><a name="en-us_topic_0030911465_p48614360222846"></a><a name="en-us_topic_0030911465_p48614360222846"></a>Total number of inband outgoing bytes on an ECS/Monitoring period</p>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p45449088222846"><a name="en-us_topic_0030911465_p45449088222846"></a><a name="en-us_topic_0030911465_p45449088222846"></a>N/A</p>
</td>
</tr>
<tr id="en-us_topic_0030911465_row22492419121215"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p1105187121215"><a name="en-us_topic_0030911465_p1105187121215"></a><a name="en-us_topic_0030911465_p1105187121215"></a>Outband Incoming Rate</p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p22411285121215"><a name="en-us_topic_0030911465_p22411285121215"></a><a name="en-us_topic_0030911465_p22411285121215"></a>Indicates the number of incoming bytes on an ECS per second at the virtualization layer.</p>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p4924384121215"><a name="en-us_topic_0030911465_p4924384121215"></a><a name="en-us_topic_0030911465_p4924384121215"></a>Total number of outband incoming bytes on an ECS/Monitoring period</p>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p63330824121215"><a name="en-us_topic_0030911465_p63330824121215"></a><a name="en-us_topic_0030911465_p63330824121215"></a>This metric is unavailable if SR-IOV is enabled.</p>
</td>
</tr>
<tr id="en-us_topic_0030911465_row62680097121215"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p27249966121215"><a name="en-us_topic_0030911465_p27249966121215"></a><a name="en-us_topic_0030911465_p27249966121215"></a>Outband Outgoing Rate</p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p59763627121215"><a name="en-us_topic_0030911465_p59763627121215"></a><a name="en-us_topic_0030911465_p59763627121215"></a>Indicates the number of outgoing bytes on an ECS per second at the virtualization layer.</p>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p59175014121215"><a name="en-us_topic_0030911465_p59175014121215"></a><a name="en-us_topic_0030911465_p59175014121215"></a>Total number of outband outgoing bytes on an ECS/Monitoring period</p>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p28446836121215"><a name="en-us_topic_0030911465_p28446836121215"></a><a name="en-us_topic_0030911465_p28446836121215"></a>This metric is unavailable if SR-IOV is enabled.</p>
</td>
</tr>
<tr id="en-us_topic_0030911465_row2605901916337"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p3320458516337"><a name="en-us_topic_0030911465_p3320458516337"></a><a name="en-us_topic_0030911465_p3320458516337"></a>System Status Check Failed</p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p521685316337"><a name="en-us_topic_0030911465_p521685316337"></a><a name="en-us_topic_0030911465_p521685316337"></a>Check the status of the cloud platform for running ECSs. The check result is <strong id="en-us_topic_0030911465_b84235270623397"><a name="en-us_topic_0030911465_b84235270623397"></a><a name="en-us_topic_0030911465_b84235270623397"></a>0</strong>&nbsp;or&nbsp;<strong id="en-us_topic_0030911465_b842352706233910"><a name="en-us_topic_0030911465_b842352706233910"></a><a name="en-us_topic_0030911465_b842352706233910"></a>1</strong>.</p>
<a name="en-us_topic_0030911465_ul13348182820394"></a><a name="en-us_topic_0030911465_ul13348182820394"></a><ul id="en-us_topic_0030911465_ul13348182820394"><li id="en-us_topic_0030911465_li1761573816122"><a name="en-us_topic_0030911465_li1761573816122"></a><a name="en-us_topic_0030911465_li1761573816122"></a><strong id="en-us_topic_0030911465_b171676334619247"><a name="en-us_topic_0030911465_b171676334619247"></a><a name="en-us_topic_0030911465_b171676334619247"></a>0</strong>: The system is running properly. All check items are normal.</li><li id="en-us_topic_0030911465_li635562817397"><a name="en-us_topic_0030911465_li635562817397"></a><a name="en-us_topic_0030911465_li635562817397"></a><strong id="en-us_topic_0030911465_b1087511831192613"><a name="en-us_topic_0030911465_b1087511831192613"></a><a name="en-us_topic_0030911465_b1087511831192613"></a>1</strong>: The system is not running properly. At least one check item failed.</li></ul>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p5086914416723"><a name="en-us_topic_0030911465_p5086914416723"></a><a name="en-us_topic_0030911465_p5086914416723"></a>The system periodically checks the status and returns check results using value <strong id="en-us_topic_0030911465_b842352706192323"><a name="en-us_topic_0030911465_b842352706192323"></a><a name="en-us_topic_0030911465_b842352706192323"></a>0</strong>&nbsp;or&nbsp;<strong id="en-us_topic_0030911465_b842352706192327"><a name="en-us_topic_0030911465_b842352706192327"></a><a name="en-us_topic_0030911465_b842352706192327"></a>1</strong>.</p>
<a name="en-us_topic_0030911465_ul3386195716122"></a><a name="en-us_topic_0030911465_ul3386195716122"></a><ul id="en-us_topic_0030911465_ul3386195716122"><li id="en-us_topic_0030911465_li1539445316122"><a name="en-us_topic_0030911465_li1539445316122"></a><a name="en-us_topic_0030911465_li1539445316122"></a>If the detected fault does not affect ECS functions, certain management operations performed on the ECS, such as starting, stopping, or specifications modifications, may be affected.</li><li id="en-us_topic_0030911465_li15881204014392"><a name="en-us_topic_0030911465_li15881204014392"></a><a name="en-us_topic_0030911465_li15881204014392"></a>If the detected fault affects ECS functions, such as a host power supply failure, the system will recover the ECS as soon as possible. </li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p225190516337"><a name="en-us_topic_0030911465_p225190516337"></a><a name="en-us_topic_0030911465_p225190516337"></a>When the power source of the physical host fails or the hardware/software becomes faulty, the check result is <strong id="en-us_topic_0030911465_b842352706201616"><a name="en-us_topic_0030911465_b842352706201616"></a><a name="en-us_topic_0030911465_b842352706201616"></a>1</strong>.</p>
</td>
</tr>
<tr id="en-us_topic_0030911465_row44572200141717"><td class="cellrowborder" valign="top" width="20.162016201620165%" headers="mcps1.2.5.1.1 "><p id="en-us_topic_0030911465_p65605483141717"><a name="en-us_topic_0030911465_p65605483141717"></a><a name="en-us_topic_0030911465_p65605483141717"></a>InfiniBand NIC status</p>
</td>
<td class="cellrowborder" valign="top" width="33.31333133313332%" headers="mcps1.2.5.1.2 "><p id="en-us_topic_0030911465_p12443932141717"><a name="en-us_topic_0030911465_p12443932141717"></a><a name="en-us_topic_0030911465_p12443932141717"></a>This metric is used to monitor the status of an InfiniBand NIC on an H2 ECS to ensure proper InfiniBand NIC running.</p>
<div class="note" id="en-us_topic_0030911465_note14324438161653"><a name="en-us_topic_0030911465_note14324438161653"></a><a name="en-us_topic_0030911465_note14324438161653"></a><span class="notetitle"> NOTE: </span><div class="notebody"><p id="en-us_topic_0030911465_p61811084161653"><a name="en-us_topic_0030911465_p61811084161653"></a><a name="en-us_topic_0030911465_p61811084161653"></a>Only Mellanox EDR 100 GB single-port InfiniBand NICs are supported.</p>
</div></div>
</td>
<td class="cellrowborder" valign="top" width="26.932693269326936%" headers="mcps1.2.5.1.3 "><p id="en-us_topic_0030911465_p1325610141717"><a name="en-us_topic_0030911465_p1325610141717"></a><a name="en-us_topic_0030911465_p1325610141717"></a>The system periodically checks the status and returns check results using value <strong id="en-us_topic_0030911465_b842352706192323_1"><a name="en-us_topic_0030911465_b842352706192323_1"></a><a name="en-us_topic_0030911465_b842352706192323_1"></a>0</strong>&nbsp;or&nbsp;<strong id="en-us_topic_0030911465_b842352706192327_1"><a name="en-us_topic_0030911465_b842352706192327_1"></a><a name="en-us_topic_0030911465_b842352706192327_1"></a>1</strong>.</p>
<a name="en-us_topic_0030911465_ul28823487141959"></a><a name="en-us_topic_0030911465_ul28823487141959"></a><ul id="en-us_topic_0030911465_ul28823487141959"><li id="en-us_topic_0030911465_li58084791141959"><a name="en-us_topic_0030911465_li58084791141959"></a><a name="en-us_topic_0030911465_li58084791141959"></a><strong id="en-us_topic_0030911465_b171676334619247_1"><a name="en-us_topic_0030911465_b171676334619247_1"></a><a name="en-us_topic_0030911465_b171676334619247_1"></a>0</strong>: The system is running properly. That is, the InfiniBand NIC is functional.</li><li id="en-us_topic_0030911465_li53001078141959"><a name="en-us_topic_0030911465_li53001078141959"></a><a name="en-us_topic_0030911465_li53001078141959"></a><strong id="en-us_topic_0030911465_b1087511831192613_1"><a name="en-us_topic_0030911465_b1087511831192613_1"></a><a name="en-us_topic_0030911465_b1087511831192613_1"></a>1</strong>: The system is not running properly. That is, the InfiniBand NIC malfunctions.</li></ul>
</td>
<td class="cellrowborder" valign="top" width="19.591959195919593%" headers="mcps1.2.5.1.4 "><p id="en-us_topic_0030911465_p40265596141717"><a name="en-us_topic_0030911465_p40265596141717"></a><a name="en-us_topic_0030911465_p40265596141717"></a>When the physical NIC corresponding to a virtual NIC becomes faulty, for example, the network cable is not securely connected to the NIC, the switch or adapter is incompatible with the InifiniBand NIC, or the NIC is disabled, the returned value is <strong id="en-us_topic_0030911465_b842352706174428"><a name="en-us_topic_0030911465_b842352706174428"></a><a name="en-us_topic_0030911465_b842352706174428"></a>1</strong>.</p>
</td>
</tr>
</tbody>
</table>

-   Key Management Service \(KMS\)

    The encryption feature relies on KMS. You can use an encrypted image or EVS disks when creating an ECS. In such a case, you are required to use the key provided by KMS to improve data security.

-   Cloud Trace Service \(CTS\)

    Allows you to record ECS-related operations for later query, audit, and backtrack.

-   Cloud Server Backup Service \(CSBS\)

    Protects ECS backups. CSBS backs up all EVS disks of an ECS, including the system disk and data disks, and uses the backup to restore the ECS.


