# SBI Branch Office Enterprise Network Project
This project involves the implementation of a real-time enterprise network for an SBI Branch Office. The primary objective is to ensure high availability and redundancy in the network by integrating multiple ISPs and configuring appropriate routing techniques. The network was successfully designed, tested, and implemented using GNS3 simulation.
 **Branch Office Router**:
   - Model: Cisco ISR 4000 series Router
   - Configured with a default route to ensure redundancy by leveraging two ISPs (Tata and Airtel)

   - **Switch**:
   - Model: Cisco Catalyst 2960-X Series Switch
   - Provides connectivity to branch office end devices (Manager system, Cashier1, and Cashier2).

 **ISP Routers**:
   - Tata Bandwidth: Static IP routing with AD value of 30.
   - Airtel Bandwidth: Static IP routing with AD value of 50.
   - The lower AD value is preferred for routing traffic.

   - *End Devices**:
   - Manager system, Cashier1, and Cashier2 are connected to the branch office network.
   - *Other Components**:
   - Google DNS (8.8.8.8) is used for external DNS resolution.

   - DHCP Configuration (Branch Office Router):
ip dhcp pool branchoffice
 network 192.168.10.0 255.255.255.0
 default-router 192.168.10.1
 dns-server 192.168.10.100


Features and Highlights
- **Redundancy**: Implemented dual ISP connections to ensure uninterrupted internet connectivity.
- **Dynamic IP Allocation**: Configured DHCP for automatic IP assignment to branch office end devices.
- **High Availability**: Preferred route is based on AD values to dynamically select the best path.
- **Scalable Design**: The topology can easily be extended to accommodate additional devices or branches.

- 
## Achievements
- Successfully established and tested connectivity between all devices in the branch office.
- Verified redundancy by simulating ISP link failures and confirming automatic failover.
- Ensured proper IP address management and DNS resolution for branch office devices.

- 
## Future Improvements
- Implement dynamic routing protocols (e.g., OSPF or BGP) for better scalability.
- Integrate security features such as firewalls and VPNs.
- Monitor network performance using SNMP or NetFlow.

- How to Run the Project
1. Open the project in GNS3.
2. Start all devices in the topology.
3. Test connectivity using ping and traceroute commands.
4. Simulate link failures to verify redundancy.
