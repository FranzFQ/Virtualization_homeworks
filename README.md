# hw-04: IPsec
## Topology
### Network addressing
#### Network A

* **Subnet:** 192.168.1.0/24
* **Router_1:** 
    * **Interface 0/0/0:** 10.0.0.1/30
    * **Interface 0/0/1:** 192.168.1.1/24
* **PC0:**
    * **Static IP:** 192.168.1.2/24

#### Network B

* **Subnet:** 192.168.2.0/24
* **Router_2:**
    * **Interface 0/0/0:** 20.0.0.2/30
    * **Interface 0/0/1:** 192.168.2.1/24
* **PC1:**
    * **DHCP IP:** 192.168.2.11/24
* **Server:**
    * **Static IP:** 192.168.2.10/24

#### Internet simulation network

* **Router_IPS:**
    * **Interface 0/0/0:** 10.0.0.2/30
    * **Interface 0/0/1:** 20.0.0.1/30

![Topology](/public/images/topology.png)

## Pre-test Baseline
Initial baseline state of both **Router_1** and **Router_2** prior to sending test traffic through the IPsec tunnel

### Router_1
![Router_1](/public/images/before_router_1.png)

### Router_2
![Router_2](/public/images/before_router_2.png)

## Traffic verification with ping test

### PC0 ping test
In this ping test sent to the server in network B through IPsec tunnel

![PC0](/public/images/ping.png)

### successfully established IPsec tunnel
Both routers now display an **ACTIVE** state and displays active encapsulation/decryption packet counters and the applied transform set (`esp-aes esp-sha-hmac`), confirming that traffic is successfully matching the crypto map and utilizing the tunnel

#### Router_1
![router_1](/public/images/after_ping_router_1.png)

#### Router_2
![router_2](/public/images/after_ping_router_2.png)

### Web access verification over the IPsec tunnel

#### PC0 HTTP test
The browser successfully loads the default Cisco Packet Trader web page hosted on the remote server, demonstrating application-layer communication across the secure tunnel.

![PC0](/public/images/web.png)

### Successfully HTTP connection
Both routers show an incremented number of encapsulated and decrypted packet counters driven by the HTTP request and response

#### Router_1
![Router_1](/public/images/after_web_router_1.png)

#### Router_2
![Router_2](/public/images/before_router_2.png)