# VagrantShift
SIFT Vagrant Environment

This project provides a Vagrant environment for setting up the SANS Investigative Forensic Toolkit (SIFT) on a virtual machine.
The Vagrantfile in this repository will automatically install SIFT on a Ubuntu virtual machine using the SIFT SaltStack formula.

Requirements
To use this Vagrant environment, you'll need to have the following software installed on your host machine:

VirtualBox: Virtualization software for creating and running virtual machines. You can download it from the VirtualBox website.
Vagrant: A command-line tool for managing virtual machines. You can download it from the Vagrant website.
Chocolatey (Windows only): A package manager for Windows. You can download it from the Chocolatey website.
Usage
Linux
Install VirtualBox and Vagrant by downloading and running the installation packages for your Linux distribution.

Clone this repository or download the Vagrantfile to your local machine.

Open a terminal and navigate to the directory where the Vagrantfile is located.

Run the following command to start the virtual machine:

Copy code
vagrant up
Once the virtual machine has started and the SIFT installation is complete, you can log in to it by running the following command:

Copy code
vagrant ssh
Windows
Install Chocolatey, VirtualBox, and Vagrant by opening a PowerShell prompt as Administrator and running the following commands:

sql
Copy code
Set-ExecutionPolicy Bypass -Scope Process -Force; `
iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
choco install virtualbox -y 
choco install vagrant -y
Clone this repository or download the Vagrantfile to your local machine.

Open a Command Prompt or PowerShell prompt and navigate to the directory where the Vagrantfile is located.

Run the following command to start the virtual machine:

Copy code
vagrant up
Once the virtual machine has started and the SIFT installation is complete, you can log in to it by running the following command:

Copy code
vagrant ssh
License
This project is licensed under the MIT License.
