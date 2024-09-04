# Networking Overview
## Components
The core networking infrastructure is made up of the following devices
- 1x [[Mikrotik CRS309-1G-8S+IN]]
- 1x [[Cisco WS-C3650-48FQ-S Catalyst 3650]]
- 6x [[TRENDnet TEG-3102WS]]

## Architecture
### Hardware
The [[Mikrotik CRS309-1G-8S+IN]] functions as our core networking switch. It is capable of both layer 2 and layer 3 routing. See [here](/Network%20Architecture/Equipment/Mikrotik%20CRS309-1G-8S+IN) for exact configuration details.

The [[Mikrotik CRS309-1G-8S+IN]] has 8 SFP+ 10G ports. Ports 1-3 are each linked to a [[TRENDnet TEG-3102WS]].

Each [[TRENDnet TEG-3102WS]] has 8 2.5G Ethernet ports, these are connected to the patch panel where the Work PC's Ethernet is terminated.

Port 4 is used for the high speed storage server.

Port 5 is linked to a [[TRENDnet TEG-3102WS]]. This switch is used to provide 2.5G speeds to each server for the room.

Port 6 is linked to the [[Cisco WS-C3650-48FQ-S Catalyst 3650]], a separate layer 3 capable switch used for the lab VLAN.

Port 7 is configured as a mirror port, and is used for traffic monitoring by the security onion server.

Port 8 is our upstream connection, it is linked to the [[Netgate 1100 pfSense Firewall]].

The single ethernet port is used for management by the WinBox utility.
### IP Scheme
The room is divided into VLANs, designed to separate class and lab traffic and prevent downtime for the [Work PCs](/PCs/Work%20PCs/General%20Information). The VLANs and IP address structure are below.

| VLAN Name | VLAN ID | Default Gateway | DHCP Range        | DNS Server   |
| --------- | ------- | --------------- | ----------------- | ------------ |
| Lab       | 10      | 192.168.10.1    | 192.168.10.50-255 | 1.1.1.1      |
| Class     | 20      | 192.168.20.1    | 192.168.10.20-255 | 192.168.30.2 |
| Server    | 30      | 192.168.30.1    | N/A               | 192.168.30.2 |
| Security  | 40      | 192.168.40.1    | N/A               | 1.1.1.1      |
There are additional addresses used for backend device communication:

| Device 1                     | IP           | Device 2                                | IP             | Purposed              |
| ---------------------------- | ------------ | --------------------------------------- | -------------- | --------------------- |
| [[Comcast Modem]]            | 10.1.10.1    | [[Netgate 1100 pfSense Firewall]]       | 10.1.10.35     | Link to outside modem |
| [[Mikrotik CRS309-1G-8S+IN]] | 192.168.1.10 | [[Netgate 1100 pfSense Firewall]]       | 192.168.1.1    | Link to firewall      |
| [[Mikrotik CRS309-1G-8S+IN]] | 192.168.5.1  | [[Cisco WS-C3650-48FQ-S Catalyst 3650]] | 192.168.5.2    | Link to lab switch    |
| [[Mikrotik CRS309-1G-8S+IN]] | 192.168.88.1 | Any PC                                  | 192.168.88.XXX | Management address    |
