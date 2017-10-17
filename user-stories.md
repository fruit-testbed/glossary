# User Stories of FRµIT Management System

## Roles

1. Sysadmin — a person who is an administrator of FRµIT clusters
2. User — a person who owns the RaspberryPi
3. Agent — a software agent that runs on the node



## User Stories

### 1. Operating System

- [ ] As a **sysadmin**, I can build an Operating System image based on a particular profile
- [x] As a **user**, I can download an Operating System image
- [x] As a **user**, I can burn the Operating System image on SD card
- [ ] As an **agent**, I can periodically download Operating System updates
- [ ] As an **agent**, I can deploy Operating System updates onto target node
- [ ] As a **sysadmin**, I can build a software repository based on a particular profile
- [x] As a **user** or an **agent**, I can download the software from the software repository



### 2. Configuration

- [ ] As a **sysadmin** or **user**, I can submit a configuration profile for a particular node
- [ ] As an **agent**, I can download the configuration profile of a particular node
- [x] As an **agent**, I can deploy the configuration profile onto target node
- [ ] As a **sysadmin**, I can replace ssh key files of a particular node



### 3. Monitoring

- [x] As an **agent**, I can periodically post the monitoring data of a particular node
- [x] As a **sysadmin** or **user**, I can download the monitoring data of particular nodes



### 4. Virtual Private Network (VPN)

- [x] As a **user**, I can register a node to VPN
- [x] As a **sysadmin** or **user**, I can unregister a node from VPN
- [x] As an **agent**, I can connect a node to VPN
- [x] As a **user**, I can download credentials and config files to connect to VPN
- [x] As a **sysadmin** or **user**, I can ssh to the node via VPN



### 5. Workloads

- ...(TODO)
