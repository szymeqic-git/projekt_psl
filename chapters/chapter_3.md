* [What is **SCADA**?](chapter_1.md)
* [Data Exchange in **SCADA**](chapter_2.md)
* [**SCADA** Applications](chapter_4.md)
* [Operating Station](chapter_5.md)
* [**SCADA** and Distributed Control System](chapter_6.md)
* [**SCADA** Databases](chapter_7.md)
* [Sources](chapter_8.md)
* [Authors](chapter_9.md)

## **SCADA** System Components


#### Remote Terminal Unit (RTU)

Remote terminal units, abbreviated as **RTUs**, establish connections with sensors and actuators within a given process and are integrated into the supervisory computer system via a network. 
**RTUs** possess inherent control capabilities and frequently adhere to the _IEC 61131-3_ standard for programming, supporting automation through methods such as:
* ladder logic
* function block diagrams
* a range of other programming languages.

In remote areas where local infrastructure is scarce or nonexistent, it is not uncommon to encounter **RTUs** that:
* rely on compact solar power systems for energy
* utilize radio, GSM, or satellite communication methods
* are built to endure harsh environmental conditions, withstanding temperatures as extreme as -40°C to +85°C, without the need for additional heating or cooling equipment.

#### Programmable logic controllers (**PLC**)

These devices, commonly referred to as ****PLC**s**, interface with sensors and actuators within industrial processes and establish connections with a central supervisory system. In the realm of factory automation, ****PLC**s** are typically equipped with high-speed links to the **SCADA** system. In remote scenarios, such as in the context of a large water treatment facility, ****PLC**s** can either directly link up with **SCADA** via:

* wireless connections
*  _(more frequently)_, employ an **RTU** to manage communication.


****PLC**s** are purpose-built for control purposes and played a pivotal role in the development of the _IEC 61131-3_ programming languages. They are often preferred for cost-effective reasons in remote installations with a significant number of input and output connections, as opposed to relying solely on an **RTU**.

#### Communication infrastructure - Radio/Modems & Sensors/Transducers & Repeaters

Radio/Modems allows for the transfer of data (usually wireless) across a large geographic area. A key component of a **SCADA** system is the ability to send and receive real-time data. Radio/modems are an efficient and reliable mode of accomplishing this feat.

* _Sensor_ is a type of transducer that can receive a signal from a physical system. It communicates information through the use of _telemetry_ (and a control system). The sensor in a **SCADA** system serves to help operators measure and collect data from a remote location.
* _Repeaters_ receive and retransmit signals. They are able to transmit signals over large distances, even with the presence of a physical obstruction.

