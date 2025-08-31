# High Availability and Scalability in a Private Cloud

## Lab Topology
- **PLABDC01** → Domain Controller (192.168.0.1/24)
- **PLABDM01** → Domain Member Server (192.168.0.2/24)
- **PLABWIN10** → Domain Member Workstation (192.168.0.3/24)

These devices were used to practice scalability and high availability options in a private cloud environment.

---

## Key Concepts

### High Availability (HA)
- Goal: keep systems running with minimal downtime.  
- Techniques include redundancy, clustering, failover, and load balancing.  
- Public clouds also use **Availability Zones (AZs)** for fault tolerance.

### Scalability
- Ensures infrastructure can meet demand.
- **Vertical scaling** = adding more CPU/RAM to a machine.  
- **Horizontal scaling** = adding more machines or servers.  
- **Cloud bursting** = moving overflow traffic to another cloud environment.  
- Auto-scaling allows VMs/containers to expand resources automatically.

### Hypervisors
- Software that creates and manages virtual machines (VMs).  
- Examples: **VMware, Microsoft Hyper-V, Oracle VirtualBox.**  
- Affinity vs Anti-Affinity: decides if VMs run on the same host or separate ones.  

### Single Points of Failure (SPOF)
- A weakness where one failure could bring down the entire system.  
- Examples:
  - Using only one hypervisor host.
  - Hardware Security Module (HSM) vulnerabilities.
  - Infrastructure reaching end of life without replacement.

### Oversubscription
- Cloud provider allocates more resources than available (multiple customers sharing).  
- Can cause performance issues if demand spikes.

### Networking for HA
- Key components:
  - Switches  
  - Routers  
  - Load Balancers  
  - Firewalls  
- In private clouds, Virtual Private Cloud (VPC) setups are often used.

---

## My Reflection
- I learned how **HA and scalability complement each other**: HA reduces downtime, while scalability ensures performance under load.  
- Setting up HA requires identifying SPOFs and planning redundancy.  
- Scalability can be vertical or horizontal, depending on the use case.  
- Networking and hypervisors play a big role in ensuring flexibility.  

---

## Next Steps
- Practice configuring Hyper-V scalability options.  
- Test failover scenarios with load balancing.  
- Document improvements to lab design.
