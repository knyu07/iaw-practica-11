# Práctica 11: Auditría de seguridad en Wordpress

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

Una vez instalado el WPScan con el comando ***wpscan --help* comprobamos.

![](imagenes/wpscan)

Para obtener la lista de plugins instalados de nuestro sitio ejecutamos:
```
wpscan --url DIRECCIÓN --enumerate p
```