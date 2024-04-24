1. Modificar ruta volumenes/bind.
2. Abrir puertos interfaz de red.
3. Modificar comando CERTBOT "--staging"(modo prueba) por "--force-renewal".
4. "docker compose -d".


1. Comprobar no errores en logs.
2. Renombrar default.conf a ..default.conf y nombrar archivo oculto .default.conf a defaul.conf (Deshabilitar puerto 80 y habilitar puerto 443) y crear/eliminar de su interior .htpasswd.
3. "docker restart nginx".



RENOVAR CERTIFICADOS AUTOMÁTICAMENTE
Crontab:
0 3 1 * * /home/****/syndeno-fedv1/ssl_renew.sh >> /var/log/cron.log 2>&1
