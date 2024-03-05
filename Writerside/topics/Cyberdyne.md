# Cyberdyne
Cyberdyne is the core of the CIS class. It runs Windows Server 2019, and provides Domain Services to the entire class.
## User Accounts
All user accounts are stored on Cyberdyne, and allows a student to log in to their account on any computer enrolled in the domain.
## DNS
Cyberdyne also provides domain DNS related services, which are forwarded from [Hampstead](Hampstead.md).
## DHCP
Cyberdyne provides DHCP for both the Class and Lab [networks](Detailed-Network-Explaination.md). Server also has it enabled because VMs on Cloud9 use that VLAN. DHCP Configs:

| VLAN       | Range              | Router       | DNS           |
|------------|--------------------|--------------|---------------|
| ClassVLAN  | 192.168.20.100-254 | 192.168.20.1 | 192.168.30.12 |
| LabVLAN    | 192.168.10.50-254  | 192.168.10.1 | 192.168.30.12 |
| ServerVLAN | 192.168.30.50-254  | 192.168.30.1 | 192.168.30.12 |