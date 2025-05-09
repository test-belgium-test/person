## Schéma : Enterprise

**Description :**
Objet permettant d'identifier une entreprise dans une déclaration employeur. Seul un des deux numéros (`enterpriseNumber` ou `nssoNumber`) doit obligatoirement être renseigné.

### Propriétés du Schéma :

* `enterpriseNumber` (integer) - Numéro unique de l'entreprise.

  * Format : Numérique
  * Longueur : 10 chiffres
  * Structure : Les positions 1 à 8 sont un numéro d'ordre, la position 1 commence par 0 ou 1, positions 9 et 10 sont des chiffres de contrôle.
  * Valeur par défaut si inconnue : 0

* `nssoNumber` (integer) - Numéro ONSS de l'employeur.

  * Format : Numérique
  * Longueur : 9 chiffres
  * Plage autorisée : 100006 à 199999934 (définitifs)
  * Structure : `NNNNNNNCC` (N = Numéro, CC = Chiffre de contrôle)
  * Valeur par défaut si `enterpriseNumber` renseigné : 0

### Contraintes métier :

* **Condition exclusive** : Un seul des deux numéros peut être complété (`oneOf`).

### Anomalies (réponses REST standards) :

#### enterpriseNumber

| Code anomalie | Description                        | Gravité |
| ------------- | ---------------------------------- | ------- |
| 00014-001     | Non présent                        | B       |
| 00014-002     | Non numérique                      | B       |
| 00014-093     | Longueur incorrecte                | B       |
| 00014-146     | Non admis                          | B       |
| 00014-090     | Erreur de cardinalité              | B       |
| 00014-091     | Erreur de séquence                 | B       |
| 00014-004     | Nombre de contrôle invalide        | B       |
| 00014-235     | Non repris au répertoire           | B       |
| 00014-022     | Incompatibilité avec le répertoire | NP      |

#### nssoNumber

| Code anomalie | Description                                     | Gravité |
| ------------- | ----------------------------------------------- | ------- |
| 00011-001     | Non présent                                     | B       |
| 00011-002     | Non numérique                                   | B       |
| 00011-004     | Nombre de contrôle invalide                     | B       |
| 00011-041     | Numéro ONSS/PPL erroné                          | B       |
| 00011-051     | Non repris au répertoire pour trimestre déclaré | B       |
| 00011-090     | Erreur de cardinalité                           | B       |
| 00011-093     | Longueur incorrecte                             | B       |
| 00011-146     | Non admis                                       | B       |
| 00011-155     | Pas ou plus de mandat                           | B       |
| 00011-091     | Erreur de séquence                              | B       |
