# Docstring Systems : documentation interne (fictive)

Jeu de données du guide « Comment créer un RAG avec pgvector ? ».
Docstring Systems est une entreprise imaginaire, avec des bureaux à Lyon, Paris et Lille.

## Organisation

Le nom du dossier donne le service propriétaire du document :

```
docs/
├── commun/          # visible par tout le monde
├── comptabilite/    # équipe comptabilité
├── technique/       # équipe technique
└── direction/       # direction uniquement (documents confidentiels)
```

## Qui voit quoi ?

| Personne  | Service      | Bureau | Dossiers visibles                                |
|-----------|--------------|--------|--------------------------------------------------|
| Patrick   | Comptabilité | Lyon   | `commun`, `comptabilite`                         |
| Élodie    | Technique    | Lille  | `commun`, `technique`                            |
| Sébastien | Direction    | Paris  | `commun`, `comptabilite`, `technique`, `direction` |

## Les pièges prévus dans les documents

| Question à poser                                        | Ce qu'elle teste                                                                 |
|---------------------------------------------------------|----------------------------------------------------------------------------------|
| « Comment redémarrer srv-lyon-02 ? »                    | Identifiant exact : srv-lyon-01, 02 et 03 se ressemblent pour la recherche vectorielle |
| « Que faire en cas d'erreur ERR-4021 ? »                | Code d'erreur proche de ERR-4012                                                 |
| « Comment je fais pour partir en vacances ? »           | Paraphrase : le mot « vacances » n'apparaît nulle part, seulement « congés »      |
| « Je peux bosser de chez moi combien de jours ? »       | Paraphrase familière, aucun mot-clé en commun avec le document                   |
| « Comment redemarrer srv-lyon-02 ? » (sans accent)      | Recherche plein texte sans accents                                               |
| « Est-ce qu'on recrute des développeurs en 2027 ? »     | Droits : Sébastien a la réponse, Patrick et Élodie ne doivent rien obtenir        |
| « Quelle est la recette de la tartiflette ? »           | Question hors sujet : le RAG doit répondre qu'il ne sait pas                     |
# docstring-systems
