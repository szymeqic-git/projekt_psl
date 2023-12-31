# **SCADA** Systems

## Table of Contents
* [What is **SCADA**?](#what-is-SCADA)
* [Data Exchange in **SCADA**](#data-exchange-in-SCADA)
* [**SCADA** System Components](#SCADA-system-components)
* [**SCADA** Applications](#SCADA-applications)
* [Operating Station](#operating-station)
* [**SCADA** and Distributed Control System](#SCADA-and-distributed-control-system)
* [**SCADA** Databases](#SCADA-databases)
* [Sources](#sources)
* [Authors](#authors)
  


## What is SCADA?

---

#### Definitions

**SCADA** is abbreviation from phrase „_Supervisory Control and Data Acquisition_”. **SCADA** system is mostly used in connection with software and hardware components, for example programmable logic controllers (**PLC**) and remote terminal units (**RTU**).

**HMI** (_Human Machine Interface_) is part of a bigger **SCADA** system, with its **PLC**, **RTU** and other functions. **HMI** is system which operators use to interact with **SCADA**, while overriding **SCADA** system implements all the processes connected with collecting, storing data and controlling hardware. **HMI** interfaces are often equipped with screens and, in perfect case, easy to use control panels and contol elements. They can use graphics and visualizations, simplifying control and interpretation of data and functions. 

#### Tasks

Tasks of **SCADA** systems:

 • Constant communication with **PLC** controller

 • Readable data visualization in real time 

 • Database control with appropriate technological informations 

 • Alarm installation control 

 • Generating technological process’ progress raports 

#### Applications

**SCADA** systems systems are especially important with _complicated, mulit-scale_ industrial installations. Ability to manage work of many components simultaneously is important, in opposite of simple **HMI** systems. **SCADA** systems nable organizations to monitor and report processes based on real time data and archive data to process and evaluate in the future. 

#### Schema

![](https://cdn.discordapp.com/attachments/982375180401770526/1150086602945724416/panel-hmi-zamontowany-na-maszynie-automatyka-webhmi-scada4.jpg)

## Data Exchange in SCADA

![](https://33333.cdn.cke-cs.com/kSW7V9NHUXugvhoQeFaf/images/d32f02a0d256a3cb3115a531a950927cc46e02269df37cbd.png)

#### System levels

 0. On the lowest level there are _executive_ and _measuring_ devices
 1. First level cosists of **PLC** controllers 
 2. Level two are supervisory computers, responsible for **HMI** and transferring information to coordinating computers
 3. Level third’s units do not have direct influence on executive devices’ work but they monitor overall production
 4. The highest level is responsible for production plan and collective data analysis


## SCADA System Components


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

These devices, commonly referred to as **PLCs**, interface with sensors and actuators within industrial processes and establish connections with a central supervisory system. In the realm of factory automation, **PLCs** are typically equipped with high-speed links to the **SCADA** system. In remote scenarios, such as in the context of a large water treatment facility, **PLCs** can either directly link up with **SCADA** via:

* wireless connections
*  _(more frequently)_, employ an **RTU** to manage communication.


**PLCs** are purpose-built for control purposes and played a pivotal role in the development of the _IEC 61131-3_ programming languages. They are often preferred for cost-effective reasons in remote installations with a significant number of input and output connections, as opposed to relying solely on an **RTU**.

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

#### SCADA Supervisory Computers

In small **SCADA** systems, the master station is a single computer that communicates with controls systems and other equipment. 
In larger **SCADA** systems, this can include multiple servers, software applications, remote terminal units (**RTUs**), and programmable logic circuits (**PLCs**). This forms the central nucleus of the **SCADA** system, responsible for both gathering data from the industrial process and dispatching control instructions to the connected field devices. It encompasses:

* computer hardware and software that manages communication with the field connection controllers -  **RTUs** and **PLCs**
*  the **HMI** software running on operator workstations.

In smaller-scale **SCADA** setups, the supervisory computer may consist of a single PC, in which case the **HMI** is integrated into this same computer.
Conversely, larger **SCADA** systems often feature:
* a master station with multiple **HMIs** hosted on client computers
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

 4. Data Presentation: Human-Machine Interfaces (**HMIs**) play a pivotal role in **SCADA** systems by visually representing both current and historical data to operators. **HMIs** provide an intuitive interface for operators to interact with the system.

 5. Real-time and Historical Data: **SCADA** systems incorporate both real-time and historical data. Real-time data allows users to monitor the current state of processes, while historical data enables the tracking of performance against past trends.

 6. Alarms: **SCADA** systems include alarm functionalities that alert operators to potentially significant conditions within the system. These alarms can be customized to notify operators of process blockages, system failures, or the need for adjustments in various aspects of **SCADA** processes.

 7. Reporting: Reporting is a valuable aspect of **SCADA** system operations. It involves generating reports on system status, process performance, and customized reports tailored to specific application requirements. These reports provide insights into the functioning and efficiency of the **SCADA** system.


## SCADA Applications
#### **SCADA** (Supervisory Control and Data Acquisition) systems are employed across various industries and industrial sectors for the purposes of monitoring, controlling, and collecting data from processes. Here are some common applications:
 1. **Industrial Process Control:** **SCADA** systems are extensively used in industrial settings to monitor and control manufacturing and production processes. They ensure that equipment and machinery operate efficiently and within specified parameters.
 2. **Utilities Management:** **SCADA** is employed in managing utility services such as water treatment, wastewater management, and power distribution. It helps optimize resource usage and maintain the quality of services.
 3. **Energy Management:** **SCADA** systems play a crucial role in monitoring and controlling energy production and distribution, including power generation plants, substations, and smart grids.
 4. **Oil and Gas Industry:** In the oil and gas sector, **SCADA** systems are used for monitoring and controlling pipelines, drilling operations, and refining processes. They aid in the safe and efficient extraction and distribution of resources.
 5. **Environmental Monitoring:** **SCADA** systems are utilized in environmental applications like air quality monitoring, weather stations, and pollution control. They help gather data for regulatory compliance and environmental protection.
 6. **Transportation and Infrastructure:** **SCADA** systems are employed in managing transportation systems, including traffic control, railway operations, and airport management. They ensure smooth and safe transportation services.
 7. **Building Automation:** In commercial and residential buildings, **SCADA** systems are used for HVAC (Heating, Ventilation, and Air Conditioning) control, lighting management, and security systems.
 8. **Water and Wastewater Management:** **SCADA** systems are vital for monitoring and controlling water treatment plants, distribution networks, and wastewater treatment facilities, ensuring the supply of clean water and proper sanitation.
 9. **Telecommunications:** **SCADA** systems help manage telecommunications infrastructure, including cell towers, ensuring network availability and performance.

## Here are a few key SCADA system applications, and their main features:
#### Asix **SCADA**:
 **User-Friendly Interface:** Asix offers a user-friendly graphical interface that allows users to quickly understand and control processes.
 
 **Real-Time Data Collection:** The application allows for real-time data collection from various devices and processes, enabling continuous monitoring and response to changes.
 
 **Integrated Diagnostic Tools:** Asix provides advanced diagnostic tools that assist in quickly identifying and resolving issues within the system.
 
 **Support for Various Communication Protocols:** It supports various communication protocols, making it easy to connect with different devices and systems.

#### Wonderware InTouch:
 **Process Visualization:** Wonderware InTouch provides advanced process visualization capabilities, enabling the creation of interactive user interfaces.
 
 **Integration with Other Systems:**  It allows integration with other systems such as databases, enabling comprehensive data management.
 
 **Scalability:** The system is scalable, allowing customization for different sizes and types of installations.
 
 **Alarm and Event Management:** It offers advanced tools for managing alarms and events, facilitating quick responses to failures and anomalies.

#### Siemens WinCC:
 **Integration with Industrial Automation Systems:** Siemens WinCC is often used in industrial automation, allowing seamless integration with industrial automation devices.
 
 **Advanced Reporting Features:**  It offers advanced reporting and data analysis tools, making data-driven decision-making easier.
 
 **Security and Availability:** It ensures a high level of system security and availability, crucial in critical industrial applications.
 
 **Support for Distributed Systems:** It can handle distributed **SCADA** systems, which is useful for large and complex installations.

## Operating Station
 It is a device that enables the operator to track the technological process and influence its course (operator station called is sometimes a visualization station)
Destiny:
It is to enable the operator to contact the automation system installed on object
Role:
Should perform specific tasks abbreviated as MMI (known as **HMI**) and **SCADA**
 Functions:
 1. Process flow control (automatically or by operator)
 2. Visualization of the automated process technological (industrial)
 3. Possibility to exchange data with:
-company IT system
-spreadsheets
-databases
### Features of the visualization system
 - open
 - flexible
 - network
 - localizable
 - scalable (possibility of easy expansion)
 - updateable
### Visualization system tasks
**The visualization, control, and process monitoring system installed on the facility should provide:
Communication with automation equipment (e.g., **PLC** controllers) and ensure reliable operation.**
 1. Real-time process visualization (graphical representation of the process).
 2. Intervention in the process by authorized personnel.
 3. Comprehensive analysis of selected process parameters.
 4. Data archiving and presentation of current data (trends) and reporting (daily and periodic).
 5. Generation of informative, warning, and alarm messages.
 6. Data exchange with other applications (e.g., spreadsheets and databases).
 7. Scalability (i.e., the ability to expand) of the control system.

## SCADA and Distributed Control System
### Seperate Systems
 A **DCS** _(Distributed Control System)_ and **SCADA** are used for industrial automation to control and monitor processes; they are designed for different applications. **SCADA** is used for monitoring and basic control of geographically scattered operations, whereas **DCS** is used for exact control of complicated processes. There are many differences between them, from safety, processing times to industries where there are used.
 ![image](https://github.com/szymeqic-git/projekt_psl/assets/106694089/82d6726b-b42f-4aa3-8ccf-d8c791c17b12)

### Architecture
 **DCS** and **SCADA** systems are built following the ISA95 Purdue reference model architecture, which consists of five levels. The first level encompasses devices, actuators, and sensors on the production floor, while the second level utilizes **PLCs** and PID controllers to interface with field-level devices. In the third level, traditionally occupied by **SCADA** systems, data is funneled to support process control, asset management, historical analysis, and IT applications. **DCS** systems may include servers that can be considered part of a **SCADA** system, connecting corporate and IT systems.
![image](https://github.com/szymeqic-git/projekt_psl/assets/106694089/bcb8823a-c7eb-420d-82c8-1bb4253631ff)

 Modern **DCS** and **SCADA** systems encompass various software and hardware components located in the first and second levels of manufacturing control. These systems serve as a crucial bridge for digitalization, facilitating the seamless flow of information from the plant floor to the boardroom, integrating all five levels of the automation pyramid.
 Today, **SCADA** and **DCS** are very similar. **DCS** is used on large continuous process plants where high reliability and security is important, and the control room is not geographically remote.

### Digital transformation
 Both **DCS** (_Distributed Control Systems_) and **SCADA** (_Supervisory Control and Data Acquisition_) systems are undergoing transformations aligned with the broader digital transformation trends, including the Industrial Internet of Things (**IIoT**). This transformation aims to enhance industrial automation capabilities and deliver greater value to process manufacturers.
End users are presenting new challenges, pushing vendors to rethink operational technology (OT) automation systems by incorporating Commercial Off-The-Shelf (COTS) hardware and software. They seek automation systems that outperform current **DCSs** in terms of reliability, security, and overall user value. Additionally, end users are looking for systems that allow them to preserve their control strategies when transitioning to upgraded or new systems. Modularized hardware components and decoupled software from hardware and I/O are also desired to facilitate incremental upgrades and execution flexibility within the system.

### Expansion of **SCADA**
 **SCADA** systems have evolved through four generations:

 * First generation ("Monolithic"):\
 Early **SCADA** systems relied on large minicomputers and operated independently with no connectivity to other systems. Communication protocols were proprietary, and redundancy was achieved through backup mainframe systems.
 ![image](https://github.com/szymeqic-git/projekt_psl/assets/106694089/7252c3c8-e11a-42a6-9da1-a458df9a85f0)

 * Second generation ("Distributed"):\
 **SCADA** information and command processing became distributed across multiple stations connected through a LAN. Each station had specific tasks, reducing costs compared to the first generation. Network protocols were still proprietary, and security was often overlooked.\
![image](https://github.com/szymeqic-git/projekt_psl/assets/106694089/a67ae0ff-71e7-4c19-a97e-051024f712d9)

 * Third generation ("Networked"):\
 Similar to distributed architecture, **SCADA** systems were connected through communication protocols, often spanning multiple LAN networks. This allowed for cost-effective solutions in large-scale systems.
![image](https://github.com/szymeqic-git/projekt_psl/assets/106694089/b34f1920-d1ed-4bf3-a1a8-4d4aed3dcf5f)


 * Fourth generation ("Web-based"):\
 The growth of the internet led to **SCADA** systems implementing web technologies, enabling users to access data, exchange information, and control processes from anywhere in the world through web socket connections. Web **SCADA** systems use internet browsers like Google Chrome and Mozilla Firefox as graphical user interfaces, simplifying client-side installation and facilitating access from various platforms, including:

* servers
*  PCs
* laptops
*  tablets
* and mobile phones.




## SCADA Databases
Automation systems often require efficient data storage and retrieval. Production data, including machine **OEE** (_Overall equipment effectiveness_), operator log-ins, product and password management, and historical machine information, is typically managed through interactions with a database, which essentially is an organised data collection. This data is stored for easy categorisation and future access and is designed in away to create meaningful correlations.

### Types of databases

**SCADA** systems often are separated into multiple databases each with its specific purpose. The most common type of database in **SCADA** systems is a history database. The purpose of these databases is to provide a solution for real time data logging for the observed systems. They are simple relational databases consisting of a timestamp, measured values and tags regarding what category the machine belongs to.

There are several other database types used in **SCADA** systems, but what kind of databases are used mostly depends on what is crucial for the particular system. One more popular type is specifically for events. Some systems use a database containing logs of all registered events. Another common database type would be a configuration database of the system, containing all the information related to how the system was set up. **SCADA** systems don’t have to be split into multiple databases but it can be seen in various solutions.

### Structure

Most **SCADA** systems use databases based on **SQL**. This very advantageous over self built repositories. **SQL** is a very common language used in the field of databases making them easy to expand and integrate with other software used for maintenance of **SCADA** systems. Although databases for **SCADA** systems are usually structured relationally, it is not uncommon to see other data structures.
Databases in the general context can be categorised based on content ( text, images or file types) or application area ( production or maintenance). A different way to categorise databases is according to their data structure.

#### Here are some common database structure types:
* **Relational Database:** Organises data in rows and columns, with each row having a unique primary key. Examples include Access, MySQL, and SQL Server.
* **Object-Oriented Database (OODB):** Stores data in objects containing both data and procedures. Examples include GemFire and Versant.
* **Object-Relational Database:** Combines elements of both relational and object-oriented databases. Examples include DB2, Oracle, and Visual FoxPro.
* **Multidimensional Database:** Stores data in dimensions, allowing for more than two dimensions and facilitating flexible data access. Examples include Oracle Express.

When designing a database, it's crucial to:

* determine its purpose
* design tables or files for each subject
* establish records and fields
* define relationships
* ensure efficient data management
  
## Sources: 

* [copadata.com](https://www.copadata.com/pl/product/zenon-software-platform-platforma-programowa-firmy-copa-data/wizualizacja-kontrola/co-to-jest-SCADA/)
* [iautomatyka.pl](https://iautomatyka.pl/co-to-jest-SCADA-i-co-daje-wizualizacja-procesow-przemyslowych/)
* [**SCADA** wikipedia.pl](https://pl.wikipedia.org/wiki/SCADA)
* [htt.io](https://htt.io/resources/SCADA-basics/)
* [techtarget.com](https://www.techtarget.com/whatis/definition/SCADA-supervisory-control-and-data-acquisition)
* [tutorialspoint.com](https://www.tutorialspoint.com/difference-between-dcs-and-SCADA)
* [dcs wikipedia.com](https://en.wikipedia.org/wiki/Distributed_control_system)
* [yokogawa.com](https://www.yokogawa.com/eu/library/resources/white-papers/what-are-the-roles-of-dcs-and-SCADA-in-digital-transformation/)
* [automation.com](https://www.automation.com/en-us/articles/september-2021/roles-dcs-SCADA-digital-transformation)
* [Lamb, Frank. 2013. “Software.” Chap. 6 in Industrial Automation: Hands-On. 1st ed. New York: McGraw-Hill Education.](https://www-1accessengineeringlibrary-1com-1000022uo0007.han.bg.pg.edu.pl/content/book/9780071816458/chapter/chapter6)
* [laquis**SCADA**.com](https://laquisSCADA.com/blogger/database-how-to-create-a-database/)
* [d2000.ipesoft.com](https://d2000.ipesoft.com/blog/databases-in-**SCADA**-and-mes-systems/)
* [tesla**SCADA**.com](https://teslaSCADA.com/HTML/databases2.html)
* [electrical-engineering-portal.com](https://electrical-engineering-portal.com/three-generations-of-SCADA-system-architectures)

## Authors:
Agnieszka Stromska 188560\
Oliwer Losvik 188629\
Jakub Kabat 191339\
Miłosz Smolarczyk 189008\
Szymon Kowalski 188795\
Jakub Siciarek 188642\
Bartosz Krajewski 189655\
Marcel Krużycki 188734
