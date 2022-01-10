# What is Docker?

## About
- **In short:** Docker is basically a container engine which uses the Linux Kernel features like namespaces and control groups to create containers on top of an operating system and automates application deployment on the container. Docker uses Copy-on-write union file system for its backend storage

---
- **In depth:** Docker is a tool designed to make it easier to create, deploy, and run applications by using containers. Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and deploy it as one package. By doing so, thanks to the container, the developer can rest assured that the application will run on any other Linux machine regardless of any customized settings that machine might have that could differ from the machine used for writing and testing the code.

---
- **To make it simple:** In a way, Docker is a bit like a virtual machine. But unlike a virtual machine, rather than creating a whole virtual operating system, Docker allows applications to use the same Linux kernel as the system that they're running on and only requires applications be shipped with things not already running on the host computer. This gives a significant performance boost and reduces the size of the application.

---
!!! info
    **License:** Docker is open source. This means that anyone can contribute to Docker and extend it to meet their own needs if they need additional features that aren't available out of the box.

## Docker and metrix

- **Stability:** Docker engine is usually driven on the top of server or NAS device. Most used metrix docker server is unRAID. 
Server is by nature more reliable and stable than usual personal computer.

- **24/7 usage:** As server is already 24/7 in use, you don't need to let your personal computer to do the same only to run Metrix masternode or to stake coins. 
Your electric usage is not affected by running Metrix masternode/stake this way.

- **Updates:** You don't need to think about Metrix wallet updates, as this is done in background.
Only thing you need to do is to update Metrix docker (usually by one click). 
And if you use unRAID server, even Metrix docker update is done automaticaly.


## Installation

## Synology NAS
**Getting ready for docker world:** Synology NAS is one of devices that support docker hosting.

Synology has limited Docker availability in the package manager to only some select models:

- 18 series:DS3018xs, DS918+, DS718+, DS218+
- 17 series:FS3017, FS2017, RS18017xs+, RS4017xs+, RS3617xs+, RS3617xs, RS3617RPxs, DS3617xs, DS1817+, DS1517+
- 16 series:RS18016xs+, RS2416+, RS2416RP+, DS916+, DS716+II, DS716+, DS216+II, DS216+
- 15 series:RS815+, RS815RP+, RC18015xs+, DS3615xs, DS2415+, DS1815+, DS1515+, DS415+
- 14 series:RS3614xs+, RS3614xs, RS3614RPxs, RS2414+, RS2414RP+, RS814+, RS814RP+
- 13 series:RS10613xs+, RS3413xs+, DS2413+, DS1813+, DS1513+, DS713+
- 12 series:RS3412xs, RS3412RPxs, RS2212+, RS2212RP+, RS812+, RS812RP+, DS3612xs, DS1812+, DS1512+, DS712+, DS412+
- 11 series:RS3411xs, RS3411RPxs, RS2211+, RS2211RP+, DS3611xs, DS2411+, DS1511+, DS411+II, DS411+
- *10 series:RS810+, RS810RP+, DS1010+, DS710+

Beside NAS, you can install docker images on **unRAID** server **(preferred)**

## **Install steps unRAID**
- Docker hub URL:  [Docker Hub URL](https://hub.docker.com/r/medolino2009/docker-metrix-multiwallet/)
- Icon URL: [Icon URL](https://avatars3.githubusercontent.com/u/41876146?s=200&v=4)
- WebUI: http://[IP]:[PORT:6080]/vnc.html?resize=remote&host=[IP]&port=[PORT:6080]&autoconnect=1

## **Make Volumes** 
In docker host you need to make following volumes (for block chain and configuration):

Metrix --> /home/ubuntu/.metrix 
ColX --> /home/ubuntu/.ColossusXT 
Send --> /home/ubuntu/.send 
Shard --> /home/ubuntu/.shard 
Bitcoin --> /home/ubuntu/.bitcoin 
Usdex --> /home/ubuntu/usde2 
Vulcano--> /home/ubuntu/.vulcanocore 
Epic--> /home/ubuntu/.epic 
NulleX--> /home/ubuntu/.nullexqt 
Maxcoin--> /home/ubuntu/.maxcoin 
Rapids--> /home/ubuntu/.rapids
MWalletconfig --> /home/ubuntu/.config

