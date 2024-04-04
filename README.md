# Group project "Establish a Network Plan" #
Project made by group of 3 during our bootcamp 

- Project type: Group 
- Project file: *pkt file link*

# Project #

A group of 3 members developed a secure network in cisco packet tracer

## Team members ##

- Cosimo 
- Edjane 
- Bukunmi

Project Aim:

- Design a secure and efficient network for a client relocating to a new office
- Deliver a clear and structured documentation

Requirements

- DHCP server
- iSCSI server
- Active Directory and DNS server
- DMZ concept (through VLANs and ACLs)
- Four network sectors :
    - Management/Secretariat (5 workstations)
    - Study (8 workstations)
    - Production (10 workstations)
    - Support (2 sectors, 10 workstations each) 


Design 

We developed 2 different network plans and compared their functionalities: one with routers, the other with switches.

Router network

Physical connection: End devices for each sector were connected to a switch, similarly for a cluster of servers. These switches were connected to routers which route network traffic between them. The firewall was setup at the network terminal to inspect traffic in and out of the network. DMZ comprising the company's web server was isolated at the other end of the firewall.

Logical connection: Each sector was allotted a network IP address (see addressing table below). Dynamic addressing through DHCP was implemented for end devices except the servers.

Addressing table

| Name | Network | Subnet | VLAN | 
|------|---------|--------|------|
| SERVER | 192.168.4.0 | 255.255.255.248 | 1 |






Configurations Made


Addressing with DHCP


Pool Name
Start IP Address
Subnet Mask
Production
192.168.2.2
255.255.255.0
Management
182.168.0.2
255.255.255.224
Study
192.168.1.2
255.255.255.0
Support
172.16.0.2
255.255.0.0
serverPool
192.168.4.0
255.255.255.248



Virtual-LAN with Firewall

- Three vlans were setup to delineate the internal network from internet traffic and DMZ. The following priority levels were set:

