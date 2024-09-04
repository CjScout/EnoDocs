# Networking Overview
## Components
The core networking infrastructure is made up of the following devices
- 1x [[Mikrotik CRS309-1G-8S+IN]]
- 1x [[Cisco WS-C3650-48FQ-S Catalyst 3650]]
- 6x [[TRENDnet TEG-3102WS]]

## Architecture
### Hardware
The [[Mikrotik CRS309-1G-8S+IN]] functions as our core networking switch. It 

### IP Scheme
The room is divided into VLANs, designed to separate class and lab traffic and prevent downtime for the [Work PCs](/PCs/Work%20PCs/General%20Information). The VLANs and IP address structure are below.

| VLAN Name | VLAN ID | Default Gateway | DHCP Range        | DNS Server   |
| --------- | ------- | --------------- | ----------------- | ------------ |
| Lab       | 10      | 192.168.10.1    | 192.168.10.50-255 | 1.1.1.1      |
| Class     | 20      | 192.168.20.1    | 192.168.10.20-255 | 192.168.30.2 |
| Server    | 30      | 192.168.30.1    | N/A               | 192.168.30.2 |
| Security  | 40      | 192.168.40.1    | N/A               | 1.1.1.1      |
There are additional addresses used for backend device communication:

| Device 1                     | IP           | Device 2                                | IP          |
| ---------------------------- | ------------ | --------------------------------------- | ----------- |
| [[Comcast Modem]]            | 10.1.10.1    | [[Netgate 1100 pfSense Firewall]]       | 10.1.10.35  |
| [[Mikrotik CRS309-1G-8S+IN]] | 192.168.1.10 | [[Netgate 1100 pfSense Firewall]]       | 192.168.1.1 |
| [[Mikrotik CRS309-1G-8S+IN]] | 192.168.5.1  | [[Cisco WS-C3650-48FQ-S Catalyst 3650]] | 192.168.5.2 |