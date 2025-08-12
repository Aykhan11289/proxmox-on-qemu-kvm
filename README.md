# Proxmox on QEMU/KVM with Debian & Windows VMs
 Proxmox Virtual Environment (Proxmox VE) is a powerful open-source platform for managing virtual machines and containers. It's widely used in production, but it's also perfect for creating a study lab to experiment and learn.

In this tutorial, we'll go one step deeper and run Proxmox inside QEMU/KVM. This 'nested' setup lets you try Proxmox without needing a dedicated server - all you need is a Linux host with virtualization enabled.

By the end of this guide, you'll have Proxmox installed and running in QEMU/KVM, plus two fully working virtual machines inside it: one Debian server and one Windows machine. You'll learn how to set up networking, upload ISOs, and configure your VMs from scratch. 

1. First we should download the iso image file from Proxmox's official website. For this we can use the terminal command: wget https://enterprise.proxmox.com/iso/proxmox-ve_8.4-1.iso or you can visit https://www.proxmox.com/en/downloads and download the current version.

2. Run the terminal command 'virt-manager' and create 'New virtual machine'. Set up 6GB RAM and 75GB hard drive (if you have more ram and hard disk capacity you can set up more). In the 'Operating system' section, choose Debian 12. Other sections leave 'default'. Start installation. After start you should see the Proxmox VE installation menu. Choose 'Install Proxmox VE(Graphical)'.
   ![image 1](images/00-install-proxmox.png)

   3. Read the 'End user license agreement' and press 'I agree'.
   ![image 2](images/01-install-proxmox.png)
