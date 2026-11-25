# Codes d'erreur de l'application

## ERR-4012 : paiement refusé par la banque

La banque du client a refusé la carte, par exemple parce qu'elle est expirée ou que le plafond est atteint.

Il n'y a rien à faire côté technique. Le support invite le client à utiliser un autre moyen de paiement.

## ERR-4021 : délai dépassé avec la passerelle de paiement

La passerelle de paiement n'a pas répondu dans les 30 secondes.

Il faut consulter la page de statut du prestataire de paiement. Si l'incident dure plus de 15 minutes, ouvrir un ticket de priorité haute et prévenir la personne d'astreinte.

## ERR-5003 : base de données injoignable

L'application n'arrive pas à joindre srv-lyon-01.

C'est un incident critique : il faut prévenir la personne d'astreinte immédiatement, sans attendre.
