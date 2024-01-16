# Operating Systems (SOFE3950)

todo: fix this, catch up on lecture 1 notes.

| Category                     | Mark   |
|------------------------------|--------|
| In-Class Activities/Quizzes  | 10%    |
| Tutorials                    | 10%    |
| Labs                         | 15%    |
| Midterm (Feb. 13th)          | 20%    |
| Final                        | 45%    |

Office hours:
- Tuesday: 6 - 7 pm
- Thursday: 2 - 3 pm


**Quizzes:**
- Lockdown browser will be used in quizzes and must be done in class. 
- Expect a quiz every week. *(Lowest quiz mark dropped)*

**Midterm:**
- The exam will be on Feb. 13th during the class time. (**yes that means it's at 8pm**)
- No midterm deferral, marks will be added to the final exam
- Must pass final.

|Course Type | Location | Day | Time | Start Date |
|-|-|-|-|-|
|74025 |UA3130 |Thu |11:10am - 02:00 pm| 26/1, 9/2, 1/3, 15/3, 29/3|
|74026 |UA3130 |Thu| 11:10am - 02:00 pm |19/1, 2/2, 16/2, 8/3, 22/3,|

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 1 | Introduction to OS</summary>
  
  # Introduction
*What is an Operating System?*

Acts as an intermediary b/w user of computer and computer hardware.

Operating System Goals:
- Execute user programs & make solving user problems easier
- Make computer system convenient to use
- Use computer hardware in an efficient manner.

## Computer System Hardware
![os1](../static/OS_1_1.png)

Computer system can be divided into four components:

**Hardware** – provides basic computing resources
- CPU, memory, I/O devices

**Operating system**
- Controls and coordinates the use of hardware among various applications and users

**Application programs** – define the ways in which the system resources are used to solve the computing problems of the users
- Word processors, compilers, web browsers, database systems, video games

**Users**
- People, machines, other computers

# What do Operating Systems do?

***Exploring the OSes from two viewpoints***:

**User view:**

Users prefer <ins>convenience, ease of use, and good performance.</ins> Not resource utilization.

Users of delicate systems such as workstations have dedicated resources but frequently use shared resources from servers

Handheld computers (smartphones) are resource poor, optimized for usability and battery life, and some computers have little or no user interface, such as embedded computers in devices and automobiles.

**System view:**

The OS is the program that most intimately involved with the hardware. We can view the OS as a:
- Resource allocator
  - Manages all resources
  - Decides between conflicting requests for efficient and fair
resource use
- Control program
  - Controls the execution of user programs to prevent errors and improper use of the computer
 

# Computer System Organization

Common definition:
Kernel: The one program running at all times on the computer.

And two other types of programs:
- a system program (ships with the operating system)
- an application program.

## Computer System Operation

![os2](../static/OS_1_2.png)

I/O devices and the CPU can execute concurrently. Each device controller is **in charge of a particular device type** and has a **local buffer**.

CPU moves data from/to main memory to/from local buffers, I/O moves data from the device to local buffer of controller, of which the controller informs the CPU that it has finished its operation by causing an interrupt.

The bootstrap program is typically stored in **ROM** or **EEPROM**, generally known as firmware. 

1. It initializes all aspects of the system,
2. Loads operating system kernel and starts execution
3. The kernel then starts providing services to the system and its users.
4. Some services are provided outside of the kernel, by system programs that are loaded into memory at boot time to become system processes, or system daemons that run the entire time the kernel is running.
5. The system is now running and waiting for an event to occur.

## Common Function Interrupts

OSes are **interrupt driven.**

Occurrences of events are usually signaled via interrupts by either:

The **hardware,** triggering an interrupt by sending a signal to the CPU, or, 

the **software,** triggering an interrupt by executing a **system call.**

Interrupt transfers control to the interrupt service routine generally, through the **interrupt vector**, which contains the addresses of all the service routines.

Interrupt architecture must save the address of the interrupted instruction. 

A trap or exception is a software-generated interrupt caused either by an error or a user request.

![os3](../static/OS_1_3.png)

### Interrupt Handling
OS preserves state of CPU by storing registers and program counter, and determines which kind of interrupt has occurred:

- **polling**
- **vectored** interrupt system

Separate segments of code determine what happens for each interrupt type.

### Storage Structure
**Main memory**: only large storage media that the CPU can access directly
- Random access
- Typically, volatile

**Secondary storage**: extension of main memory that provides large nonvolatile storage capacity

**Hard disks**: rigid metal or glass platters covered with magnetic recording material
- Disk surface is logically divided into tracks, which are subdivided into sectors
- The disk controller determines the logical interaction between the device and the computer

**Solid-state disks**: faster than hard disks, nonvolatile

### Storage Hierarchy

![os4](../static/OS_1_4.png)

### Caching
Copying information into faster storage system; main memory can be viewed as a cache for secondary storage

It is an important principle, that is performed at many levels in a computer (in hardware, operating system, software). Information in use copied from slower to faster storage temporarily. Faster storage (cache) checked first to determine if information is there
- If it is, information used directly from the cache (fast)
- If not, data copied to cache and used there

- Cache smaller than storage being cached
- Cache management is an important design problem
- Cache size and replacement policy

### Storage Definitions and Notation Review:
- The basic unit of computer storage is the bit.
- A byte is 8 bits, and on most computers, it is the smallest convenient chunk of storage.
- A word, which is a given computer architecture’s native unit of data. A word is made up of one or more bytes.
- Computer storage, along with most computer throughput, is generally measured and manipulated in bytes and collections of bytes.

|Name|Amount|
|-|-|
| kilobyte (KB) | 1,024 bytes (2<sup>10</sup>) |
| megabyte (MB) | 1,024<sup>2</sup> bytes (2<sup>20</sup>) |
| gigabyte (GB) | 1,024<sup>3</sup> bytes (2<sup>30</sup>) |
| terabyte (TB) | 1,024<sup>4</sup> bytes (2<sup>40</sup>) |
| petabyte (PB) | 1,024<sup>5</sup> bytes (2<sup>50</sup>) |

## I/O Structure

A general-purpose computer system consists of CPUs and multiple device controllers that are connected through a common bus. 

Each device controller is in charge of a specific type of devices. Operating systems have a device driver for each device controller to manage I/O.

Interrupt-driven I/O is good for moving small amounts of data:

1. The device driver loads the appropriate registers within the device controller.
2. The device controller determines what action to take (such as “read a character from the keyboard”).
3. The controller transfers the data from the device to its local buffer.
4. Then the device controller informs the device driver via an interrupt that it has finished its operation.
5. The device driver then returns control to the operating system

Produces <ins>high overhead</ins> when moving bulk data; DMA is used to solve this.

### Direct Memory Access (DMA) Structure

![os5](../static/OS_1_5.png)

### Single-Processor Systems:
- Most systems use a single general-purpose processor
  - Most systems have special-purpose processors as well for keyboard, disks, etc.

### Multiprocessors Systems
- Growing in use and importance
  - Also known as parallel systems, or multicore systems
  - They have two or more processors in close communication, sharing the computer resources
  - Advantages include:
    1. Increased throughput: more work done in less time
    2. Economy of scale: cost less than equivalent multiple single-processor systems
    3. Increased reliability: graceful degradation or fault tolerance

The multiple-processor systems in use today are of two types:
- Asymmetric Multiprocessing: each processor is assigned a specific task.
  - This scheme defines a boss–worker relationship. The boss processor schedules and allocates work to the worker processors.
- Symmetric Multiprocessing (SMP):
  - It is the most common
  - All processors are peers: each processor performs all tasks
  - Symmetric Multiprocessing Architecture:
 
![os161](../static/OS_1_6_1.png)
 
### Multi-Core CPUs

They are more efficient than multiple chips with single cores because on-chip communication is faster than between-chip communication.

- Uses significantly less power than multiple single-core chips
- These multicore CPUs appear to the operating system as N standard processors.
- dual-core design with two cores on the same chip

![os162](../static/OS_1_6_2.png)

### Clustered Systems

They are like multiprocessor systems, but multiple systems working together, usually sharing storage via a storage-area network (SAN)
- Provides a high-availability service which survives failures
- Asymmetric clustering has one machine in hot-standby mode
- Symmetric clustering has multiple nodes running applications, monitoring each other
- Some clusters are for high-performance computing (HPC)
- Applications must be written to use parallelization
- Some have distributed lock manager (DLM) to avoid conflicting operations

![os163](../static/OS_1_6_3.png)

# Operating System Structure

### Important Aspects of Operating Systems
- _**Multiprogramming (Batch system)**_ is needed for efficiency:
  - Single user cannot keep CPU and I/O devices busy at all times
  - Multiprogramming organizes jobs (code and data), so CPU always has one to execute
  - A subset of total jobs in system is kept in memory
  - One job selected and run via **job scheduling**
  - When it must wait (for I/O for example), OS switches to another job
 
- _**Timesharing (multitasking)**_ is a logical extension to multiprogramming in which CPU switches jobs so frequently that users can interact with each job while it is running, creating interactive computing
  - Response time should be < 1 second
  - Each user has at least one program executing in memory -> process
  - If several jobs ready to run at the same time -> CPU scheduling
  - If processes don't fit in memory, swapping moves them in and out to run
  - Virtual memory allows execution of processes that are larger than actual physical memory

## Operating System Operations

### Dual-Mode and Multi-Mode Operation
- To ensure the proper execution of the OS, we must be able to distinguish between the execution of operating-system code and user-defined code.
- Therefore, computer systems provide hardware bit to differentiate among various modes of execution.
- **Dual-mode** operation allows OS to protect itself and other system components
  - **User** mode and **kernel** mode (called _supervisor_, _system_, or _privileged_ mode)
  - **Mode bit** provided by hardware (kernel (0), user (1))
    - Provides ability to distinguish when system is running user code or kernel code
    - Some instructions designated as **privileged**, only executable in kernel mode (such as: switch mode, I/O control, timer management, and interrupt management instructions)
  - Transition from user to kernel mode:
    - _System call_ changes mode to kernel, return from call resets it to user



![os7](../static/OS_1_7.png)

The concept of modes can be extended beyond two modes:
- Increasingly CPUs support multi-mode operations
- CPU uses more than one bit to set and test the mode.

Example:

CPUs that support virtualization frequently, have a separate mode to indicate when the virtual machine manager (VMM) and the virtualization management software is in control of the system. In this mode, the VMM has more privileges than user processes but fewer than the kernel

### Transition from User to Kernel Mode
To ensure that the OS maintains control over the CPU, we use timers, which are used to prevent a user program from getting stuck in an infinite loop / process hogging resources
- Timer is set to interrupt the computer after some time period
- Keep a counter that is decremented by the physical clock.
- Operating system set the counter (it is a privileged instruction)
- When counter reaches zero, it generates an interrupt
- Set up before scheduling process to regain control or terminate program that exceeds allotted time

# Process Management

A process is a program in execution. It is a unit of work within the system.

**Program** is a _passive_ entity.

**Process** is an _active_ entity.

Process needs resources to accomplish its task
- CPU, memory, I/O, files
- Initialization data

Process termination requires reclaim of any reusable resources

Single-threaded process has one program counter specifying location of next instruction to execute
- Process executes instructions sequentially, one at a time, until completion

Multi-threaded process has one program counter per thread
- Typically, a system has many processes, some user, some operating system running concurrently on one or more CPUs
  - Concurrency by multiplexing the CPUs among the processes / threads

## Process Management Activities

The operating system is responsible for the following activities in
connection with process management:
- Scheduling processes and threads on the CPUs
- Creating and deleting both user and system processes
- Suspending and resuming processes
- Providing mechanisms for process synchronization, process communication, and deadlock handling

## Memory Management

To execute a program all (or part) of the instructions _and_ all (or part) of the data that is needed by the program must be in memory. Memory management determines what is in memory and when.
- Optimizing CPU utilization and computer response to users

This creates the need for memory management which has the following activities:
- Keeping track of which parts of memory are currently being used and by whom
- Deciding which processes (or parts of processes) and data to move into and out of memory
- Allocating and deallocating memory space as needed

## Storage Management

### Storage Management

OS provides uniform, logical view of information storage. It abstracts physical properties to a logical storage unit - file. Each medium is controlled by device (i.e., disk drive, tape drive)and varying properties include access speed, capacity, data-transfer rate, access method (sequential or random).

### File-System management
It is one of the most visible components of an operating system, and files are usually organized into directories. Access control on most systems to determine who can access what.

OS activities include:
- Creating and deleting files and directories
- Support primitives to manipulate files and directories
- Mapping files onto secondary storage
- Backup files onto stable (non-volatile) storage media

### Mass-Storage Management:
- Usually, disks used to store data that does not fit in main memory or data that must be kept for a “long” period of time
- Proper management is of central importance
- Entire speed of computer operation hinges on disk subsystem and its algorithms
- OS is responsible for the following activities:
  - Free-space management
  - Storage allocation
  - Disk scheduling
  - Some storage need not be fast
  - Tertiary storage includes optical storage (CD, DVD), magnetic tape
  - Still must be managed – by OS or applications
  - Varies between WORM (write-once, read-many-times) and RW (read-write) formats

### Caching
- Information is normally kept in main memory, when it is used, it is copied into a faster storage system (the cache) on a temporary basis.
- _Cache management_ is an important design problem.
  - Cache size and the replacement policy can result in greatly increased performance
- Main memory can be viewed as a fast cache for secondary storage
- Performance of Various Levels of Storage

![os18](../static/OS_1_8.png)

### Cache Coherency
- In a hierarchical storage structure, the same data may appear in different levels of the storage system.
- For example,
  - Migration of integer “A” from Disk to Register

![os181](../static/OS_1_8_1.png)

  - Multitasking environments must be careful to use most recent value, no matter where it is stored in the storage hierarchy
  - Multiprocessor environment must provide cache coherency in hardware such that all CPUs have the most recent value in their cache
  - Distributed environment situation even more complex
  - Several copies of a datum can be kept in different computers
  - Distributed systems must ensure that, when a replica is updated in one place, all other replicas are brought up to date on time

## I/O Systems:
- One purpose of OS is to hide peculiarities of hardware devices from the user
- The I/O subsystem consists of several components:
- Memory management of I/O including buffering (storing data temporarily while it is being transferred), caching (storing parts of data in faster storage for performance), spooling (the overlapping of output of one job with input of other jobs)
- General device-driver interface
- Drivers for specific hardware devices
- Only the device driver knows the peculiarities of the specific device to which it is assigned.

# Protection & Security

**Protection**: any mechanism for controlling access of processes or users to resources defined by the OS

**Security**: defense of the system against internal and external attacks

Huge range, including denial-of-service, worms, viruses, identity theft, theft of service
- Systems generally first distinguish among users, to determine who can do what
  - User identities (**user IDs**, security IDs) include name and associated number, one per user
  - User ID then associated with all files, processes of that user to determine access control
  - Group identifier (**group ID**) allows set of users to be defined and controls managed, then also associated with each process and file
  - **Privilege escalation** allows user to change to effective ID with more rights

# Kernel Data Structures
## Lists, Stacks, and Queues:
- An array is a simple data structure in which each element can be accessed directly.
  - For example, main memory is constructed as an array.
- A list is the most fundamental data structures in computer science.
  - The items in a list must be accessed in a particular order.
  - Linked list is the most common method for implementing the list,
  - Lists are used for constructing more powerful data structures, such as stacks and queues

![os19](../static/OS_1_9.png)

**Stack:**
- It is a sequentially ordered data structure that uses the last in, first out **(LIFO)** principle for adding and removing items

**Queue:**
- It is a sequentially ordered data structure that uses the first in, first out (FIFO) principle

## Trees:
- A _tree_ is a data structure that can be used to represent data hierarchically.
- Data values in a tree structure are linked through parent–child relationships
- In a _binary tree_, a parent may have at most two children (left child and the right child).
- A _binary search tree_ additionally requires an ordering between the parent’stwo children in which left_child <= right_child.
  - Search performance is O(n)
- An algorithm can be used to create a balanced binary search tree.
  - A tree containing **n** items has at most log<sub>2</sub>(n) levels,
  - Search performance is O(log<sub>2</sub>(n))

## Hash Functions and Maps:

A hash function takes data as its input, performs a numeric operation on this data, and returns a numeric value, of which, can then be used as an index into a table (typically an array) to quickly retrieve the data.

- Performance can be as good as O(1)
- Hash functions are used extensively in operating systems.
- Hash collision can be accommodated by having a linked list at that table location that contains all of the items with the same hash value
- A hash map, which associates (or maps) [key:value] pairs using a hash function

![os110](../static/OS_1_10.png)

## Bitmaps:
- A bitmap is a string of n binary digits that can be used to represent the status of n items.
- Example,
  - Consider the bitmap 001011101
- Resources 2, 4, 5, 6, and 8 are unavailable; resources 0, 1, 3, and 7 are available.


# Computing Environments
## Traditional Computing
- Stand-alone general purpose machines
- But blurred as most systems interconnect with others (i.e., the Internet)
- Portals provide web access to internal systems
- Network computers (thin clients) are like Web terminals
- Mobile computers interconnect via wireless networks
- Networking becoming ubiquitous – even home systems use firewalls to protect home computers from Internet attacks


## Mobile Computing
- Handheld smartphones, tablets, etc
- What is the functional difference between them and a “traditional” laptop?
- Extra feature – more OS features (GPS, gyroscope)
- Allows new types of apps like augmented reality
- Use IEEE 802.11 wireless, or cellular data networks for connectivity
- Leaders are **Apple iOS** and **Google Android**


## Distributed Computing
- Collection of separate, possibly heterogeneous, systems networked together
  - Network is a communications path, _TCP/IP_ most common
    - Local Area Network (LAN)
    - Wide Area Network (WAN)
    - Metropolitan Area Network (MAN)
    - Personal Area Network (PAN)
- Network Operating System provides features between systems across network
- Communication scheme allows systems to exchange messages
- Illusion of a single system

## Client-Server
- Many systems now servers, responding to requests generated by clients
  - Compute-server system provides an interface to client to request services (i.e., database)
    - Example: A server running a database that responds to client requests for data
  - File-server system provides interface for clients to store and retrieve files
    - Example: a web server that delivers files to clients running web browsers.

## Peer-to-Peer
- Another model of distributed system
- P2P does not distinguish clients and servers
  - Instead, all nodes are considered peers
  - May each act as client, server or both
  - Node must join P2P network
    - Registers its service with central lookup service on network, or
    - Broadcast request for service and respond to requests for service via discovery protocol
  - Examples include Napster and Gnutella, Voice over IP (VoIP) such as Skype

## Virtualization
- Allows operating systems to run as applications within other OSes
  - Vast and growing industry
- Emulation is used when the source CPU type is different from the target type (i.e. PowerPC to Intel x86)
  - Generally slowest method
  - When computer language not compiled to native code – Interpretation
- Virtualization – OS natively compiled for CPU, running guest OSes also natively compiled
  - Consider VMware running Win10 guests, each running applications, all on native Win10 host OS
  - VMM (virtual machine Manager) provides virtualization services
- Use cases involve laptops and desktops running multiple OSes for exploration or compatibility
  - Apple laptop running Mac OS X host, Windows as a guest
  - Developing apps for multiple OSes without having multiple systems
  - QA testing applications without having multiple systems
  - Executing and managing compute environments within data centers
- VMM can run natively, in which case they are also the host
  - There is no general-purpose host them like (VMware ESX and CitrixXenServer) but rather they are the host


![os111](../static/OS_1_11.png)

## Cloud Computing
- Delivers computing, storage, even apps as a service across a network
- It is logical extension of virtualization because it uses virtualization as the base for its functionality.
  - Amazon Elastic Compute Cloud (EC2) has thousands of servers, millions of virtual machines, petabytes of storage available across the Internet, pay based on usage
- Many types of cloud computing:
  - Public cloud – available via Internet to anyone willing to pay
  - Private cloud – run by a company for the company’s own use
  - Hybrid cloud – includes both public and private cloud components
  - Software as a Service (SaaS) – one or more applications available via the Internet (i.e., word processor)
  - Platform as a Service (PaaS) – software stack ready for application use via the Internet (i.e., a database server)
  - Infrastructure as a Service (IaaS) – servers or storage available over Internet (i.e., storage available for backup use)

- Cloud computing environments composed of traditional OSes, plus VMMs, plus cloud management tools
  - Internet connectivity requires security like firewalls
  - Load balancers spread traffic across multiple applications
 
![os112](../static/OS_1_12.png)

# Open-Source Operating Systems

- Operating systems made available in source-code format rather than just binary closed-source
- Counter to the copy protection and Digital Rights Management (DRM) movement
- Started by Free Software Foundation (FSF), which has “copyleft” GNU Public License (GPL)
- Examples include GNU/Linux and BSD UNIX (including core of Mac OS X), and many more
- Can use VMM like VMware Player (Free on Windows), Virtualbox (open source and free on many platforms - http://www.virtualbox.com)
  - Used to run guest operating systems for exploration
  
</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 2 | Operating System Structures</summary>

# Operating System Services






# User Operating System Interface




# System Calls





# Types of System Calls




# System Programs




# Operating System Design and Implementation



# Operating System Structure




# Operating System Debugging




# Operating System Generation






# System Boot






</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 3 | ???</summary>

</details>

---

<details>
  <summary style="font-size: 30px; font-weight: 500; cursor: pointer;">Lecture 4 | ???</summary>

</details>

---
