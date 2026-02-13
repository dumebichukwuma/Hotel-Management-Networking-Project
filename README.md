# Hotel-Management-Networking-Project
This project features a hierarchical, three-floor enterprise network designed and simulated in Cisco Packet Tracer. The architecture focuses on departmental segmentation through VLANs, high-availability routing, and seamless wireless integration.
Network Architecture & Features
1. Core Routing & OSPF Configuration
The backbone of the network consists of three Cisco 2911 ISR Routers connected in a mesh topology via serial interfaces.
Routing Protocol: OSPF (Open Shortest Path First) is implemented across all routers to ensure dynamic path selection and rapid convergence.
Area Design: All routers reside in Area 0 (Backbone), allowing for efficient route propagation between the 10.10.x.x/30 point-to-point links.
Redundancy: The triangle topology ensures that if one serial link fails, OSPF automatically reroutes traffic through the remaining functional paths.
2. Logical Segmentation (VLANs)
To ensure security and reduce broadcast traffic, the network is segmented into departmental VLANs using a Router-on-a-Stick configuration:
Floor,Department,VLAN ID,Subnet
1st Floor,"Logistics, Store, Reception","60, 70, 80",192.168.6.0 - 8.0/24
2nd Floor,"Sales, HR, Finance","30, 40, 50",192.168.3.0 - 5.0/24
3rd Floor,"IT, Admin","10, 20",192.168.1.0 - 2.0/24
3. Switching & Access Layer
Layer 2 Infrastructure: Each floor utilizes Cisco 2960 Catalyst Switches to manage end-device connectivity.
Wireless Connectivity: Integrated Access Points provide mobility for laptops, tablets, and smartphones, bridged directly into their respective floor's VLANs.
End Devices: The network supports a mix of PCs, Network Printers, and mobile hardware.
