# docker
4 wordpress en 2 dominios con subdominios

una carpeta (nginx-proxy) con un yaml para el contenedor para nginx don la librería jwilder y otro contenedor con el letsencrypt para aplicar certificados SSL
una carpeta (paso5) con un yaml con los containers para 4 wordpress, cada uno asociado a un contenedor distinto para la base de datos

dominios obtenidos en freenom.com:
elearn4all.tk, con el subdominio wordpress.elearn4all.tk
elearn4all.ml, con el subdominio wordpress.elearn4all.ml

con persistencia: en la carpeta /var/lib/docker/volumes del servidor
-------------------------
Pendiente:
- SSL
- phpmyadmin


