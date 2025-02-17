# Exercice les Log

__Captue d'écran des Log du Serveur Web Apache :__

![log-serveur-web-apache](https://github.com/Tr3n4rT/WCS_Quetes/blob/main/LOG/qu%C3%AAtes-log.png)

L'avant dernière ligne des log du serveur (à l'emplacement /var/log/apache2/access.log) est l'enregistrement d'une __requête HTTP__ (__GET__) __résussie__ (__code de sortie 200__). Elle a été effectué le 17/Feb/2025:12:01:17.  __L'adresse IP__ de la machine avec laquelle la requête a été effectué est __172.16.10.5__ :\

172.16.10.5 - - [17/Feb/2025:12:01:17 +0100] "GET /glpi/ajax/dashboard.php?action=get_card&dashboard=central&card_id=count_Monitor_MonitorModel&force=0&args%5Bcolor%5D=%23f5fafa&args%5Bwidgettype%5D=donut&args%5Buse_gradient%5D=1&args%5Blimit%5D=5&args%5Bcard_id%5D=count_Monitor_MonitorModel&args%5Bgridstack_id%5D=count_Monitor_MonitorModel_5a476ff9-116e-4270-858b-c003c20841a9&d_cache_key=69a57c4b79e0f5fe32dca1f62d083167cbffc2b6&c_cache_key= HTTP/1.1" 200 1378 "http://172.16.10.2/glpi/front/central.php/tutu" "Mozilla/5.0 (X11; Linux x86_64; rv:128.0) Gecko/20100101 Firefox/128.0"
::1 - - [17/Feb/2025:12:01:22 +0100] "OPTIONS * HTTP/1.0" 200 126 "-" "Apache/2.4.62 (Debian) (internal dummy connection)"


La dernière ligne des log du serveur montre l'echec d'une __requête HTTP__ (__GET__) à une __page non trouvé__ nomé "tutu" avec le code de sortie __404__. Elle a été effectuée le [17/Feb/2025:12:01:24.
172.16.10.5 - - [17/Feb/2025:12:01:24 +0100] "GET /tutu HTTP/1.1" 404 490 "-" "Mozilla/5.0 (X11; Linux x86_64; rv:128.0) Gecko/20100101 Firefox/128.0"
