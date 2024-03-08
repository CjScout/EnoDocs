# Proxmox VM

Our proxmox server is considered a bare-metal VM server, the hypervisor runs directly on the hardware with no operating sysetm in between.

## Creating a VM

### Accessing Proxmox
1. Navigate to [https://192.168.10.8/](https://192.168.10.8) you MUST include https://

2. Use the following login credentials

    | Field    | Credential                       |
    |----------|----------------------------------|
    | Username | Student1                         |
    | Password | Pinkerton1!                      |
    | Realm    | Proxmox VE authentication server |
    | Language | English - English                |

3. Select Login

4. Select OK

### Creating the VM
1. Select Create VM in the top right

2. Give your VM a name and select Next

3. Click the box next to ISO Image and select an operating system to install

4. Select the relevant type and version of your operating system and select Next

5. Ensure your screen matches this photo EXACTLY then select Next

6. Increase disk size to 64 and select Next

7. Increase the number of cores to 2, and change type to host, then select Next

8. Increase memory to 4096, then select Next

9. Skip all settings in the network page as long they match below

10. Select Next and then Finish


### Final Setup
1. On the left side of the screen, click the arrow next to Cloud9 to see the list of VMs

2. Select your VM, then select Console

3. Select Start Now, and press Esc repeatedly until this screen appears

4. Using the arrows keys, move to Device Manager and press Enter.

5. Using the arrows keys, move to Secure Boot Configuration and press Enter.

6. Using the arrows keys, move to Attempt Secure Boot and press Enter so that the X disappears.

7. Press Enter, then F10, then Y, then press Escape until you are back to the starting screen.

8. Using the arrow keys, move to Reset and press Enter.

9. Install your OS and enjoy.
