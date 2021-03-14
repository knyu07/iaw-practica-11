# Práctica 11: Auditoría de seguridad en Wordpress

La herramienta WPScan CLI es un escáner de seguridad de WordPress de caja negra gratuito, para uso no comercial, escrito para profesionales de la seguridad y mantenedores de blogs para probar la seguridad de sus sitios.

## Instalación:

Instalamos Ruby
```
apt install ruby -y
```

Instalamos las dependencias
```
apt install build-essential libcurl4-openssl-dev libxml2 libxml2-dev libxslt1-dev ruby-dev  libgmp-dev zlib1g-dev -y
```

Instalamos el WPscan
```
gem install wpscan 
```

## COMANDOS DOCKER: 

Para obtener la lista de plugins instalados en nuestro sitio WordPress podemos ejecutar:
```
docker run -it --rm wpscanteam/wpscan --url http://192.168.22.20  --enumerate p
```
Para realizar un escaneo completo de un sitio WordPress podemos ejecutar:
```
docker run -it --rm wpscanteam/wpscan --url http://DIRECCIÓN_IP
```
Para poder hacer uso del servicio de la API de WPScan,es necesario registrarse en su web y obtener un TOKEN.

![](imagenes/token)

```
docker run -it --rm wpscanteam/wpscan --url http://DIRECCIÓN_IP --api-token 8pIlWnF2dxbgfvyQfDAUaV3T3iafo0uO1K8OPr2KKRM
```
![](imagenes/token2)

Una vez instalado el WPScan con el comando ***wpscan --help* comprobamos.

![](imagenes/wpscan)

Para obtener la lista de plugins instalados de nuestro sitio ejecutamos:
```
wpscan --url DIRECCIÓN --enumerate p
```
