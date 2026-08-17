# hw-03: VM Networks modes 

For these ping tests, the command "ping -4 -c 4 google.com" was used because it forces the test to use the IPv4 protocol, ensuring the response is received in IPv4. 

## Hostname configuration
To change the hostname, the command "sudo hostnamectl set-hostname Francisco_hw-03" was used

New hostname: Francisco_hw-03

![Hostname](/public/images/change-hostname.png)

## First ping test using the ip provided by DHCP

ip: 192.168.0.11

![firstping](/public/images/first-ping.png)

## Important

For the following ping tests, i assign a static IP address by modifying the configuration file located at /etc/netplan/00-installer-config.yaml. 

## Second ping test using the static ip within the same subnet

### First file configuration  

![firstconfig](/public/images/first-config.png)

### Ping test

ip: 192.168.0.50

![secondping](/public/images/second-ping.png)

## Third ping test using the static ip outside the hypervisor

### Second file configuration

![secondconfig](/public/images/second-config.png)

### Ping test

ip: 10.0.99.50

![thridping](/public/images/third-image.png)

