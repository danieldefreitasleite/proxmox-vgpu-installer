---------------------------------------------------------------------------------------------------------------------------------------------------------
TO RUN THE SCRIPT USE THE FOLLOWING COMMANDS:

If GIT is not already installed: apt install -y git

1st run:

cd ~ && git clone https://github.com/danieldefreitasleite/proxmox-vgpu-installer.git && cd proxmox-vgpu-installer && bash proxmox-installer.sh

2nd run (after reboot)
cd ~ && cd proxmox-vgpu-installer && bash proxmox-installer.sh

---------------------------------------------------------------------------------------------------------------------------------------------------------
ORIGINAL INSTRUCTIONS ARE IN:

https://gitlab.com/polloloco/vgpu-proxmox

---------------------------------------------------------------------------------------------------------------------------------------------------------

This is a little Bash script that configures a Proxmox 7 or 8 server to use Nvidia vGPU's. 

For further instructions see my blogpost at https://wvthoog.nl/proxmox-7-vgpu-v3/

Changes in version 1.1
- Added new driver versions
    16.2
    16.4
    17.0
- Added checks for multiple GPU's
- Added MD5 checksums on downloaded files
- Created database to check for PCI ID's to determine if a GPU is natively supported
- If multiple GPU's are detected, pass through the rest using UDEV rules
- Always write config.txt to script directory
- Use Docker for hosting FastAPI-DLS (licensing)
- Create Powershell (ps1) and Bash (sh) files to retrieve licenses from FastAPI-DLS
