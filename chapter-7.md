#### Networking Support

##### Contents
- Network Management - Class based queuing [CBQ]
- Cloud interconnection networks
- Storage area networks [SAN]
- Content delivery networks [CDN]
- Scale free networks 
- Epidemic Algorithms

###### Class Based Queuing
Objectives
- Flexible link sharing for applications
- balance between short lived network flows

It aggregates connections and constructs  a tree like hierarchy of different classes according to priority and throughput applications.

CBQ functional units
1. classifier
2. estimator
3. selector / scheduler
4. delayer

class is
1. Over-limit -> if over a certain recent period it has used more than its allocation.
2. Under-limit -> if it has used less
3. at-limit -> exactly its allocation

leaf class is
1. satisfied -> if under-limit and has a persistent backlog.
2. unsatisfied -> otherwise.

non-leaf class - unsatisfied -> if under-limit and has some descendant class with persistent backlog.

###### Hierarchical Token Buckets (HTB)
- link sharing algorithm inspired by CBQ
- example is linux kernel
- Each class has 
  - An Assured rate (AR).
  - A ceil rate (CR).
- Supports Borrowing

###### Cloud interconnection networks
- Network infrastructure organised hierarchically
- servers -> racks -> rack router -> cluster router -> local communication fabric.
- several requirements of networking infrastructure
  1. scalability
  2. Low cost
  3. Low latency
  4. High bandwidth
  5. location transparent communication between servers
> Interconnection networks - InfiniBand
- used by supercomputers and computer clouds
- Data rates can be SDR, DDR, QDR, FDR, EDR.

###### Routers and Switches
 - cost of inter-connection = cost of routers + number of cables.
 - Better performance , lower costs -> router architecture.
 - ROUTER - SWITCH interconnecting several networks
   1. *low-radix routers* -> small port numbers, divide bandwidth into smaller number of *wide* ports.
   2. *high-radix routers* -> large port numbers, divide bandwidth into large number of *narrow* ports.
 - high-radix => lower latency & reduced power consumption
 > Network Characterization
 - diameter of network = average distance between all pair of nodes.
 - bisection bandwidth = measures communication between 2 networks of same size.
 - cost
 - power consumption

###### Clos Networks

- *Butterfly network*
  comes from inverted triangles pattern created by interconnections.
  uses most efficient route, but blocking when it comes to handling 2 packets transferring to same port at same time (conflict).
- *Clos*
  Multistage non-blocking network with an odd number of stages.
  2 butterfly networks. last layer of input fused with first stage of output.
  A packet takes twice as many hops as it really needs.
- *Folded-Clos network*
  input and output networks share switch modules.
  also called fat tree.
  Myrinet, InfiniBand & Quadrics

###### Storage area networks
- high speed network for data block transfers between computer systems and storage elements.
- Fibre Channel (FC) is the dominant architecture of SANs.
- FC is a layered protocol.
- SAN interconnects servers to servers, servers to storage and storage to storage devices.

###### FC Protocol layers
- part of SAN, a layered protocol.
> 3 layer protocol
- FC-0, the physical interface.
- FC-1, the transmission protocol.
- FC-2, signaling protocol.
> 2 upper layer protocol
- FC-3, common services layer
- FC-4, protocol mapping layer
> *FC networks*
- unique id - WWN (World Wide Name), 64-bit address.
- Each switch in switched fabric - own unique 24-bit address. Domain, Area and Port address.
- Switch assigns port numbers dynamically and maintains port addresses.
- Switch maintains correlation between port and WWN address using name server.
- Name server, component o fabric operating system.

###### Content Delivery Networks (CDNs)
- supports scalability
- increases reliability and performance
- provides better security

1. CDN receives content from origin server, replicates it in edge-cache servers. Content delivered through *closest* edge server.
2. CDN content delivery methods
   - Static content - maintained using traditional caching techs as changes are infrequent. ex: HTML pages, images, docs, software patches, etc
   - Live Media  - real-time content delivery from encoder to media server.
3. CDN Protocols
   - NECP - Network element control protocol
   - WCCP - Web cache coordination protocol
   - CARP - Cache array routing protocol
   - ICP - Internet cache protocol
   - HTCP - HyperText Cache Protocol
   - Cache digest
4. CDN design & policy decisions
   - edge server placement
   - content selection and delivery
   - content management
   - request routing policies
5. CDN performance metrics
   - Cache hit ratio
   - Reserved Bandwidth
   - Latency
   - Edge server utilization
   - Reliability

###### Scale-free networks
- follows power law
- physical & social systems interconnected by a scale free networks.
- The web, the scientific paper citation, social networks confirm this trend.
- vertices of this network:
  -- directly connected to vertices with highest degree
  -- low degree & only a few vertices connected to large number of edges.

###### Epidemic Algorithms

- mimic transmission of infectious diseases and often used in distributed systems to accomplish tasks such as :
  1. disseminate information, e.g. topology information
  2. compute aggregates, e.g. arrange nodes in a gossip overlay into a list sorted by logarithmic time.
  3. manage data replication in distributed system
- Game of Life implements Epidemic algorithm
- several classes exist. concept for classifying these algorithms
  1. Susceptible (S)
  2. Infective (I)
  3. Recovered (R)
> Epidemic algorithm types
- Susceptible-Infective (SI) algo -> when entire population is subject to be infected. one infected, remains in that state until entire population infected.
- Susceptible-Infectious-Recover (SIR) -> follows transition from one state to another. size is fixed.
- Susceptible-Infectious-Susceptible (SIS) -> special case of SIR when recovery happens without immunity.