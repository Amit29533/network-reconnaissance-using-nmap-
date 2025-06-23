# network-reconnaissance-using-nmap
This repository provides a detailed walkthrough of network reconnaissance using Nmap. It covers identifying open ports, analyzing services running on those ports, discovering known vulnerabilities, and includes a comprehensive cheat sheet for efficient scanning and enumeration.

## How to Install and Run?

 ⛩️ Before building Nmap, install required dependencies:
 ```bash 
sudo apt update
sudo apt install -y build-essential checkinstall libssl-dev \
libpcap-dev libpcre3-dev lua5.3 liblua5.3-dev \
zlib1g-dev git
```

1️⃣ Step 1: Clone the Nmap Source Code
```bash
git clone https://github.com/nmap/nmap.git
cd nmap
```
2️⃣ Step 2: Build Nmap
```bash
./configure
make
```
3️⃣ Step 3: Install Nmap
```bash
sudo make install
```
4️⃣ Step 4 : Verify Installation
```bash
nmap --version
```

To utilise nmap, you will need your ip address. Here are quick ways to find your Ip address.

## Finding your public IP address:
✨  Simply visit : https://whatismyipaddress.com/

## Finding your local IP address:


🪟 In a Windows machine
```bash
ipconfig
```
![image](https://github.com/user-attachments/assets/2e95d077-9459-4dfc-8453-190b7d67b0d6)


🐧  In a Linux machine
```bash
ifconfig
```
![image](https://github.com/user-attachments/assets/0e909292-13fb-4e12-9174-c93e193b6596)



## Demonstrating some basic commands :

 📝 NOTE : Normally commands first ping the system then if it finds the system is up then start the port scan.
 
 1️⃣ Identify open TCP ports on a target machine
 
 ```bash
nmap -sS ip_address
```
Replace ip_address with the ip you are trying to scan.
![image](https://github.com/user-attachments/assets/6c723b02-0e7c-4d2e-98eb-6721123175ff)

 2️⃣ Identify open UDP ports on a target machine
 ```bash
nmap -sU <ip_address>
```
3️⃣ Avoid pinging the system and directly start to scan for open ports.
``` bash
nmap -sS -Pn <ip_address>
```
4️⃣ Split the ping and Scan data packets into 8byte fragments to evade firewalls, IDS and packet filters.
```bash
nmap -f <ip_address>
```
5️⃣ Fool the address by sending decoy data packets.
```bash
nmap -sS -D [decoy1,decoy2,decoy3..-ip_adddress] <target_ip__address>
```
There are so many more commands, you can finds those in the cheat_sheet..
