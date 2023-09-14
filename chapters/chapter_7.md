## Table of Contents
* [What is **SCADA**?](chapter_1.md)
* [Data Exchange in **SCADA**](chapter_2.md)
* [**SCADA** System Components](chapter_3.md)
* [**SCADA** Applications](chapter_4.md)
* [Operating Station](chapter_5.md)
* [**SCADA** and Distributed Control System](chapter_6.md)
* [Sources](chapter_8.md)
* [Authors](chapter_9.md)
  
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
  
