---
Status: In Progress
Summary: Overview of installed tools
---
Below is the list of all software tools with descriptions installed by default on the golden image.

- Chrome - Web browser
- Firefox - Web browser
- VLC Media Player - Media player
- Steam - Game launcher
- Spotify - Music service
- Discord - Chat service
- 7-Zip - Archive manager
- Notepad++ - Advanced text editor
- PuTTY - Remote connection tool
- Python 3.11.1 (python.org) - Code interpreter
- Anki - Flashcard software
- VirtualBox - Virtual Machine manager
- Teraterm - Remote connection tool
- VS Code - Simple code editor
- Git 2.39 - Version control software
- Wireshark - Network packet sniffer
- Angry IP Scan - Network device scanner
- Advance IP Scanner - Network device scanner
- Nmap - Network device scanner
- Packet Tracer 8.2 - Cisco network simulation tool

Below is an install script to install all tools with the exception of Cisco Packet Tracer

```
winget install Google.Chrome --scope machine -h

winget install Mozilla.Firefox --scope machine -h

winget install VideoLAN.VLC --scope machine -h

winget install Valve.Steam --scope machine -h

winget install Spotify.Spotify --scope machine -h

winget install Discord.Discord --scope machine -h

winget install 7zip.7zip --scope machine -h

winget install Notepad++.Notepad++ --scope machine -h

winget install PuTTY.PuTTY --scope machine -h

winget install Python.Python.3.12.3 --scope machine -h

winget install Anki.Anki --scope machine -h

winget install Oracle.VirtualBox --scope machine -h

winget install TeraTermProject.teraterm --scope machine -h

winget install Microsoft.VisualStudioCode --scope machine -h

winget install Git.Git --scope machine -h

winget install WiresharkFoundation.Wireshark --scope machine -h

winget install angryziber.AngryIPScanner --scope machine -h

winget install Famatech.AdvancedIPScanner --scope machine -h

winget install Insecure.Nmap --scope machine -h

pause
```