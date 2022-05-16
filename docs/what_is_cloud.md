#### Journey To The Cloud

###### DATA SYSTEM

   1. Database System = Db + Dbms
DB = ordered collection of info stored & read electronically from a computing system.
      * Structured - rdbms -> allows different operations to be performed on data
      * Unstructured -> pics, videos, text
Client-server architechture -> data is stored in a centralised loc. and users worldwide can access. Searching is fast & memory utilization is efficient

> _HowToSearchIn DBMS & FlatFileSystem: need to know attr of file i.e. name, loc & metadata | request sent to server to access data._

   2. Difference b/n DBMS & FlatFIleSystem
      * support multi-user access at same time | doesn't
      * role based security control | doesn't
      * used by small & large buz | small buz
      * no redundancy & integrity issues | it has
      * expensive | cheap
      * can work w/ complicated transactions | can't 

   3. Components of DBMS: hardware, software, data, procedures, dal(data access lang i.e. sql)

   4. Types of DBMS:
      * Hierarchical Model - tree structure, 1-1
      * Network Model -  graph structure, 1-1, many-many
      * Relational Model - 2-dimensional tables using rows/cols, sql
      * Object-Oriented Model - objects, oop concepts 

> _Main difference between hierarchical databases and relational databases is that hierarchical databases store data in the form of a tree with parent and child nodes, whereas relational databases store data in tables with rows and columns as entities and attributes. A hierarchical database contains duplicate data, but relational databases do not. Relationships: One-one,one-many | One-one,one-many,many-many. Data retrieval: The tree must be traversed from the root node to the required node | Using SQL query language_

   5. Fields that use dbms: Financial, Banking, University, Sales, Telecom, Airlines, HR Mgt, Manufacturing/ distribution

   6. Advantages of dbms: Controls Db Redundancy, Privacy, Data Integrity, Backup & Recovery, Sharing Data, Data Consistency, Data Security

   7. Disadvantages of dbms: Cost of Hardware & software(high speed processor & huge memory) and is quite high, Huge size, Higher impact of failure(stored in a centralised place), Complex to use(training)

   8. Popular dbms software: mysql, sqlite, postgresql, microsoft sql server, oracle db, ibm


###### NETWORKING FUNDAMENTALS
   1. Networks - simply connected stuff
Uses: public transportation, national power grid for electricity, meet & greet people, postal systems for sending stuff, connect two/more devices

   2. Internet - giant network(public) that consists of many small networks(private) within.
first iteration of the internet ->  ARPANET (US Defence Dept) 1960
actual -> WWW (Tim Berners-Lee) 1989

   3. Types: Private, Public

   4. Identify devices through - 
      * IP Addr(street addr unique in the network/area) - id host on a network. Divided into 4 parts(octets). IP addr standards are called protocols. IPv4: 2^32(4.29b) , IPv6: 2^128 (340tr+)

      * MAC (Media Access Control) address (i.e.l. serial no.) -> Pyhsical network interface(microchip board) found on motherboard is given a unique address(hex16, split in twos by a colon. 1st 6digits rep company that made the interface, last 6digits a unique no.) at the factory it was built in.

> _Spoofing - networked device identifies pretentiously as another using its MAC addr which can break poorly implemented security. MAC addr control can be used to manage attacks._

   5. Ping uses (ICMP: Internet Control Message Protocol) to determine the perfomance of a connection b/n devices. eg. if connection is reliable or exits.
Time taken for ICMP packets travelling b/n devices is measured using echo packet and ICMP's echo reply from target device.
> `ping ipaddr/web-url` <br>
> `ping -c 4 8.8.8.8` = ends after 4 packets


###### OPERATING SYSTEMS
   1. OS - manages hardware & running programs. It loads, manage processes, provides interfaces to hardware via sysyem calls, provides a filesystem, provides a basic ui.

   2. Series of OS:
Microsoft - Windows 8, Windows Server 2012
Unix - Linux, BSD, OS X

   3. Device driver - plug-in module that manages a particular io device

   4. Pre-emptive multitasking

> _cpu receives interrupt > interrupt invokes handler > handler savesrest of state of CPU for the process > handler does its business > handler invokes scheduler > scheduler selects a process to run > scheduler restores state of the CPCU for that process > scheduler jumps execution to that process_

   5. System calls - processes initiate requests to OS. Process uses "syscall" to invoke a system call, where the process specifies a systemcall no. The process checks the system call table for the addr routine to that no. and jumps execution to that addr.

   6. How a process uses memory: call stack(store local vars), heap(everything else), text(the code){never modified for the duration of the process}

   7. memory leak- Failure to deallocate unneeded heap memory which is obviously taking up address space.
To free valuable ram, OS may swap pages of a process to a storage(hard drive) and they are not connected to ram

> _created > waiting(to be selected by the scheduler) > running > (<<blocked<) > terminated_
 
   8. File system (read, write info). File partioning - space division. In unix, / is refered to as root dir.
> eg, /banana = root/banana.
Partitions can be nested on root dir.
 
   9. IPC (Interprocess Communication) - any mechanism(files, pipes, sockets, signals, shared memory) that facilitates communication b/n processes 


