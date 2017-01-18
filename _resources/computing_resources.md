---
title: NBCR Computing resources
layout: page
order: 4
---

#### Kivid cluster

This cluster is in production as of July 2015 and is 
used for software development and for running interactive
and batch computational jobs mainly with GPU access.

<table class="resources">
  <tr><th>Node</th><th>Specification</th></tr>
  <tr><td>Frontend</td>
      <td>Exxact Server:
      <ul>
      <li>2 16-core processors Intel(R) Xeon(R) CPU E5-2640 v3 @ 2.60GHz</li>
      <li>64GB memory</li>
      <li>50Tb disk (available via NFS mount to all nodes)</li>
      <li>10GBe interconnect</li>
      </ul>
      </td>
  </tr>
  <tr><td>9 compute nodes</td>
      <td>Exxact server:
      <ul>
      <li>32-core AMD Opteron(TM) Processor 6274 @1400 MHz</li>
      <li>32GB memory</li>
      <li>1Tb disk</li>
      <li>8 GPU GeForce TITAN</li>
      </ul>
      </td>
  </tr>
  <tr><td>2 compute nodes</td>
      <td>Exxact server:
      <ul>
      <li>32-core AMD Opteron(TM) Processor 6274 @1400 MHz </li>
      <li> memory </li>
      <li> disk </li>
      <li> GPU GeForce TITAN </li>
      </ul>
      </td>
  </tr>
  <tr><td>1GB eth network</td>
      <td>to all nodes </td>
  </tr>
  <tr><td>10GB eth network</td>
      <td>to all nodes </td>
  </tr>
</table>

<p></p>

#### Rocce cluster

This cluster is in production as of May 2010 and is 
used for software development and for running interactive
and batch computational jobs.

<table class="resources">
  <tr><th>Node</th><th>Specification</th></tr>
  <tr><td>Frontend</td>
      <td>Dell PowerEdge R410 server:
      <ul>
      <li> 32Gb memory</li>
      <li> 2 quad-core Intel XeonE5620 2.4Ghz processors</li>
      <li> 500Gb disk</li>
      </ul>
      </td>
  </tr>
  <tr><td>32 compute nodes</td>
      <td>Dell PowerEdge R410 server:
      <ul>
      <li>24GB memory </li>
      <li>2 quad-core Intel XeonE5620 2.4Ghz processors </li>
      <li>500GB disk </li>
      </ul>
      </td>
  </tr>
  <tr><td>4 virtual container nodes</td>
      <td>Dell PowerEdge R610 server:
      <ul>
      <li>64GB memory </li>
      <li>2 quad-core Intel XeonE5650 2.66 Ghz processors </li>
      <li>2TB disk </li>
      </ul>
      </td>
  </tr>
  <tr><td>8 GPU nodes</td>
      <td>Rackform iSErv R350.v2 server:
      <ul>
      <li>48GB memory </li>
      <li>dual Intel XeonX5650 6-core 2.66Ghz processors </li>
      <li>4TB disk </li>
      </ul>
      </td>
  </tr>
<!--  Dead node
  <tr><td>high memory node</td>
      <td>Rackform iServ R422 server:
      <ul> 
      <li>256 Gb memory</li>
      <li>4 Intel Xeon E7530 6-core 1.86Ghz</li>
      <li>4TB disk</li>
      </ul> 
      </td> 
  </tr>
-->
  <tr><td>3 storage servers</td>
      <td>2 Aberdeen Stirling X538:
      <ul> 
      <li>dual Intel Xeon E5530 quad core 2.4 Ghz </li>
      <li>12Gb memory </li>
      <li>48Tb disk </li>
      </ul> 
         1 SunFire x4540 server:
      <ul> 
      <li>dual 6-core AMD opteron model 2435 2.6 Ghz processors </li>
      <li>32 Gb memory </li>
      <li>48Tb disk </li>
      </ul> 
      </td> 
  </tr>
  <tr><td>6 gpu nodes</td>
      <td>Dell PowerEdge R720
       <ul>
       <li>384 Gb memory </li>
       <li>2 GPU M2075 Tesla </li>
       <li>16 CPUs </li>
       <li>150Gb disk </li>
       </ul>
       </td>
  </tr>
  <tr><td>high cpu/high memory node</td>
      <td>
      <ul>
      <li>64 Intel(R) Xeon(R) CPU E7- 8830 </li>
      <li>2 GPU C2075 Tesla </li>
      <li>1TB memory </li>
      <li>1TB disk </li>
      </ul>
      </td>
  </tr>
  <tr><td>1GB ethernet network</td> 
       <td>2 SMC TigerSTack II SMC8848M 48 port stackable switches </td>
  </tr>

  <tr><td>10GB network</td>
      <td>Myricom switch includes:
      <ul>
      <li>1 7u enclosure for Clos networks with up to 128 host ports</li>
      <li>2 center spine switch card </li>
      <li>3 line cards with 16 Myrinet-protocol front panel ports </li>
      <li>1 line card with 16 ethernet protocol front-panel ports </li>
      <li>2 SFP+ transceivers (optic for switch) </li>
      <li>4 blank line cards (cover unused slots) </li>
      <li>PCIE cards:
        <ul>
        <li>46 PCI-Express x8 NICs with single QSFP port card (for frontend</li>
        <li>memory, 32 compute, 8 gpu, 4 vm container nodes)</li>
        <li>3 PCI-Express x8 NICs with single SFP+ port card (for 3 storage servers)</li>
        </ul></li>
      <li>Arista 52-port 10GbE Switch:
        <ul>
        <li>IB cards (for Dellgpu, high cpu/high memory nodes and sten cluster)</li>
        </ul></li>
      </ul>
      </td>
  </tr>

</table>


<!--
#### Sten cluster

Cluster sten.ucsd.edu is in production as of May 2012.

This cluster hosts scientific applications that are accessible via web
services. There are no interactive logins.

Please see
[http://nbcr-222.ucsd.edu](http://nbcr-222.ucsd.edu "http://nbcr-222.ucsd.edu")


Frontend

EclipseA64 2U AMD server:

-   16-core AMD Opteron(TM) Processor 6212 @1400 MHz
-   32GB memory
-   500Gb disk
-   IB+10GBe interconnect

6 compute nodes

EclipseA64 2U AMD server with:

-   32-core AMD Opteron(TM) Processor 6274 @1400 MHz
-   64GB
-   500Gb disk
-   IB+10GB interconnect

1 compute node

EclipseA64 2U AMD server :

-   16-core AMD Opteron(TM) Processor 6212 @1400 MHz
-   32GB
-   500Gb disk
-   IB+10GBe interconnect

1 storage node

-   24 GB memory
-   16 Intel(R) Xeon(R) CPU E5620 @ 2.40GHz
-   10TB disk

1GB ethernet network

Melanox 18-port QDR switch

10GB network

Arista 52-port 10GbE Switch

(also used for some nodes on rocce cluster)

-->
