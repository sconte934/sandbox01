# Sandbox Environment

### Install the following to the local host (windows):

| Name          | Requirements     | Link  |
| ------------- |:----------------:|:-----:|
| Vagrant       | version 2.2.6    | [link](https://releases.hashicorp.com/vagrant/2.2.6/vagrant_2.2.6_x86_64.msi) |
| VirtualBox    | version 6.0.14   | [link](https://download.virtualbox.org/virtualbox/6.0.14/VirtualBox-6.0.14-133895-Win.exe) |
| Wireshark     | version 3.2.0    | [link](https://1.na.dl.wireshark.org/win64/Wireshark-win64-3.2.0.exe) |
| Atom          | version 1.42.0   | [link](https://github.com/atom/atom/releases/download/v1.42.0/AtomSetup-x64.exe) |
| Git           | version 2.24.1.2 | [link](https://github.com/git-for-windows/git/releases/download/v2.24.1.windows.2/Git-2.24.1.2-64-bit.exe) |
| Putty         | version 0.72     | [link](https://the.earth.li/~sgtatham/putty/latest/w64/putty-64bit-0.73-installer.msi) |

### Basic Setup Requirements:

1. Github setup (Clone, Configuration & SSH Keys)
    * Open "Git Bash"
        * Execute ``` git clone https://github.com/sconte934/sandbox01.git ```
        * ``` cd sandbox01 ```
        * ``` git config --global user.name "Your Name Here" ```
        * ``` git config --global user.email "Your E-mail Here" ```
        * ``` ssh-keygen -t rsa -C "Your E-mail Here" ```
        * ``` cat /c/Users/Conte/.ssh/id_rsa.pub ```
            * Copy the output
    * Open a browser and go to https://github.com/settings/ssh/new
        * Fill in a title "My_XPS_Laptop"
        * Paste the ssh key output that was copied earlier
        * Click "Add SSH key"
    * Go back to the "Git Bash" window and execute
        * ``` ssh -T git@github.com ```
2. Disable Hyper-V (VirtualBox conflict resolution)

### Vagrant box image used for setup:
| Name              | Type                     |  Vagrant Box                 |
| ----------------- |:------------------------:| :---------------------------:|
| Cumulus Linux     | Network Operating System | [CumulusCommunity/cumulus-vx](https://app.vagrantup.com/CumulusCommunity/boxes/cumulus-vx)|
| Ubuntu 18.04 LTS  | Operating System         | [ubuntu/bionic64](https://app.vagrantup.com/ubuntu/boxes/bionic64)|
| Ubuntu 16.04 LTS  | Operating System         | [ubuntu/xenial64](https://app.vagrantup.com/ubuntu/boxes/xenial64)
* Ubuntu 16.04 LTS was utilized to work around the "ip forwarding" persistence bug on fw1 [link](https://bugs.launchpad.net/ubuntu/+source/procps/+bug/50093)

### Software Elements

| Name              | Type                     | Information Link                |
| ----------------- |:------------------------:|:---------------------------:|
| vault             | Secure Key Management    |                             |
| ansible           | Configuration Management |                             |
| GitHub Actions    | CI, Pipeline Management  |                             |
| docker            | Container Engine         |                             |
| nginx             | Web Server               |                             |
| mysql             | Database                 |                             |
| HA Proxy          | Load Balancer            |                             |
| iptables          | Firewall                 |                             |

### Configuration Manual

1. [wiki](https://github.com/sconte934/sandbox01/wiki)

### Topology

![Network Topology](diagram.png)
