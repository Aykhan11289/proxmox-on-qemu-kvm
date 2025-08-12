   # Proxmox on QEMU/KVM with Debian & Windows VMs
 Proxmox Virtual Environment (Proxmox VE) is a powerful open-source platform for managing virtual machines and containers. It's widely used in production, but it's also perfect for creating a study lab to experiment and learn.

In this tutorial, we'll go one step deeper and run Proxmox inside QEMU/KVM. This 'nested' setup lets you try Proxmox without needing a dedicated server - all you need is a Linux host with virtualization enabled.

By the end of this guide, you'll have Proxmox installed and running in QEMU/KVM, plus two fully working virtual machines inside it: one Debian server and one Windows machine. You'll learn how to set up networking, upload ISOs, and configure your VMs from scratch. 

1. First we should download the iso image file from Proxmox's official website. For this we can use the terminal command: wget https://enterprise.proxmox.com/iso/proxmox-ve_8.4-1.iso or you can visit https://www.proxmox.com/en/downloads and download the current version.

2. Run the terminal command 'virt-manager' and create 'New virtual machine'. Set up 6GB RAM and 75GB hard drive (if you have more ram and hard disk capacity you can set up more). In the 'Operating system' section, choose Debian 12. Other sections leave 'default'. Start installation. After start you should see the Proxmox VE installation menu. Choose 'Install Proxmox VE(Graphical)'.
   ![image 1](images/00-install-proxmox.png)

3. Read the 'End user license agreement' and press 'I agree'.
   ![image 2](images/01-install-proxmox.png)

4. Choose 'Target Harddisk' and press 'Next'.
   ![image 3](images/02-install-proxmox.png)

5. Select the 'Country', 'Time zone' and 'Keyboard layout' and press 'Next'.
   ![image 4](images/03-install-proxmox.png)
   
6. Enter administration password and valid email address, then press 'Next'.
   ![image 5](images/04-install-proxmox.png)

7. Select 'Management Interface', if you have FQDN, write it either just leave the default. Other network options just leave the default, then press 'Next'.
   ![image 6](images/05-install-proxmox.png)

8. Check the 'Summary' and press 'Install'.
   ![image 7](images/06-install-proxmox.png)

9. The installation process.
   ![image 8](images/07-install-proxmox.png)

10. After installation, you should see the IP address and port number. It will automatically reboot.
   ![image 9](images/08-install-proxmox.png)

11. After reboot it will run in command line mode. Open on your host machine web browser and access the IP address and port which have been given before.
   ![image 10](images/09-install-proxmox.png)

12. It will open Proxmox VE login window. In the username field enter 'root', in the password field enter your password, then press 'login'.
   ![image 11](images/10-install-proxmox.png)

13. Whenever you start Proxmox VE, the 'No valid subscription' window always shows up, just press 'OK'.
   ![image 12](images/11-install-proxmox.png)

14. Click the storage 'local' on node to see 'Summary'.
   ![image 13](images/12-install-proxmox.png)

15. Click the 'ISO Images' to see uploaded images.
   ![image 14](images/13-install-proxmox.png)

16. Click on 'Upload', it will open the 'Upload' window, press 'Select' to select iso from local files.
   ![image 15](images/14-install-proxmox-upload-debian-image.png)

17. It will show uploadable file. 
   ![image 16](images/15-install-proxmox-upload-debian-image.png)

18. If you see 'error', try to change the ownership of the file.
   ![image 17](images/17-install-proxmox-upload-debian-image-error.png)

19. After successfully uploading, you will get a 'TASK OK' output.
   ![image 18](images/18-install-proxmox-upload-debian-image-success.png)

20. Click the 'Create VM' button, select 'Use CD/DVD disk image file(iso), from the drop-down menu select your local iso image file and press the 'Next'.
   ![image 19](images/20-install-proxmox-create-debian-vm.png)

21. The 'System' settings leave default and press 'Next'.
   ![image 20](images/21-install-proxmox-create-debian-vm.png)

22. The 'Disks' settings leave default and press 'Next'.
   ![image 21](images/22-install-proxmox-create-debian-vm.png)

23. The 'CPU' settings leave default(you can add more cores if you want) and press 'Next'.
   ![image 22](images/23-install-proxmox-create-debian-vm.png)


24. For Debian a minimum of 1GB of RAM is suggested for a basic desktop installation, but 2GB or more is preferable. After set up 'Memory' settings press 'Next'.
   ![image 23](images/24-install-proxmox-create-debian-vm.png)


25. The 'Network' settings leave default and press 'Next'.
   ![image 24](images/25-install-proxmox-create-debian-vm.png)

26. Check all options and click the 'Finish' button.
   ![image 25](images/26-install-proxmox-create-debian-vm.png)

27. Click the 'Start' button to create a Virtual Machine.
   ![image 26](images/27-install-proxmox-create-debian-vm.png)

28. Choose 'console' to see the installation menu. Select which installation method is apropriate for you.
   ![image 27](images/29-install-proxmox-install-debian-vm.png)

29. The installation process of the Debian virtual machine.
   ![image 28](images/30-install-proxmox-install-debian-vm.png)

30. Booting after installation.
   ![image 29](images/33-install-proxmox-run-debian-vm.png)

31. Checking the hostname and username of a Virtual Machine.
   ![image 30](images/35-install-proxmox-final-check-debian-vm.png)


32. Click on 'Upload', it will open the 'Upload' window, press 'Select' to select iso from local files.
   ![image 31](images/37-install-proxmox-upload-windows-10-image.png)


33. After successfully uploading, you will get a 'TASK OK' output. 



34. Click the 'Create VM' button, select 'Use CD/DVD disk image file(iso), from the drop-down menu select your local iso image file and press the 'Next'.



35. The 'System' settings leave default and press 'Next'.



36. The 'Disks' settings leave default(If you will challenged to boot a virtual machine, just change 'SCSI0' from drop-down menu to 'SATA'.) and press 'Next'.



37. The 'CPU' settings leave default(you can add more cores if you want) and press 'Next'.



38. For Windows 10 a minimum of 2GB of RAM is suggested for a basic desktop installation, but 4GB or more is preferable. After set up 'Memory' settings press 'Next'.



39. The 'Network' settings leave default and press 'Next'.



40. Check all options and click the 'Finish' button.



41. Click the 'Start' button to create a Virtual Machine.



42. Choose 'console' to see the installation menu. Select which installation method is apropriate for you.



43. Booting Windows 10 virtual machine.



44. Overview of the datacenter with all nodes and virtual machines.



45. The node summary.



46. The Debian Virtual Machine summary.



47. The Windows 10 Virtual Machine summary.



