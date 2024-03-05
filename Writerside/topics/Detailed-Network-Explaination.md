# Detailed Network Explanation

A detailed look at the networking that runs the CIS room.  
[Quick Overview](General-Overview.md)

Comcast Modem: **10.1.10.1**  
runs to

Firewall WAN Port: **10.1.10.35**

Firewall LAN Port: **192.168.1.1**  
runs to Layer 3 Switch

| VLAN ID | IP Address Range    | Router Address | Name - Purpose                                                                                                 |
|---------|---------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| 10      | 192.168.10.0-255    | 192.168.10.1   | Lab - Mess around here, no consequences                                                                        |
| 20      | 192.168.20.0-255    | 192.168.20.1   | Class - Regular Class network, do **not** mess around here, regular class activities should not be interrupted |
| 30      | 192.168.30.0-255    | 192.168.30.1   | Server - All long-term servers are here, **NEVER** mess around here                                            |
| 40      | 192.168.40.0-255    | 192.168.40.1   | Security - Used for Level 3 Cybersecurity stuff, basically never used but nice to have                         |

They all utilize subnet mask **255.255.255.0** and **192.168.30.12** (Hampstead) for DNS requests.