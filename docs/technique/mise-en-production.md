# Mise en production et astreinte

## Quand peut-on déployer ?

Les mises en production ont lieu du lundi au jeudi, entre 9 h et 16 h. Aucune mise en production n'est faite le vendredi, ni la veille d'un jour férié.

## Comment déployer ?

Toute modification passe par une merge request relue par une autre personne de l'équipe technique. Une fois la branche fusionnée dans `main`, le déploiement sur srv-lyon-02 est automatique.

Après chaque déploiement, il faut vérifier que la page `/sante` de l'application répond bien.

## L'astreinte

Chaque semaine, une personne de l'équipe technique est d'astreinte, du lundi 9 h au lundi suivant 9 h. Elle est la seule à pouvoir autoriser une intervention sur srv-lyon-01.

Le planning d'astreinte se trouve dans Kiosque, rubrique « Technique ». Un échange d'astreinte entre deux personnes doit y être noté au moins 48 heures à l'avance.