###### SERVERS
   1. Server - dedicated computer that provides services on behalf of clients.  A server is a role that a pc takes. A desktop can be set up as a server but cannot handle large clients/workload cos it can only handle a limited amt of concurrent connections.

   2. Servers can vary in types: 
      * Web Server - host a website
      * Db Server - stores data at backend and retrieved at frontend
      * Email server - sending & receiving email

> _A server can be set up to handle various services_

   3. Servers need to be reliable, made with robust hardware that runs non stop with little to no downtime.

   4. Desktop server uses a processor designed for servers - intel core series. (AMD processors support ECC RAM)
A server uses a processor designed for servers
> Xeon (
> * supports multi processing env.
> * ECC Ram i.e. Error  Correcting Code memory- detects if data was correctly processed, protect against memory error.
> * supports largr amt of RAM.
> * larger cache memory.
> * higher core count.
> * hot swappable hard drive in RAID config. RAID copies data on multiple disks and restores on new inserts.
> * server should have redundant power supplies, use server OS (linux, windows, macOS) cos they are robust and stable. <br>
>) 


###### VIRTUALIZATION
> Hardware - (cpu + ram + network ) + traditional storage <br><br>
> Virtual Server - (virtual cpu + virtual ram + virtual network + virtual storage)
> and each component can be scaled to needs.

   1. Virtualization - process of creating a software based / virtual version of something

   2. Hyperversor (makes virtualization feasible) - software that runs above a server/ host. They pull resources from physical server and allocate to virtual env. and manages them
      * Type 1/ Bare metal HV - stored directly on top of a physical server (takes the place of host os). They are secure and lowers latency. Eg Citrix/Xen Server, VMware ESXi and Microsoft Hyper-V, Opensource KVM
      * Type 2/ Hosted HV is used for end user virtualization. Eg. Microsoft Virtual PC, Oracle Virtual Box, VMware Workstation, Oracle Solaris Zones, VMware Fusion, Oracle VM Server for x86

> _You can build a virtual variant/ vm once you have hypervisor installed. You can have multiples vms on an HV. These vms are independent of each other and can have different os. They are also portable to different HVs._

   3. Benefits
      * cost savings
      * agility and speed


###### CLOUD COMPUTING
   1. Compare On-premise to Cloud
      * higher pay, less scalability | pay for what you use 
      * alot space for servers | no server space required
      * appoint a team for hardware & software maintenance | no experts required for hardware & software maintenance
      * poor data security | better data security
      * less chance data recovery | disaster recovery
      * lack flexibility | high flexibility
      * no auto updates | auto software updates
      * less collabo | teams collab from widespread locations
      * data cannot be accessed remotely | data can
      * takes longer implementation time | rapid implementation

   2.  Cloud computing - ability to deliver on demand computing services over the internet on a pay as you go basis. Files are saved and managed in cloud / (overtheinternet)

   3. Types

      * Deployment model:
         * Public: access to anyone eg. bus transportation. It is made available to public over the internet and owned by cloud provider eg. AWS, MS Azure, IBM's Blue Cloud, Sun Cloud
         > _dedicated to two/more orgs = multitenancy_<br> Also, an org can have multiple public clouds i.e. renting spaces from different landlords.
         * Hybrid: pay for use only when needed eg. rent a taxi. Eg. some agencies might use prite cloud for secure info and public to share datasets with public
         > _an org can have both by apportioning their services or all services on private and backup on public_

         * Private: owned by single person eg. car owner. It is exclusively operated by a single org. and can be managed by the org / 3rd party and may exist on / off premise eg. AWS, VMware

       * Service Model:
         * IaaS - Infastructure if buz needs vm | Users:  IT admins
         > _building on a lease land_

         * PaaS - Platform if buz needs a platform for building software products |Users: software devs
         > _renting equipments to build_

         * SaaS - Software if buz doesnt need to maintain any IT equipment(accessed w/ username & pwd) | Users: end users
         * Serverless - Provide backend services on an as-used basis
         > _pay for a sevice only when needed = multitenancy_

         __What you'll manage in a service model__
         > * Applications - IaaS, PaaS
         > * Data - IaaS, PaaS
         > * Runtime - IaaS
         > * Middleware - IaaS
         > * OS - IaaS
         > * Virtualization
         > * Servers
         > * Storage
         > * Networking

   4. Cloud Providers 
      * AWS - IaaS, PaaS, SaaS. Services can be used to create, deploy any type of app in the cloud, uses pay-for-what-you-use subscription | Amazon
      * MS Azure -building, testing, deploying and managing app through servers throughout global networks MS offers. IaaS, PaaS, SaaS, supports various programming tools | MS
      * IBM Cloud - IaaS, SaaS, PaaS, Deployment Models | IBM
      * VMWare - platform virtualization software and services | Dell Tech | x86arch
      * GCP -  soup of cloud services run on same infastructure used internally for end user products eg. Youtube, GSearch. <br>
 Also provides computing, data storage, data analytics and machine learning services | Google
      * Digital Ocean - data centers worldwide, provides cloud services that helps to deploy & scale apps to run simultanuously on multiple pcs jan 2018 3rd | Newyork

   5. Lifecycle of a cloud computing solution
> Define purpose -> Define hardware -> Define Storage -> Define Network -> Define Security -> Testing the process -> Analytics
