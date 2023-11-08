# PROJECT: DictionaryAttacks {Dictionary Attack Simulation}
## Overview
### *What is a dictionary attack?*
A dictionary attack is a cyberattack to gain unauthorized access to a host computer system(s) or online account(s). It is a form of brute-force attack that takes input from many potential passwords, passphrases, or usernames and tries to guess the correct one. 

The simulation discussed in this project involves initiating a dictionary attack on a *Host-only network VM* i.e. Mininet from the host machine. 

## Prerequisites to use
__NOTE:__ This simulation has been performed on a Linux based OS *i.e, Kali GNU/Linux 2023.3 only* 

Any code executed in a terminal is recommended to be executed with elevated privileges.


### 1. VirtualBox
[VirtualBox](https://www.virtualbox.org/wiki/Linux_Downloads) is a virtualization program that will run the virtual environment where we intend to initiate the dictionary attack. 

Open an elevated terminal where the download is located and install using `apt install ./virtualbox-<version>.deb` 

Example: `apt install ./virtualbox-7.0_7.0.12-159484~Ubuntu~jammy_amd64.deb` 

After installation run `apt install update` and then `apt install upgrade -y`


### 2. Mininet Virtual Machine (Mininet VM)
[Mininet VM](https://github.com/mininet/mininet/releases/) (available as `-ovf.zip` files) is a virtualization program that enables computer networks to be created where the dictionary attack will be performed. 

Extract the `.zip` to a desired location to get the `.ovf` file and open the VirtualBox application. 

Click on "File" then "Import Appliance". 

In the pop-up ensure that "Local File System" is selected in the "Source" section. 

Click on the folder icon to choose the `.ovf` that was extracted earlier and click next. 

Set up the appliance if needed (Recommended to leave settings as default) then click finish. 

Now go to the tools tab (listed above the Mininet VM) and navigate to the host-only networks tab. 

Click on the create icon and an adapter called *vboxnet0* will appear. You can configure the adapter if you need to. Click on apply. 

Now navigate back to your Mininet VM and click on the settings gear icon to open the VM's settings. 

Navigate to the "Network" Tab and enable "Adapter 1" and "Adapter 2" (Adapters 3 and 4 should remain disabled). 

Go into Adapter 1 and change the "Attached to:" option to `NAT`. 

Go into Adapter 2 and change the "Attached to:" option to `Host-only Adapter` and select `vboxnet0` as the name from the provided Dropbox. This allows other programs running on your host computer to connect to the VM using SSH. 

Other VM settings may be changed to the user's liking. 

### 3. Username and Password Lists *(already provided in this repo)*
These are `usernameshack.txt` and `testhack1.txt` used to recreate the attack.


### 4. Hydra
[Hydra](https://www.kali.org/tools/hydra/) comes preinstalled in Kali GNU/Linux.  
  
In an instance where Hydra isn't installed run: `sudo apt install hydra`  
  
To confirm Hydra is successfully installed run: `hydra`

## Usage
