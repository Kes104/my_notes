#### Cloud Resource virtualization

##### Contents
- Virtualization
- Layering and virtualization
- Virtual Machine Monitor [VMM]
- Virtual Machine
- Performance and Security isolation
- Architectural support for virtualization
- Full-virtualization and Para-virtualization

###### Motivation
- Virtualization is basic tenet of Cloud Computing.
- VM state running under VMM can be saved and migrated to another server to balance workload.
- allows users to operate in environment they are familiar with instead of idiosyncratic ones.
- virtualization is important as 
  1. *System security*, allows isolation of services under same hardware.
  2. *Performance and reliability*, allows app to migrate from one platform to another.
  3. development and management of services offered by provider
  4. *Performance isolation*

###### Virtualization
Simulates interface to a physical object by :
1. Multiplexing
2. Aggregation
3. Emulation
4. Multiplexing and Emulation

###### Layering
Common approach to manage system complexity
Simplifies description of subsystems
- Layering in Computer System :
  1. Hardware
  2. Software
     - Operating System
     - Libraries
     - Applications

###### Interfaces
- *Instruction set architecture (ISA)*
  boundary between hardware and software.
- *Application binary interface (ABI)*
  allows ensemble to access the hardware.
- *Application Programming Interface (API)*
  Involves HLL library calls that often invoke system calls

###### Virtual Machine Monitor
Partitions the resources of a virtual machine into one or more virtual machines.
Allows several OS to run concurrently on a single hardware platform.
- Multiple services - same platform
- Live migration
- System modification
- isolation among systems - security
> VMM virtualization of CPU and memory
- privileged instructions
- interrupts
- Shadow page table - used by Memory Management Unit (MMU)
- Monitors system performance

###### Virtual Machine
- isolated environment that appears to be a whole computer but is actually accessing only a portion of computer resources.
> VM Types
- Process VM
- System VM
- Traditional VM
- Hybrid VM
- Hosted VM

**Conditions for efficient virtualization**
- Program under VMM shall execute same behavior as the one running on an equivalent machine.
- VMM shall be in complete control of virtualized resources.
- significant fraction of machine instructions shall be executed without VMM intervention
  Two classes of machine instructions
  1. Sensitive - special precaution at execution time
     - Control sensitive
     - Mode sensitive
  2. Innocuous - not sensitive

###### Full Virtualization & Para Virtualization

*Full virtualization*
- a guest OS can run unchanged under the VMM as if running directly on hardware platform
- example is VMware. VirtualBox.

*Para Virtualization*
- a guest OS is modified to use only instructions that can be virtualized
- Reasons for this can be
  1. Some hardware aspects can not be virtualized
  2. Improved Performance
  3. Simpler interface presentation
- examples are Xen, Denaly
