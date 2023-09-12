## 1\. Wprowadzenie

---

#### Definicje

**SCADA** jest skrótem od frazy „_Supervisory Control and Data Acquisition_”, oznaczającej kontrolę nadzorczą i pozyskiwanie danych. System **SCADA** jest zwykle stosowany w połączeniu z oprogramowaniem i elementami sprzętowymi, na przykład programowalnymi sterownikami logicznymi (**PLC**) i zdalnymi jednostkami terminali (**RTU** _ang. Remote Terminal Unit_).

**HMI** (_ang. Human Machine Interface_) jest częścią większego systemu **SCADA**, razem z jego **PLC**, **RTU** i innymi funkcjami. Dokładniej HMI to system, którego operatorzy używają do interakcji ze **SCADA**, natomiast nadrzędny system **SCADA** realizuje wszystkie procesy związane z gromadzeniem i przechowywaniem danych oraz kontrolowaniem sprzętu. Interfejsy **HMI** są często wyposażone w ekrany i, w idealnym przypadku, posiadają łatwe w obsłudze panele obsługowe i elementy sterowania. Mogą wykorzystywać grafikę i wizualizację, ułatwiającą obsługę i interpretację danych i funkcji.

#### Zadania

Do zadań systemu **SCADA** należy:

> • Ciągła komunikacja ze sterownikiem **PLC**
>
> • Czytelna wizualizacja danych w czasie rzeczywistym
>
> • Obsługa bazy danych z odpowiednimi informacjami technologicznymi
>
> • Obsługa instalacji alarmowych
>
> • Generowanie raportów o postępach procesu technologicznego

#### Zastosowanie

Systemy **SCADA** są szczególnie istotne przy _skomplikowanych, wielkoskalowych_ instalacjach przemysłowych. Istotna jest zdolność do organizacji pracy wielu składowych równocześnie, w przeciwieństwie do prostych systemów **HMI**. Systemy **SCADA** umożliwiają organizacjom monitorowanie i raportowanie procesów na podstawie danych w czasie rzeczywistym oraz archwizację danych na potrzeby późniejszego przetwarzania i ewaluacji.

#### Schemat

