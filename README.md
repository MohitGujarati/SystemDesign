# System Analysis and Design Project: Small Company Network Implementation
## Project Overview
This project implements a comprehensive network infrastructure for a small company using Cisco Packet Tracer for simulation. The implementation follows Agile methodology across six sprints.

## Project Specifications
- **Duration**: 12 weeks (2 weeks per sprint)
- **Team Size**: 4-6 students
- **Tools**: Cisco Packet Tracer
- **Methodology**: Agile with Scrum

## Agile Phase 1: Project Initiation and Requirements Gathering (Sprint 1)
### Objective
Define project scope, gather requirements, and develop initial design plan.

### Tasks
1. **Requirements Analysis**
   - Document network size requirements
   - Define number of users and departments
   - Identify peak usage periods
   - List security requirements
   - Define backup and redundancy needs

2. **Infrastructure Planning**
   - Server Requirements:
     * Database Server: 64GB RAM, 4 CPU cores
     * Web Server: 32GB RAM, 2 CPU cores
     * File Server: 128GB RAM, 4 CPU cores
     * ERP Server: 64GB RAM, 4 CPU cores
   
   - Network Equipment:
     * Cisco Catalyst 9200 Series switches
     * Cisco 4000 Series ISR routers
     * Cisco ASA 5500-X Series firewall
     * Cisco Aironet 9120 Access Points
     * NetApp FAS2750 NAS system

### Deliverables
- Requirements documentation
- Network topology diagram
- Initial budget estimation
- Risk assessment document

## Agile Phase 2: System Analysis (Sprint 2)
### Objective
Develop detailed technical specifications and network architecture.

### Tasks
1. **Network Architecture Design**
   ```
   Internet --> ASA Firewall --> Core Router --> 
   Distribution Switch --> Access Switches --> End Devices
   ```

2. **IP Addressing Scheme**
   - Server Network: 172.16.10.0/24
   - User Network: 192.168.1.0/24
   - WiFi Network: 192.168.2.0/24
   - Management Network: 10.10.10.0/24

3. **VLAN Design**
   - VLAN 10: Servers
   - VLAN 20: Staff
   - VLAN 30: WiFi
   - VLAN 99: Management

### Deliverables
- Network architecture document
- IP addressing scheme
- VLAN design document

## Agile Phase 3: Design and Prototyping (Sprint 3)
### Objective
Create configuration templates and prototype critical components.

### Tasks
1. **Switch Configuration Template**
   ```cisco
   enable
   configure terminal
   hostname SW-CORE
   vlan 10
   name Servers
   vlan 20
   name Staff
   vlan 30
   name WiFi
   vlan 99
   name Management
   ```

2. **Router Configuration Template**
   ```cisco
   enable
   configure terminal
   hostname RT-CORE
   interface GigabitEthernet0/0
   ip address 192.168.1.1 255.255.255.0
   no shutdown
   ```

3. **Firewall Basic Configuration**
   ```cisco
   enable
   configure terminal
   hostname ASA-MAIN
   interface GigabitEthernet0/0
   nameif outside
   security-level 0
   ip address dhcp
   ```

### Deliverables
- Configuration templates
- Prototype test results
- Updated network diagrams

## Agile Phase 4: System Configuration and Implementation (Sprint 4)
### Objective
Implement the network design in Cisco Packet Tracer.

### Tasks
1. **Server Implementation**
   - Configure blade servers with specified RAM and CPU
   - Set up operating systems and basic services
   - Configure network interfaces and IP addressing

2. **Network Device Configuration**
   - Configure VLANs on switches
   - Set up inter-VLAN routing
   - Configure DHCP services
   - Implement access control lists

3. **WiFi Implementation**
   - Configure Cisco Access Points
   - Set up WPA3 security
   - Configure guest network

### Deliverables
- Completed Packet Tracer simulation
- Configuration documentation
- Test plan

## Agile Phase 5: Testing and Validation (Sprint 5)
### Objective
Comprehensive testing of all network components.

### Tasks
1. **Connectivity Testing**
   ```cisco
   ping 192.168.1.1
   traceroute 172.16.10.10
   show ip interface brief
   show vlan brief
   ```

2. **Security Testing**
   - Firewall rule validation
   - Access control testing
   - WiFi security testing
   - VLAN separation testing

3. **Performance Testing**
   - Bandwidth testing
   - Latency checking
   - Load testing

### Deliverables
- Test results documentation
- Performance reports
- Security audit report

## Agile Phase 6: Documentation and Presentation (Sprint 6)
### Objective
Complete project documentation and prepare presentation.

### Tasks
1. **Documentation**
   - Network topology documentation
   - Configuration guides
   - Troubleshooting procedures
   - User manuals

2. **Presentation Preparation**
   - Create technical presentation
   - Prepare live demonstration
   - Document lessons learned

### Deliverables
- Complete project documentation
- Presentation slides
- Live demonstration
- Project completion report

## Project Success Criteria
1. All servers accessible and functioning
2. Successful VLAN implementation
3. Secure WiFi access
4. Functional firewall rules
5. Complete documentation
6. Successful live demonstration

## Group Collaboration Guidelines
1. Daily 15-minute stand-up meetings
2. Weekly sprint planning
3. End-of-sprint retrospectives
4. Use of project management tools
5. Regular communication with stakeholders

  
