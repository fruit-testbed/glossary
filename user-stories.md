# User Stories of FRµIT Management System

## Roles

1. Sysadmin — a person who is an administrator of FRµIT clusters
2. User — a person who owns the RaspberryPi
3. Agent — a software agent that runs on the node



## Management Components

### 1. Operating System

- As a **sysadmin**, I can <u>build</u> an Operating System image based on a particular profile
- As a **user**, I can <u>download</u> an Operating System image
- As a **user**, I can <u>burn</u> the Operating System image on SD card
- As an **agent**, I can <u>periodically download</u> Operating System updates
- As an **agent**, I can <u>deploy</u> Operating System updates onto target node
- As a **sysadmin**, I can <u>build</u> a software repository based on a particular profile
- As a **user** or an **agent**, I can <u>download</u> the software from the software repository



### 2. Configuration

- As a **sysadmin** or **user**, I can <u>submit</u> a configuration profile for a particular node
- As an **agent**, I can <u>download</u> the configuration profile of a particular node
- As an **agent**, I can <u>deploy</u> the configuration profile onto target node
- As a **sysadmin**, I can <u>replace</u> ssh key files of a particular node



### 3. Monitoring

- As an **agent**, I can <u>periodically post</u> the monitoring data of a particular node
- As a **sysadmin** or **user**, I can <u>download</u> the monitoring data of particular nodes



### 4. Virtual Private Network (VPN)

- As a **user**, I can <u>register</u> a node to VPN
- As a **sysadmin** or **user**, I can <u>unregister</u> a node from VPN
- As an **agent**, I can <u>connect</u> a node to VPN
- As a **user**, I can <u>download</u> credentials and config files to connect to VPN
- As a **sysadmin** or **user**, I can <u>ssh</u> to the node via VPN
