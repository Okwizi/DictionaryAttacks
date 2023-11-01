# PROJECT: DictionaryAttacks {Dictionary Attack Simulation}
## Overview
### *What is a dictionary attack?*
A dictionary attack is a cyberattack to gain unauthorized access to a computer system or online account. It is a form of brute-force attack that relies on systematically trying many potential passwords or passphrases to guess the correct one.

## Prerequisites to use
__NOTE:__ This simulation has been performed on a Linux based OS *i.e, Kali GNU/Linux 2023.3 only*


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

Now go into the Virtual Machine's Settings and navigate to the Network tab.

### 3. Username and Password Lists *(already provided in this repo)*
These are `usernameshack.txt` and `testhack1.txt` which are used to recreate the attack.


### 4. Hydra
[Hydra](https://www.kali.org/tools/hydra/) comes preinstalled in Kali GNU/Linux.  
  
In an instance where Hydra isn't installed run: `sudo apt install hydra`  
  
To confirm Hydra is successfully installed run: `hydra`

## Usage
