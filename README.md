Download Link: https://assignmentchef.com/product/solved-cisco-networking-wan-implementation-with-soho-configuration-parts-1-3
<br>
Along with the challenges presented in this document, you will be provided an overall site topology to work from, as well as specific device configurations (where applicable) to make your recommendations.

Suggested solutions should be comprehensive and justified in approach. Configurations of technologies should be written out to help guide the systems administrators with implementation. In some cases, you may find it necessary to implement additional cabling, which can be done by adding to the supplied topology. Any adjustments to the sites’ topology that you find necessary should be documented and supplied with your submission.

Your document will be divided up by site and solutions per site. Each area is unique in requirements but collectively will demonstrate your understanding of network routing and switching technologies. Each scenario will provide you with suggested sections within TestOut (LabSim) to use as a guide in your analysis and recommendations.

You can use this <a href="https://umuc.equella.ecollege.com/file/544a1486-4b7c-4d94-b96d-659de4f44b21/7/CMIT_350_Final_Project_Template.docx">template</a> as a guide on how to format your project. Be sure to cite your external sources using the <a href="https://umuc.equella.ecollege.com/file/544a1486-4b7c-4d94-b96d-659de4f44b21/7/IEEE.html">IEEE citation style</a>. To learn how you will be assessed on this assignment, please take a moment to review the <a href="https://umuc.equella.ecollege.com/file/544a1486-4b7c-4d94-b96d-659de4f44b21/7/CMIT350Rubric11_2015.pdf">rubric</a>.




<strong>Existing VLANs </strong>

–

Remote locations vary in terms of size and requirements. Some implementations will require current site router/switch-running configurations, which will be provided. All sites will use the following four VLANs, but you will need to configure only what is asked per site (some assumptions will be made).

<ul>

 <li>Existing VLANs, per xACME:

  <ul>

   <li>Faculty VLAN

    <ul>

     <li>used by faculty on-site for all office locations (non-instructional communications)</li>

     <li>total devices per site will vary</li>

    </ul></li>

   <li>Administrative VLAN

    <ul>

     <li>used by staff on-site for business administrative communications</li>

     <li>total devices per site will vary</li>

    </ul></li>

   <li>Academic VLAN

    <ul>

     <li>used by faculty and students for classroom labs and instructional communications</li>

     <li>total devices per site will vary</li>

    </ul></li>

   <li>Server VLAN

    <ul>

     <li>used by IT staff for all technology/management communications</li>

     <li>total devices per site will vary</li>

    </ul></li>

  </ul></li>

</ul>

The types of devices per site will be the same; however, the number of deployed devices may vary (all documented in the xAcme educational topology).

<strong>Routers Per Site:</strong>

<table width="439">

 <tbody>

  <tr>

   <td colspan="3"><strong>Cisco 2800 Series Integrated Services</strong></td>

  </tr>

  <tr>

   <td rowspan="5">Interfaces Ports Available</td>

   <td><strong>4 Fast Ethernet Interfaces(Per Router)</strong></td>

   <td><strong>2 Serial Interfaces(Per Router)</strong></td>

  </tr>

  <tr>

   <td>fa0/0</td>

   <td>s0/0/0</td>

  </tr>

  <tr>

   <td>fa0/1</td>

   <td>s0/0/1</td>

  </tr>

  <tr>

   <td>fa1/0</td>

   <td rowspan="2"></td>

  </tr>

  <tr>

   <td>fa1/1</td>

  </tr>

 </tbody>

</table>

<strong>Switches Per Site:</strong>

<table width="439">

 <tbody>

  <tr>

   <td colspan="2"><strong>Cisco Catalyst 6500 Series</strong></td>

  </tr>

  <tr>

   <td rowspan="5" width="211">Ports Available</td>

   <td><strong>96 Total Gigabit EthernetPorts Per Switch</strong></td>

  </tr>

  <tr>

   <td>Module 1 = gi0/1 – gi0/24</td>

  </tr>

  <tr>

   <td>Module 2 = gi1/1 – gi1/24</td>

  </tr>

  <tr>

   <td>Module 3 = gi2/1 – gi2/24</td>

  </tr>

  <tr>

   <td>Module 4 = gi3/1 – gi3/24</td>

  </tr>

 </tbody>

</table>

<strong><em>Note: </em></strong><em>Device type will not impact your configuration commands and implementation of ALL required technologies will use Cisco IOS commands/concepts learned in our TestOut lecture(s). Standard switchports will be configured and used as trunk OR access ports, and DCE ends should be noted when configuring serial ports per router.</em>