Traditional **SCADA** systems have traditionally relied on a mix of radio and wired connections, although larger systems like those used in railways and power stations often opt for **SONET**/**SDH** technology. The remote monitoring and management aspect of a **SCADA** system is commonly referred to as _telemetry_. Some users prefer to have their **SCADA** data transmitted over their existing corporate networks or share the network with other applications. However, remnants of older, low-bandwidth protocols are still in use.

**SCADA** protocols are designed to be highly efficient and compact. Many are designed to transmit data only when the master station requests information from the **RTU**. Examples of legacy **SCADA** protocols include:

* Modbus RTU
* RP-570
* Profibus
* Conitel

While these communication protocols are specific to **SCADA** vendors, they are widely adopted and utilized, with the exception of Modbus, which has been made open by Schneider Electric. Standardized protocols such as:
* _IEC 60870-5-101_ 
* _IEC 60870-5-104_
* _IEC 61850_
* _DNP3_

are recognized by all major **SCADA** vendors. Many of these protocols have been extended to operate over TCP/IP. However, it's important to note that while conventional networking standards like TCP/IP are used, they serve fun_damentally different purposes from industrial networking.

To meet increasing security requirements, such as those outlined by the North American Electric Reliability Corporation (NERC) and critical infrastructure protection (CIP) regulations in the US, **satellite-based** communication is becoming more prevalent. This approach offers advantages such as:
* self-contained infrastructure (independent of public telephone circuits)
* built-in encryption
* tailored engineering for **SCADA** system reliability and availability.

Modern carrier-class systems provide the necessary quality of service for **SCADA** applications, whereas earlier experiences with consumer-grade **VSAT** were less satisfactory.

#### **SCADA** Supervisory Computers

In small **SCADA** systems, the master station is a single computer that communicates with controls systems and other equipment. 
In larger **SCADA** systems, this can include multiple servers, software applications, remote terminal units (**RTUs**), and programmable logic circuits (****PLC**s**). This forms the central nucleus of the **SCADA** system, responsible for both gathering data from the industrial process and dispatching control instructions to the connected field devices. It encompasses:

* computer hardware and software that manages communication with the field connection controllers -  **RTUs** and ****PLC**s**
*  the **HMI** software running on operator workstations.

In smaller-scale **SCADA** setups, the supervisory computer may consist of a single PC, in which case the **HMI** is integrated into this same computer.
Conversely, larger **SCADA** systems often feature:
* a master station with multiple ****HMI**s** hosted on client computers
* numerous servers for data collection
* distributed software applications
* contingency sites for disaster recovery.
    
  To enhance system reliability, these multiple servers are frequently configured in a dual-redundant or hot-standby arrangement, ensuring continuous control and monitoring even in the event of a server malfunction or failure.

#### **SCADA** Monitoring Software

**SCADA** Monitoring Software is simply a set of data instructions that instructs the system how to interact with all of the hardware and other components. It is a way to easily monitor and control the performance of a **SCADA** system.

#### Human Machine Interface (**HMI**)

The human-machine interface (**HMI**) serves as the visual gateway for operators within the supervisory system. Its primary function is to convey plant-related information to operators through graphical representations like:

* mimic diagrams, which provide a schematic overview of the controlled plant
* pages for logging alarms and events.

The **HMI** is closely connected to the **SCADA** supervisory computer, enabling it to:

* display real-time data
*  animate mimic diagrams
* showcase alarms
* generate trend graphs.
  
In many setups, the **HMI** serves as the primary graphical user interface for operators, responsible for:

* gathering data from external devices
* generating reports
*  managing alarms
* facilitating notifications.
  
Mimic diagrams incorporate line drawings and symbolic representations to depict various process elements. They may also incorporate digital photographs of the actual process equipment overlaid with animated symbols.
The **HMI** is the central control point for plant operations, allowing operators to issue commands using input devices such as mice, keyboards, and touch screens. 

For instance, a pump symbol can indicate whether the pump is running, and a flow meter symbol can display the current flow rate. Operators can stop the pump by clicking the mouse or touching the screen, and the **HMI** will reflect the real-time decrease in fluid flow through the pipe.

Typically, the **HMI** software package for a **SCADA** system includes a drawing tool that operators or maintenance personnel can use to customize how these data points are presented in the interface. These representations can be as straightforward as an on-screen traffic light, which mirrors the status of a real traffic light in the field, or as intricate as a multi-projector display illustrating the positions of all elevators in a skyscraper or the locations of all trains on a railway network.

#### What is Telemetry?

Telemetry represents a data acquisition method that enables: 

* remote collection
* transmission
* reporting of information.
  
This process is primarily facilitated by a _telemetry unit_ (or _telemetry system_) that communicates wirelessly, often through a software category referred to as **SCADA**. It's important to note that while wireless communication is common, telemetry can also utilize telephones and computer networks for data transfer. Telemetry monitoring allows valuable measurements to be transmitted and received from a distance. It serves as an efficient real-time solution for monitoring environmental conditions and the functionality of equipment.

The advantage of telemetry monitoring lies in its ability to provide instant access to crucial information necessary for data-driven decision-making. Thanks to the remote nature of this technology, data and measurements can be simultaneously accessed by decision-makers, operators, and engineers. 


#### Features of **SCADA** systems

While **SCADA** systems may offer specialized features tailored to various industries or applications, most systems encompass the following key functions:

 1. Data Collection: At the core of **SCADA** systems is data acquisition. Sensors collect data from the field, which is then relayed to field controllers. These controllers subsequently transmit the collected data to the **SCADA** computers.

 2. Remote Control: **SCADA** systems enable remote control by managing field actuators based on the data gathered from field sensors. This capability allows operators to make adjustments and control processes from a distance.

 3. Networked Data Communication: Effective communication is crucial in **SCADA**. Data obtained from sensors must be efficiently transmitted to **SCADA** field controllers, which, in turn, establish communication with the **SCADA** supervisory computers. Additionally, remote control commands are sent from the **SCADA** supervisory computers to actuators.

 4. Data Presentation: Human-Machine Interfaces (**HMI**s) play a pivotal role in **SCADA** systems by visually representing both current and historical data to operators. **HMI**s provide an intuitive interface for operators to interact with the system.

 5. Real-time and Historical Data: **SCADA** systems incorporate both real-time and historical data. Real-time data allows users to monitor the current state of processes, while historical data enables the tracking of performance against past trends.

 6. Alarms: **SCADA** systems include alarm functionalities that alert operators to potentially significant conditions within the system. These alarms can be customized to notify operators of process blockages, system failures, or the need for adjustments in various aspects of **SCADA** processes.

 7. Reporting: Reporting is a valuable aspect of **SCADA** system operations. It involves generating reports on system status, process performance, and customized reports tailored to specific application requirements. These reports provide insights into the functioning and efficiency of the **SCADA** system.
