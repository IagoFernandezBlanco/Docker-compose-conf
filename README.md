# Docker-compose-conf

## Práctica que muestra todos los cambios realizados para que nuestro servidor DNS pueda traducir una zona creada por nosotros.
### Es necesario que los archivos de configuración sean modificados dentro de nuestro volumen, salvo el archivo resolv.conf que ese se modifica dentro de nuestro cliente.


## Maquina Ubuntu
### apt update --> actualizar todos los paquetes
### apt-get install -y iputils-ping --> para que ping funcione
### apt-get install iputils-tracepath --> este paquete instala tracepath 
### apt install net-tools --> necesario para poder usar ifconfig y route
### apt-get install -y ifupdown 
### apt-get install dnsutils -y --> isntala dig y dns commands
### apt-get install -y whois --> instalar el comando whois
### apt install -y curl --> permite descargar archivos 

## Archivos configurados :
### namd.conf.local --> aqui se crean las zonas
### named.conf.options --> aqui se modifican los forwarders
### db.example.com --> aqui se escriben los parametros de la zona.

## Parametros de la zona :
### NS --> name-server
### CNAME --> nombre de la zona
### SOA --> el servidor autoritario
### A --> la ip del servidor
### AAAA --> la ipv6 del servidor
