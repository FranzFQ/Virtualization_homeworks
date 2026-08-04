# HW-02: Virtual hots to virtual host connection

## Evidencia de la actividad
## Cambiar el nombre de cada host virtual
Para ello se utilizo el comando: sudo hostnamectl set-hostname <br> 
Los nombres que recibio cada maquina virtual fueron: <br>
host virtual 1: server01 <br>
host virtual 2: server02 <br>

![Evidence01](/public/images/server_names.png)

## Modificar el adaptador para mi red domestica
Para ello se modifico la el archivo "00-installer-config.yaml" que se encuentra ubicado en: /etc/netplan/ <br> 
con la finalidad de asignarle una IP estatica a cada servidor en donde las IPs asignadas fueron: <br>
host virtual 1 IP: 192.168.1.50 <br>
host virtual 2 IP: 192.168.1.51 <br>

![Evidence02](/public/images/servers_config.png)

## Pruebas de comunicacion entre servidores
Por ultimo se realizo un ping en ambos hosts para que apunten al otro usando la ip que se configuro anterior mente

![Evidence03](/public/images/comunication_test.png)
