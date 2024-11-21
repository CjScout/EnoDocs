# Router On a Stick

Create VLANS on switchs

Configure Global Interface
- int (PORT)
- no shut
- exit

Configure sub Interfaces
- int (PORT).(VLAN)
- encapsulation dot1q (VLAN)
- ip address (default gateway for the VLAN)
- exit



