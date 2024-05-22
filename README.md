1. Modificar ruta volumenes/bind en el docker-compose.
2. Comentar puerto 443 en docker-compose.
3. Comprobar comando CERTBOT en docker compose con "--staging"(modo prueba).
4. En /nginx-conf ocultar archivo default.conf con puertos 443 añadiendo un "."
5. "docker compose up -d".
6. Comprobar logs Certbot ningun error
7. Modificar comando CERTBOT en docker compose con "--staging"(modo prueba) por "--force-renewal".
8. "docker compose up -d".
9. Descomentar puerto 443 Docker-compose
10. Desocultar default.conf(con puertos 443) y ocultar default.conf(80)
11. "docker restart nginx"


13.    
RENOVAR CERTIFICADOS AUTOMÁTICAMENTE
Añadir la siguiente linea "sudo crontab -e" (modificar ruta si es necesario)
0 3 1 * * /home/****/syndeno-fedv1/ssl_renew.sh >> /var/log/cron.log 2>&1
