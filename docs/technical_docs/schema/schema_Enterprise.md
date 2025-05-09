## Schéma : Enterprise

**Description :**
Objet permettant d'identifier une entreprise dans une déclaration employeur. Seul un des deux numéros (`enterpriseNumber` ou `nssoNumber`) doit obligatoirement être renseigné.

### Propriétés du Schéma :

* `enterpriseNumber` : [Voir les détails du champ enterpriseNumber](../field/enterpriseNumber.md)

* `nssoNumber`  : [Voir les détails du champ enterpriseNumber](../field/nssoNumber.md)


### Contraintes métier :

* **Condition exclusive** : Un seul des deux numéros peut être complété (`oneOf`).

### Anomalies (réponses REST standards) :

#### enterpriseNumber

| Code anomalie | Description                        | Gravité |
| ------------- | ---------------------------------- | ------- |
| 001     | Non présent                        | B       |
| 146     | Non admis                          | B       |
| 090     | Erreur de cardinalité              | B       |
| 091     | Erreur de séquence                 | B       |

#### nssoNumber

| Code anomalie | Description                                     | Gravité |
| ------------- | ----------------------------------------------- | ------- |
| 001     | Non présent                                     | B       |
| 090     | Erreur de cardinalité                           | B       |
| 146     | Non admis                                       | B       |
| 091     | Erreur de séquence                              | B       |
