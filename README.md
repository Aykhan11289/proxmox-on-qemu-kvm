# Proxmox on QEMU/KVM with Debian & Windows VMs
 Proxmox Virtual Environment (Proxmox VE) is a powerful open-source platform for managing virtual machines and containers. It's widely used in production, but it's also perfect for creating a study lab to experiment and learn.

In this tutorial, we'll go one step deeper and run Proxmox inside QEMU/KVM. This 'nested' setup lets you try Proxmox without needing a dedicated server - all you need is a Linux host with virtualization enabled.

By the end of this guide, you'll have Proxmox installed and running in QEMU/KVM, plus two fully working virtual machines inside it: one Debian server and one Windows machine. You'll learn how to set up networking, upload ISOs, and configure your VMs from scratch. 

This project shows how to:
-   Perequisites
-   Downloading ISOs
-   Install **Proxmox VE** inside **QEMU/KVM**
-   Configure basic networking
-   Create a Debian VM
-   Create a Windows VM
-   Final Checks and Tips
