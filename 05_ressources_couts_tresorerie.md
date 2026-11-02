# Séance 4 : Ressources, budget et trésorerie

> **À retenir :** Coût d'une activité = (somme des taux des ressources) × durée. **BAC** = somme de tous ces coûts. Le **besoin de financement** = le creux le plus bas de la trésorerie cumulée.

## 1. Estimer les ressources

Évaluer les **types et quantités** nécessaires à chaque activité. Ce processus est répété périodiquement pendant le projet. Les besoins se regroupent par lot, par branche de WBS et pour tout le projet.

**Exemple, pose des pompes d'une station de pompage :**

| Catégorie | Exemple |
|---|---|
| Humaines | 1 chef d'équipe, 2 moniteurs, 4 aides |
| Moyens à utiliser | 1 chariot élévateur, 2 palans, 1 caisse à outils |
| Équipements à monter | 4 pompes, 16 boulons de fixation |

Ces quantités, multipliées par les **coûts unitaires** et les **délais**, donnent le coût.

**Organigramme des ressources :** représentation hiérarchique par catégorie et par type.

```
Projet (niveau 0)
├── Personnel (niveau 1) : PM, chef d'équipe, responsable qualité, contrôleur de gestion (niveau 2)
├── Matériel : matière 1, matière 2
└── Équipement : équipement 1, équipement 2
```

## 2. Estimer les coûts

Le management des coûts porte sur les ressources nécessaires, mais tient aussi compte de l'effet des décisions sur le coût d'**utilisation, de maintenance et de support** du produit :

| Décision | Effet pour l'entreprise | Effet pour le client |
|---|---|---|
| Limiter le nombre de revues de conception | Réduit le coût du projet | Augmente le coût d'exploitation |
| Acheter un équipement plus sophistiqué | Augmente le coût du projet | Réduit le coût d'exploitation |

**Autres points :**
- l'estimation est répétée périodiquement ;
- si plusieurs devises sont utilisées, il faut fixer les taux de change ;
- estimer les coûts permet de savoir si le projet sera rentable ;
- l'exactitude **augmente** avec l'avancement : environ **±25 %** à l'initialisation, puis environ **±5 %**.

**Techniques :** jugement d'expert, analogie, ascendante, paramétrique, trois points.

**Trois points pour les coûts :**
- `CO` optimiste : meilleur scénario.
- `CPP` plus probable : évaluation réaliste.
- `CP` pessimiste : pire scénario.

| Distribution | Formule du coût escompté (CE) |
|---|---|
| **Triangulaire** | `CE = (CO + CPP + CP) / 3` |
| **Bêta** | `CE = (CO + 4 CPP + CP) / 6` |

**Entrées utilisées par le chef de projet :** WBS, besoin en ressources, tarifs des ressources, durée prévue. S'y ajoutent les données historiques et les informations sur les risques.

### De quoi est composé le coût ?

```
Coût = Coûts unitaires × Délais + Coûts des risques (identifiés) + Aléas (risques non identifiés)
```

- **Coût des risques identifiés :** c'est le coût de la **réponse** au risque.
- **Aléas :** un pourcentage qui dépend de la maîtrise du projet (expérience, pays, etc.).

> **Piège :** pour un risque de pluie d'une journée de retard, si la réponse consiste à acheter des bâches, le coût du risque est le **prix des bâches**, et non le coût d'une journée de ressources.

## 3. Déterminer le budget

Consolider les coûts estimés pour établir une **référence de base des coûts approuvée**, qui sert à suivre la performance.

**Le budget sert à :** faire la synthèse des ressources, évaluer la faisabilité, demander des financements.

**Structure :**

```
Budget du projet
├── Réserve pour imprévus (hors référence de base)
└── Référence de base des coûts
    ├── Réserve pour aléas
    └── Estimations des coûts des lots de travaux
        ├── Estimation du coût des activités
        └── Réserve pour aléas des activités
```

**Délégation par niveau :** chaque responsable doit respecter le budget de **son** niveau, mais les coûts du niveau inférieur peuvent varier. Le chef de projet respecte le budget du projet, alors que les budgets 1.1 à 1.3 peuvent varier.

### Exemple du cours : calcul du BAC

Taux par mois : R1 = 9 500, R2 = 4 000, R3 = 3 500, R4 = 6 500, R5 = 6 000, R6 = 7 500.

| Activité | Prédécesseur | Durée (mois) | Ressources | Coût ressources × durée | BAC (DT) |
|---|---|---|---|---|---|
| A | - | 1 | R1, R2 | (9 500 + 4 000) × 1 | 13 500 |
| B | A | 3 | R3 | 3 500 × 3 | 10 500 |
| C | B | 4 | R3, R4 | (3 500 + 6 500) × 4 | 40 000 |
| D | A | 2 | R5 | 6 000 × 2 | 12 000 |
| E | C, D | 2 | R5, R6 | (6 000 + 7 500) × 2 | 27 000 |
| | | | | **BAC du projet** | **103 000** |

Durée : 10 mois. Chemin critique : A → B → C → E.

## 4. Planifier la trésorerie et le financement

> La diapo renvoie à un **fichier Excel** qui ne figure pas dans les documents fournis. La méthode ci-dessous est une méthode standard, reconstruite à partir de l'énoncé du cas. Vérifiez-la si vous avez accès à ce fichier.

**Méthode :**
1. Répartir les coûts de chaque activité sur le temps, à partir de l'échéancier (dates au plus tôt).
2. Totaliser les **dépenses** par période.
3. Calculer les **recettes** : `coût du lot × (1 + marge)`, encaissées avec le décalage indiqué.
4. Pour chaque période : `Flux net = Recettes − Dépenses`.
5. `Cumul = Cumul précédent + Flux net`.
6. **Besoin de financement** = |cumul le plus négatif|.
7. **Financement externe** = besoin total − financement propre.
8. **Plan :** utiliser d'abord les fonds propres, puis le financement externe, et rembourser avec les excédents.

**Exemple corrigé :** partie 2 de [07_cas_projet_corrige.md](07_cas_projet_corrige.md).
