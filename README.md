# small-business-network-lab
## Objective 
We setup a small office computer network and tested connectivity between devices. We also simulated and troubleshooting a connectivity problem caused by an incorrect default gateway.
## Environment & Tools 
Cisco Packet tracer- Used to create  a virtual environment simulating a small office network configuration 
PC0- Configured the computer's IPv4 address, subnet mask, and default gateway
PC1- Configured the computer IPv4 address, subnet mask, and default gateway
Switch - connected to PC0 and PC1 to the local network
Router - configured as the gateway for the network and used to provide communication between networks.
## Network Configuration
PC0 - IPv4 address 192.168.10.20 with a /24 subnet mask
PC1 - IPv4 address 192.168.10.10 with a /24 subnet mask
Router Gigabit Ethernet 0/0 configured with a IPv4 address 192.168.10.1 with a /24 subnet mask
## Connectivity Testing
From PC0 I used ping to test connectivity to the router at 192.168.10.1, The test was successful with 0% packet loss
From PC1 I used ping to test connectivity to PC0 at 192.168.10.20. The test was successful with 0% packet loss
From PC1 I test connectivity to the router loopback address at 192.168.20.1. The first test failed with 100% packet loss
## Troubleshooting 
PC1 was able to commuicate with PC0 because both devices were on the 192.168.10.0 /24 network.
PC1 was able to reach the router 192.168.10.1 interface.
PC1 could not initially reach the router 192.168.20.1 loopback address and received 100% packet loss.
I configured Loopback 0 on the router with the 192.168.20.1/24 address to simulate a second network.
After configuring the interface I tested the connection again from PC1 using ping 192.168.20.1.
The second test was successful with 4 packets received and 0% packets loss.
## Results
Successfully tested connectivity between PC0 and PC1 on the same subnet.
Successfully tested connectivity from the PC's to the router GigabitEthernet0/0 interface.
Identified that the router loopback 0 interface was initially reachable.
Configured loopback0 with the 192.168.20.1/24 address.
Retested connectivity from PC1 to 192.168.20.1 and received 4 replies with 0% packet loss.
The troubleshooting test confirmed connectivity to the second network after the router interface was configured.
## What I learned from this
How to configure IPv4 address on end devices 
How to configure a router interface using cisco IOS commands
How to use ping to troubleshoot network connectivity
How to identify connectivity problems between different networks
How to use cisco packet tracer to build and troubleshoot a simulated business network.
