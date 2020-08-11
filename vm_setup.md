## EDURange Virtual Machine Set Up Walkthrough

This is a walkthrough for EDURange users who would like to run the EDURange application on a Windows machine. This walkthrough will guide you through the installation and setup process for downloading virtual machine software and installing ubuntu linux on it.


#### Virtual Box Set Up

1. Before installing Virtual Box you should download the latest [LTS version of Ubuntu](https://ubuntu.com/download/desktop). This download will probably take a while.

2. Go to the [Virtual Box website](https://www.virtualbox.org/wiki/Downloads) and download the latest version of Virtual Box for the os on your computer.

3. Run the downloaded executable file. You may change the installation path to your preference.

4. Once Virtual Box has been installed. Open the application and you should see the Virtual Box Manager. Click the `New` button to create a new virtual machine.

5. On the Create Virtual Machine menu enter a name for your vitual machine, and set the type of the machine to Linux. Select a version for the virtual machine, for EDURange select the Ubuntu with the same bits as your host computer. You can change the machine folder to your preference.

6. After clicking next you will be asked to select how much RAM to give the VM. Virtual Box recommends 1GB (1024 MB), but for EDURange requires 4GB (4096 MB).

7. The next page asks you to select a hard disk. Select `Create a virtual hard disk now`. Then select VDI (VirtualBox Disk Image), Dynamically allocated, and use the recommended disk image size.

8. With your EDURange virtual machine selected, scroll down to the storage section and click on `[Optical Drive] Empty` the select `Choose a disk file` from the drop down menu. You can then select your Ubuntu ISO file from where you downloaded it on your computer.

9. You can now start you virtual machine. Upon the virtual machine powering up, you will also begin the Ubuntu installation process.


#### Ubuntu Installation Set Up

10. On starting the Ubuntu installation process, select your prefered language and click Install Ubuntu.

11. Choose your prefered keyboard layouts. 

12. Use the default options of `Normal installation` and `Download updates while installing Ubuntu`. 

13. Select the default option for Installtion option which is `Erase disk and install Ubuntu`. Do not worry about this erasing your computers file, as it is contained by the vm.

14. Select your time zone.

15. Enter a your name, what you want your computer to be named, your username, and then your password for this virtual machine.

16. Ubuntu will now start installing on the virtual machine. The installation process may take a while.

17. Once the installation has been completed, you will have to restart the vm before you can log in.
