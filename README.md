# WSL-common-configurations
A list of commonly used commands for Windows Subsystem for Linux

## Getting started
#### cmd> bash  
: This command will launch the linux subsystem from cmd

#### cmd> lxrun /uninstall /full
: Will uninstall the linux subsystem

#### cmd> lxrun /install
: Will install the linux subsystem

## Resetting password
#### cmd> lxrun /setdefaultuser root
#### cmd> bash
#### bash> passwd [username]
(give new password when prompted)
#### cmd> lxrun /setdefaultuser [username]


## Configuring ssh
#### bash> sudo apt-get install openssh-server
#### bash> sudo nano /etc/ssh/sshd_config
(change ssh port from 22 to 2222 or something else)
(change UsePrivilegeSeparation to 'no')
(change PasswordAuthentication to 'yes')
#### bash> sudo service ssh --full-restart
(remember to add a firewall rule to windows for chosen port)

## ssh usage
#### bash> ssh [username]@[ip-address] -p 2222
(or another port as specified)
