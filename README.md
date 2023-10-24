# PROJECT: DictionaryAttacks {Dictionary Attack Simulation}
## Overview
### *What is a dictionary attack?*
A dictionary attack is a cyberattack to gain unauthorized access to a computer system or online account. It is a form of brute-force attack that relies on systematically trying many potential passwords or passphrases to guess the correct one.

## *Prerequisites to use*
__NOTE:__ This simulation has been performed on a Linux based OS *i.e, Kali GNU/Linux 2023.3 only*

### 1. Mininet Virtual Machine (Mininet VM)
[Mininet VM](https://github.com/mininet/mininet/releases/) (available as `-ovf.zip` files) is a virtualization program that enables computer networks to be created where the dictionary attack will be performed.


### 2. VirtualBox
[VirtualBox](https://www.virtualbox.org/wiki/Linux_Downloads) is a virtualization program that will run the virtual environment where we intend to initiate the dictionary attack.


### 3. Username and Password Lists *(already provided in this repo)*
These are `usernameshack.txt` and `testhack1.txt` which are used to recreate the attack.


### 4. Hydra
[Hydra](https://www.kali.org/tools/hydra/) comes preinstalled in Kali GNU/Linux.  
  
In an instance where Hydra isn't installed run: `sudo apt install hydra`  
  
To confirm Hydra is successfully installed run: `hydra`
