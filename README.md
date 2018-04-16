# default-nginx
Configuration basique de 3 blocs serveurs NGINX en 1 seul fichier. VHosts avec des Noms de domaine personnalisés
Cette configuration est celle d'un serveur HTTP Nginx installé sur une machine GNU/Linux que ce soit par compilation ou des dépots officiels.

La contenu du fichier "default-nginx" doit être copié dans le fichier __"/etc/nginx/sites-available/default"__.

Ensuite, il faut créé un lien symbolique vers celui-ci dans le répertoire d'activation des sites:

$ sudo ln -s /etc/nginx/sites-available/default /etc/nginx/sites-enabled/

Il faut ensuite tester la stabilité de la configutaion avec un:

$ sudo nginx -t

Et obtenir le retour suivant:

__nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful__

Ensuite redémarer le serveur pour qu'il prenne en compte les modifications apportées;

$ sudo service nginx restart

ou, pour juste re-actualiser son service principal

$ sudo service nginx reload
