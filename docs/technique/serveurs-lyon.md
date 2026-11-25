# Serveurs de Lyon

Les trois serveurs de production sont hébergés dans le bureau de Lyon.

## srv-lyon-01 : la base de données

srv-lyon-01 héberge la base PostgreSQL de production.

Ne jamais le redémarrer sans prévenir dans le canal #prod : toutes les applications perdent leur connexion à la base pendant le redémarrage. Le redémarrage se fait avec `sudo systemctl restart postgresql`, et uniquement après l'accord de la personne d'astreinte.

## srv-lyon-02 : l'application web

srv-lyon-02 héberge l'application web, servie par Gunicorn derrière Nginx.

En cas de lenteur de l'application, on peut redémarrer Gunicorn avec `sudo systemctl restart gunicorn`. Inutile de prévenir : la coupure ne dure que quelques secondes.

## srv-lyon-03 : les tâches de fond

srv-lyon-03 fait tourner Celery et Redis. C'est lui qui envoie les e-mails et génère les factures PDF.

Si les e-mails ne partent plus, il faut d'abord vérifier l'état du service avec `sudo systemctl status celery`, puis consulter les journaux avec `journalctl -u celery`.