Click <a href="https://umuc.equella.ecollege.com/file/544a1486-4b7c-4d94-b96d-659de4f44b21/7/Configuration.zip">here</a> to download the configuration file for all of the devices. Note: one of the files in the zip file is a PacketTracer file. You can open it using the Packet Tracer program that you can download from <a href="https://umuc.equella.ecollege.com/file/544a1486-4b7c-4d94-b96d-659de4f44b21/7/PacketTracer.zip">here</a>. The use of Packet Tracer is optional.




<strong>Springfield Site Device and STP Configurations (Focus on the Springfield Site Only)</strong>

–

<strong><u>Required Implementation:</u></strong> Device hostnames, banners, secured passwords and spanning tree protocol.

<ul>

 <li><strong>Device Configurations: </strong>Implement device hostnames to match the xACME educational topology labels. Provide a template and sample configuration for the MOTD banner and login banner (wording and implementation) for one of the switches. Keep this generic, as it will be implemented on <strong>all </strong>switches in the xACME educational topology. Lastly, include the configuration steps for implementing device passwords on both console port (out-of-band communications) and VTY (Telnet/in-band communications). All passwords should be encrypted.</li>

 <li><strong>Spanning Tree Protocol (STP): </strong>Briefly explain the advantages and purpose of the STP. Administrators are having a difficult time placing switch 1 as the root. Provide a sample configuration for implementing SPT on the switches. Choose the mode you feel would be best suited for the environment and justify why. Switch 1 will need to be the root switch in the Springfield topology. Consider any security measures that can be implemented to protect the devices from bogus BPDUs.</li>

</ul>

<strong><em>Note: </em></strong><em>When approaching the spanning tree challenge, <strong>do not</strong>concern yourself with the multiple VLANs at this time. Focus simply on the default VLAN1, which is the active VLAN that all ports belong to in this topology at this time.</em>

<ul>

 <li>Please refer to the following configurations:

  <ul>

   <li>SpringfieldSw1</li>

   <li>SpringfieldSw2</li>

   <li>SpringfieldSw3</li>

   <li>SpringfieldSw4</li>

  </ul></li>

</ul>




<strong>Worchester Site Device and STP Configurations (Focus on the Worchester Site Only)</strong>

–

<strong><u>Required Implementation:</u></strong> Subnet addressing to accommodate Worchester site

<strong>Subnetting: </strong>Properly subnet addressing blocks to accommodate the site’s VLAN sizes. You <strong>will not</strong> need to implement VLANs here; rather, you will create the correct sizing to properly accommodate the devices stated per the xACME educational topology. Carefully consider the challenges faced when structuring subnets too large and/or too small during your design. The starting Worchester site addressing range is 10.20.0.0 /16 (per the xACME educational topology diagram). Formatting per subnet should follow the format below and should be clearly stated and placed within a table.

<ul>

 <li>NetID</li>

 <li>mask/CIDR values</li>

 <li>broadcast</li>

 <li>usable range</li>

 <li>No additional device configurations required to complete</li>

</ul>




<strong>Boston Site Routing Protocol, Route Summarization and Topology Improvements (Focus on the Boston Site Only)</strong>

–

<strong><u>Required Implementation:</u></strong> Implement a routing protocol to manage networks within the Boston site topology as well as default routes to exit non-Boston traffic. Summarization addresses should be stated per router in Boston’s topology. Consider redundancy upgrades as well and document per topology.

<ul>

 <li><strong>Routing Protocol: </strong>Research the different routing protocol types (distance vector/link state/hybrid) and choose a routing protocol implement (OSPF, EIGRP, RIP). Justify your selection by defining its strengths and weaknesses. Define the proper addressing block to assign per point-to-point links and implement your solution per all three routers. Routing protocol should be set up in a way to advertise all IP subnets, WAN, and LAN interfaces on a router. Be sure to protect the advertisements of the routing tables as well.</li>

 <li><strong>Summarization: </strong>Define the route summarization addresses for each Boston site router. These addresses will not be implemented on the routers, but they will be documented in your response. Each summarization address must be large enough to include all required subnets contained within the underlying site subnets.</li>

 <li><strong>Default Route: </strong>Any traffic not matching internal networks will need to be routed outward. Implement default routes on the site routers to exit this traffic.</li>

 <li><strong>Topology: </strong>Consider the potential challenges with the current Boston site topology (cabling and redundancy approach). If improvements are needed, update the topology and discuss and routing redundancy approaches you see fit.</li>

 <li>Please refer to the following configurations:

  <ul>

   <li>BostonSiteRouter1</li>

   <li>BostonSiteRouter2</li>

   <li>BostonSiteRouter3</li>

  </ul></li>

</ul>




<strong>Sacramento Site VLAN, Routing on a Stick (ROS) and DHCP Implementation (Focus on the Sacramento Site Only)</strong>