![](https://cdn.discordapp.com/attachments/982375180401770526/1150086602945724416/panel-hmi-zamontowany-na-maszynie-automatyka-webhmi-scada4.jpg)

## 2\. Wymiana danych

![](https://33333.cdn.cke-cs.com/kSW7V9NHUXugvhoQeFaf/images/d32f02a0d256a3cb3115a531a950927cc46e02269df37cbd.png)

#### Poziomy systemu

>      0. Na najniższym poziomie _0_ znajdują się urządzenia _wykonawcze_ oraz _pomiarowe_
>
> 1. Pierwszy poziom składa się ze sterowników **PLC** 
> 2. Poziom drugi to komputery nadzorujące, odpowiedzialne za **HMI** oraz przekazanie informacji do komputerów koordynujących
> 3. Jednostki poziomu trzeciego nie wplywają bezpośrednio za działanie elementów wykonawczych, ale moniturują całokształt produkcji
> 4. Najwyższy poziom jest odpowiedzialny za planowanie produkcji i zbiorową analizę danych

## 3\. SCADA System Components
#### Remote Terminal Unit (RTU)
Remote terminal units, abbreviated as RTUs, establish connections with sensors and actuators within a given process and are integrated into the supervisory computer system via a network. RTUs possess inherent control capabilities and frequently adhere to the IEC 61131-3 standard for programming, supporting automation through methods such as ladder logic, function block diagrams, or a range of other programming languages. In remote areas where local infrastructure is scarce or nonexistent, it is not uncommon to encounter RTUs that rely on compact solar power systems for energy, utilize radio, GSM, or satellite communication methods, and are built to endure harsh environmental conditions, withstanding temperatures ranging from -20°C to +70°C, or even as extreme as -40°C to +85°C, without the need for additional heating or cooling equipment.
#### Programmable logic controllers (PLC)
These devices, commonly referred to as PLCs, interface with sensors and actuators within industrial processes and establish connections with a central supervisory system. In the realm of factory automation, PLCs are typically equipped with high-speed links to the SCADA system. In remote scenarios, such as in the context of a large water treatment facility, PLCs can either directly link up with SCADA via wireless connections or, more frequently, employ an RTU to manage communication. PLCs are purpose-built for control purposes and played a pivotal role in the development of the IEC 61131-3 programming languages. They are often preferred for cost-effective reasons in remote installations with a significant number of input and output connections, as opposed to relying solely on an RTU.
#### Communication infrastructure - Radio/Modems & Sensors/Transducers & Repeaters
Radio/Modems allows for the transfer of data (usually wireless) across a large geographic area. A key component of a SCADA system is the ability to send and receive real-time data. Radio/modems are an efficient and reliable mode of accomplishing this feat.
Sensor is a type of transducer that can receive a signal from a physical system. It communicates information through the use of telemetry (and a control system). The sensor in a SCADA system serves to help operators measure and collect data from a remote location.
Repeaters receive and retransmit signals. They are able to transmit signals over large distances, even with the presence of a physical obstruction.
Traditional SCADA systems have traditionally relied on a mix of radio and wired connections, although larger systems like those used in railways and power stations often opt for SONET/SDH technology. The remote monitoring and management aspect of a SCADA system is commonly referred to as telemetry. Some users prefer to have their SCADA data transmitted over their existing corporate networks or share the network with other applications. However, remnants of older, low-bandwidth protocols are still in use.

SCADA protocols are designed to be highly efficient and compact. Many are designed to transmit data only when the master station requests information from the RTU. Examples of legacy SCADA protocols include Modbus RTU, RP-570, Profibus, and Conitel. While these communication protocols are specific to SCADA vendors, they are widely adopted and utilized, with the exception of Modbus, which has been made open by Schneider Electric. Standardized protocols such as IEC 60870-5-101 or 104, IEC 61850, and DNP3 are recognized by all major SCADA vendors. Many of these protocols have been extended to operate over TCP/IP. However, it's important to note that while conventional networking standards like TCP/IP are used, they serve fundamentally different purposes from industrial networking.

To meet increasing security requirements, such as those outlined by the North American Electric Reliability Corporation (NERC) and critical infrastructure protection (CIP) regulations in the US, satellite-based communication is becoming more prevalent. This approach offers advantages such as self-contained infrastructure (independent of public telephone circuits), built-in encryption, and tailored engineering for SCADA system reliability and availability. Modern carrier-class systems provide the necessary quality of service for SCADA applications, whereas earlier experiences with consumer-grade VSAT were less satisfactory.
#### SCADA Master Station 
In small SCADA systems, the master station is a single computer that communicates with controls systems and other equipment. In larger SCADA systems, this can include multiple servers, software applications, remote terminal units (RTUs), and programmable logic circuits (PLCs). This forms the central nucleus of the SCADA system, responsible for both gathering data from the industrial process and dispatching control instructions to the connected field devices. It encompasses the computer hardware and software that manages communication with the field connection controllers, namely RTUs and PLCs, and also encompasses the HMI software running on operator workstations. In smaller-scale SCADA setups, the supervisory computer may consist of a single PC, in which case the HMI is integrated into this same computer. Conversely, larger SCADA systems often feature a master station with multiple HMIs hosted on client computers, numerous servers for data collection, distributed software applications, and contingency sites for disaster recovery. To enhance system reliability, these multiple servers are frequently configured in a dual-redundant or hot-standby arrangement, ensuring continuous control and monitoring even in the event of a server malfunction or failure.
#### SCADA Monitoring Software
SCADA Monitoring Software is simply a set of data instructions that instructs the system how to interact with all of the hardware and other components. It is a way to easily monitor and control the performance of a SCADA system.
#### Human Machine Interface (HMI)
The human-machine interface (HMI) serves as the visual gateway for operators within the supervisory system. Its primary function is to convey plant-related information to operators through graphical representations like mimic diagrams, which provide a schematic overview of the controlled plant, as well as pages for logging alarms and events. The HMI is closely connected to the SCADA supervisory computer, enabling it to display real-time data, animate mimic diagrams, showcase alarms, and generate trend graphs. In many setups, the HMI serves as the primary graphical user interface for operators, gathering data from external devices, generating reports, managing alarms, and facilitating notifications.
Mimic diagrams incorporate line drawings and symbolic representations to depict various process elements. They may also incorporate digital photographs of the actual process equipment overlaid with animated symbols.
The HMI is the central control point for plant operations, allowing operators to issue commands using input devices such as mice, keyboards, and touch screens. For instance, a pump symbol can indicate whether the pump is running, and a flow meter symbol can display the current flow rate. Operators can stop the pump by clicking the mouse or touching the screen, and the HMI will reflect the real-time decrease in fluid flow through the pipe.
Typically, the HMI software package for a SCADA system includes a drawing tool that operators or maintenance personnel can use to customize how these data points are presented in the interface. These representations can be as straightforward as an on-screen traffic light, which mirrors the status of a real traffic light in the field, or as intricate as a multi-projector display illustrating the positions of all elevators in a skyscraper or the locations of all trains on a railway network.

## 4\. SCADA Applications
#### SCADA (Supervisory Control and Data Acquisition) systems are employed across various industries and industrial sectors for the purposes of monitoring, controlling, and collecting data from processes. Here are some common applications:
> 1. **Industrial Process Control:** SCADA systems are extensively used in industrial settings to monitor and control manufacturing and production processes. They ensure that equipment and machinery operate efficiently and within specified parameters.
> 2. **Utilities Management:** SCADA is employed in managing utility services such as water treatment, wastewater management, and power distribution. It helps optimize resource usage and maintain the quality of services.
> 3. **Energy Management:** SCADA systems play a crucial role in monitoring and controlling energy production and distribution, including power generation plants, substations, and smart grids.
> 4. **Oil and Gas Industry:** In the oil and gas sector, SCADA systems are used for monitoring and controlling pipelines, drilling operations, and refining processes. They aid in the safe and efficient extraction and distribution of resources.
> 5. **Environmental Monitoring:** SCADA systems are utilized in environmental applications like air quality monitoring, weather stations, and pollution control. They help gather data for regulatory compliance and environmental protection.
> 6. **Transportation and Infrastructure:** SCADA systems are employed in managing transportation systems, including traffic control, railway operations, and airport management. They ensure smooth and safe transportation services.
> 7. **Building Automation:** In commercial and residential buildings, SCADA systems are used for HVAC (Heating, Ventilation, and Air Conditioning) control, lighting management, and security systems.
> 8. **Water and Wastewater Management:** SCADA systems are vital for monitoring and controlling water treatment plants, distribution networks, and wastewater treatment facilities, ensuring the supply of clean water and proper sanitation.
> 9. **Telecommunications:** SCADA systems help manage telecommunications infrastructure, including cell towers, ensuring network availability and performance.

#### Here are a few key SCADA system applications, and their main features:
> **Asix SCADA:**
>     • **User-Friendly Interface:** Asix offers a user-friendly graphical interface that allows users to quickly understand and control processes.
>     • **Real-Time Data Collection:** The application allows for real-time data collection from various devices and processes, enabling continuous monitoring and response to changes.
>     • **Integrated Diagnostic Tools:** Asix provides advanced diagnostic tools that assist in quickly identifying and resolving issues within the system.
>     • **Support for Various Communication Protocols:** It supports various communication protocols, making it easy to connect with different devices and systems.
##### Źródła: 

* [copadata.com](https://www.copadata.com/pl/product/zenon-software-platform-platforma-programowa-firmy-copa-data/wizualizacja-kontrola/co-to-jest-scada/)
* [iautomatyka.pl](https://iautomatyka.pl/co-to-jest-scada-i-co-daje-wizualizacja-procesow-przemyslowych/)
* [wikipedia.pl](https://pl.wikipedia.org/wiki/SCADA)
* [htt.io](https://htt.io/resources/scada-basics/)
