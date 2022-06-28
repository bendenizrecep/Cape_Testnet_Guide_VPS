# Cape Testnet Guide VPS
Espresso Systems -  Cape Testnet Guide

### System Requirement


- 2vCPU
- 2GB RAM
- Ubuntu 20.04

_You can perform node installations over a vps that will meet the above-mentioned system requirements._

### Cape Official Testnet Page;
https://docs.cape.tech/espresso-systems/cape-user-guide/getting-started



- We need to install docker as mentioned in the official guide. We will install on a Linux VPS, we must enter the code below into the terminal.
We will install on a Linux VPS, we must enter the code below into the terminal.
``` 
sudo snap install docker
```
- After installing Docker, you must enter the following codes one by one.
 ``` 
 curl https://www.espressosys.com/cape/docker-compose.yaml --output docker-compose.yaml
 
 docker-compose pull
 
 apt-get install screen
 
 screen -S cape
 
 docker-compose up

``` 
- Start CMD as administrator and enter the following codes. Enter your VPS IP address in the vpsIP field.
``` 
netsh interface portproxy add v4tov4 listenaddress=127.0.0.1 listenport=80 connectaddress=vpsIP connectport=80
netsh interface portproxy add v4tov4 listenaddress=127.0.0.1 listenport=60000 connectaddress=vpsIP connectport=60000
```

- After completing the steps, log in from your local computer by typing "localhost" in the browser.
![image](https://user-images.githubusercontent.com/61727501/174287799-73af3adf-56d9-4d45-afbe-a16fa0ef2a08.png)

- After connecting to Cape, you can create a new wallet and test Cape by following the steps in the link below.

https://docs.cape.tech/cape-user-guide/creating-a-new-wallet

### You can use the following codes to turn off port forwarding from your local computer.
```
netsh interface portproxy dump

netsh interface portproxy reset

netsh interface portproxy delete
```

### Espresso Systems Official Discord Link
https://discord.gg/5gBEVACJ2E
