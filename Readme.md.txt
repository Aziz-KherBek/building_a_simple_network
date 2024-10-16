# Hackers Poulette Lab

## Overview
This repository contains the network configuration and setup for Hackers Poulette, a startup.

## Objective
To create a scalable network infrastructure with three hosts connected through a Cisco switch.


## Configuration Details
- **Devices Used**:
  - Cisco 2960 Switch
  - 3 PCs (Windows 10)
  - 2 Routers 2911
  - Server-PT
- **IP Addressing Scheme**:
  - PC1,PC2,PC3: Dynamic address using DHCP (network :192.168.1.0 /24)Provided by ROUTER 4
  - Router 4: interface g0/1 192.168.1.1 /24
	      interface g0/0 40.0.0.1/30

  - Router 5: interface g0/0 40.0.0.2/30
	      interface g0/1 8.8.8.1 /8

   - Server : interface fa0 8.8.8.20 /8

## Report
Configuration Details:
	Device Setup
		Switch: Cisco 2960
		Router: Cisco Router with DHCP and DNS configured.(ROUTER 4)

	DHCP Configuration on Router:
		The router was configured to serve as a DHCP server, automatically assigning IP addresses to the connected PCs:

		DHCP Range: 192.168.1.100 to 192.168.1.199
		Subnet Mask: 255.255.255.0
		Default Gateway: 192.168.1.1
	Testing Connectivity:
		To verify that the network configuration is successful, the ping utility was used to test connectivity between devices:

		Ping Results:
			PC1 to PC2: Successful
			PC1 to PC3: Successful
			PC2 to PC3: Successful
			All PCs can ping the router (192.168.1.1).
			All PCs can ping the Server (8.8.8.20).
Conclusion

The network setup for Hackers Poulette was successfully completed, providing a scalable solution for the current team of three. All devices can communicate with each other and access the internet, fulfilling the initial objectives of the project. Further expansions can be easily implemented as the company grows.

Future Recommendations

 	-Consider adding more PCs and switches as the team expands.
	-Implement security features such as firewall settings and access control lists (ACLs) to protect sensitive information.
	-Solve the DNS problem on ROUTER 4 .
	

## Getting Started
To replicate this lab, ensure you have Cisco Packet Tracer installed and load the `.pkt` file in the repository.


