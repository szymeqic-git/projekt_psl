## Table of Contents
* [What is **SCADA**?](chapter_1.md)
* [Data Exchange in **SCADA**](chapter_2.md)
* [**SCADA** System Components](chapter_3.md)
* [**SCADA** Applications](chapter_4.md)
* [Operating Station](chapter_5.md)
* [**SCADA** Databases](chapter_7.md)
* [Sources](chapter_8.md)
* [Authors](chapter_9.md)
  
## **SCADA** and Distributed Control System
### Seperate Systems
 A **DCS** _(Distributed Control System)_ and **SCADA** are used for industrial automation to control and monitor processes; they are designed for different applications. **SCADA** is used for monitoring and basic control of geographically scattered operations, whereas **DCS** is used for exact control of complicated processes. There are many differences between them, from safety, processing times to industries where there are used.
 ![image](https://github.com/szymeqic-git/projekt_psl/assets/106694089/82d6726b-b42f-4aa3-8ccf-d8c791c17b12)

### Architecture
 **DCS** and **SCADA** systems are built following the ISA95 Purdue reference model architecture, which consists of five levels. The first level encompasses devices, actuators, and sensors on the production floor, while the second level utilizes **PLCs** and PID controllers to interface with field-level devices. In the third level, traditionally occupied by **SCADA** systems, data is funneled to support process control, asset management, historical analysis, and IT applications. **DCS** systems may include servers that can be considered part of a **SCADA** system, connecting corporate and IT systems.\ 
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
