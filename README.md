# Docker
En un servidor linux, se ponen operativos 4 wordpress cada uno con su base de datos, cada uno de ellos (wordpress y base de datos) en contenedores docker aislados.
Otros contenedores: 
- jwilder/nginx-proxy (proxy reverso con NGINX)
- letsencrypt
- phpmyadmin para dos wordpress

, todos dentro de la misma red:

Se utilizan 2 dominios obtenidos en freenom.com:
- elearn4all.tk, con el subdominio wordpress.elearn4all.tk
- elearn4all.ml, con el subdominio wordpress.elearn4all.ml

- una carpeta (nginx-proxy) con un yaml para el contenedor para nginx con la librería jwilder y otro contenedor con el letsencrypt para aplicar certificados SSL
- una carpeta (paso5) con un yaml con los containers para 4 wordpress, cada uno asociado a un contenedor distinto para la base de datos y dos contenedores phpmyadmin vinculados a las bases de datos de los wordpress de los dominios elearn4all.tk y elearn4all.ml


Persistencia: en la carpeta /var/lib/docker/volumes del servidor

Importante: los dominios y subdominios deben estar definidos en el archivo /etc/hosts del servidor. Ejemplo:

127.0.0.1       elearn4all.tk

127.0.0.1       www.elearn4all.tk

127.0.0.1       wordpress.elearn4all.tk

127.0.0.1       www.wordpress.elearn4all.tk

127.0.0.1       elearn4all.ml

127.0.0.1       www.elearn4all.ml

127.0.0.1       wordpress.elearn4all.ml

127.0.0.1       www.wordpress.elearn4all.ml

127.0.0.1       phpmyadmin.elearn4all.tk

127.0.0.1       phpmyadmin.elearn4all.ml

-------------------------
