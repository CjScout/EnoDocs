---
Status: To Do
---
# Cyberdyne

# Purpose
## Overview
Cyberdyne provides core room functionality. This is the most important server in the room and should only be modified on a need-to basis.
## Services
### Active Directory
#### Overview
Cyberdyne provides Microsoft Active Directory domain/login services to the room.
#### Domain Structure
##### Domain
The primary domain for the room is **skynet.prvt**.
##### Organizational Units
Computers are all put within a single Organization Unit (OU).
Users are in an OU called Students, which is sub divided by year of graduation. Additionally there is a folder called Admins for student administrators.
##### Groups
Users are also added to groups based on which class they are in, such as Level 1,2,3, or Cybersecurity.
### Domain Name System (DNS)
#### Overview
Cyberdyne also provides Active Directory related DNS services.