–

<strong><u>Required Implementation:</u></strong> VLANs, ROS, and DHCP implementation

<ul>

 <li><strong>VLANs: </strong>Implement the VLAN database on the Sacramento site switches. Explain the assignment of switchport modes and how to implement each. Demonstrate how to implement port security on the switchports to allow only two MAC addresses per port and shutdowns for violations. Additionally, consider proper security management of any unused ports.

  <ul>

   <li>Provide the VLAN IDs, ports with matching switchport modes, and sample configuration of port security and port management steps.</li>

  </ul></li>

 <li><strong>ROS: </strong>The site will be treated as a routing on a stick (ROS) topology. Provide a sample configuration for Sacramento fa0/0 interface to support the multiple VLANs and inter-VLAN routing.

  <ul>

   <li>To simplify configuration, please use the following addressing:

    <ul>

     <li>faculty VLAN: 10.50.0.0 /26</li>

     <li>administrative VLAN: 10.50.0.64 /26</li>

     <li>instructional VLAN: 10.50.0.128 /26</li>

     <li>server VLAN: 10.50.0.192 /26</li>

    </ul></li>

   <li><strong>DHCP: </strong>The site will need a solution to manage the deployment of IP addresses. Briefly explain the purpose of DHCP and provide implementation of the DHCP configuration for the VLANs. Be sure to include the pool name, exclude the last 10 addresses of each subnet range and configure the gateway, subnet mask, and DNS address (Sacramento fa0/0 address).</li>

   <li>Please refer to the following configurations:

    <ul>

     <li>SacramentoSw1</li>

     <li>SacramentoSw2</li>

     <li>SacramentoSw3</li>

     <li>SacramentoRouter</li>

    </ul></li>

  </ul></li>

</ul>




<strong>Los Angeles Site Management Technologies (Focus on the Los Angeles Site Only)</strong>

–

<strong><u>Required Implementation:</u></strong> Device configuration remote storage, remote management of switches, ACL implementation, and an NTP solution.

<ul>

 <li><strong>Remote IOS Storage: </strong>The site will require remote storage of the devices’ configurations. Server details are provided per your topology. You will determine the protocol to use and demonstrate how to implement the solution.</li>

 <li><strong>Remote Management of Switches:</strong>All devices will be configured to allow for remote management. You will be required to implement this solution on the switches found on the site.</li>

 <li><strong>ACL Implementation: </strong>In order to restrict and protect access to the devices, the only VLAN allowed to communicate remotely with the devices should belong to the server VLAN. Determine the type of ACL to implement and the placement of the list, and implement the solution on the site router.</li>

 <li><strong>Network Time Protocol: </strong>Implement an NTP solution on the devices found within this topology to ensure clock synchronization is accomplished. The purpose would be for accurate logging records and authentication protocols. Server details are provided per your topology.</li>

 <li>Please refer to the following configurations:

  <ul>

   <li>LosAngelesSw1</li>

   <li>LosAngelesSw2</li>

   <li>LosAngelesSw3</li>

   <li>LosAngelesRouter</li>

  </ul></li>

</ul>




<strong>xACME WAN – WAN Implementation and Secure Communications (Focus on All Site Entry Point Routers)</strong>

–

<strong><u>Required Implementation:</u></strong> WAN Implementation, device authentication, and topology suggestions.

<ul>

 <li><strong>WAN Implementation: </strong>Current WAN links are serial-based and connected over leased lines that are using the Cisco default protocol for layer 2 connectivity. Authentication is not present at this time, but the added security would be preferred. Research the available WAN protocols and suggest a solution to provide authentication between devices. Implement basic routing protocol authentication. Provide a sample implementation over serial links for your systems administrator to follow. Included in this task are device configurations for the current implementation.</li>

 <li><strong>Topology: </strong>Currently, the Los Angeles and Boston sites are connected across leased lines, and each remains as the entry point to its respective regional locations. There is growing concern over the amount of traffic both devices are handling. Review the xAMCE educational topology and make recommendations to provide some redundancy among sites, as well as to alleviate some of the bandwidth requirements placed on both devices. This may require additional lines to be leased. With your suggested improvements, update the topology as you see fit.</li>

</ul>

<strong><em>Note: </em></strong><em>Additional addressing is available if needed. Simply create the additional ranges from the provided available xACME public address range, 165.128.63.0 /26.</em>

<ul>

 <li>Please refer to the following configurations:

  <ul>

   <li>BostonSiteRouter1</li>

   <li>WorchesterRouter</li>

   <li>SpringfieldRouter</li>

   <li>SacramentoRouter</li>

   <li>LosAngelesRouter</li>

  </ul></li>

</ul>