# Séance 2.2 : Management du contenu du projet et WBS

> **À retenir :** faire **tout** le travail requis et **seulement** le travail requis. La WBS découpe le projet en livrables, jusqu'au **lot de travail**.

## 1. L'ennemi n° 1 : le scope creep

Le **scope creep** signifie que le périmètre n'est **pas maîtrisé**. Il ne cesse d'augmenter ou de changer, car les parties prenantes continuent de demander de nouvelles fonctionnalités et de nouveaux besoins.

## 2. Management du périmètre

C'est :
- s'assurer que **tout le travail requis, et seulement le travail requis**, est effectué pour mener le projet à son terme avec succès ;
- se concentrer sur la définition et la maîtrise de **ce qui fait partie du projet et de ce qui n'en fait pas partie**.

## 3. Définir le périmètre

| Contenu du **produit** | Contenu du **projet** |
|---|---|
| Caractéristiques et fonctions | Travail à réaliser pour produire ce produit, **y compris** réunions, rapports, analyses (management) |

**L'énoncé détaillé du périmètre comprend :**
- **Inclusions :** description détaillée du projet et du produit, **livrables** (résultats tangibles), **critères d'acceptation**.
- **Exclusions :** ce qui ne doit pas faire partie du projet.

> Le périmètre définit la **taille** du projet.

### Charte de projet ou énoncé du périmètre ?

La différence principale est le **niveau de détail** :

| Charte de projet | Énoncé du contenu et du périmètre |
|---|---|
| Informations générales, niveau **très macro** | Description **détaillée** |

Le modèle de charte montré en cours contient : titre, sponsor, date, chef de projet, client, justification, description, exigences de haut niveau, risques de haut niveau, objectifs avec critères de succès et personne qui approuve (périmètre, temps, coût, autre), et jalons avec dates.

### Les 13 points à documenter
1. Exigences du projet et des livrables
2. Exigences et caractéristiques du produit
3. Méthodes et critères d'acceptation du produit
4. Limites du projet
5. Contraintes du projet
6. Hypothèses du projet
7. Organisation initiale du projet
8. Risques définis initiaux
9. Jalons de l'échéancier
10. WBS initiale
11. Estimation des coûts
12. Grandes lignes de la maîtrise du contenu
13. Exigences d'approbation

## 4. La WBS (Work Breakdown Structure)

> Décomposition **hiérarchique orientée vers les livrables**, qui organise et définit **tout** le contenu du projet.

**Autres noms :** structure de découpage du projet, organigramme technique du projet, organigramme des tâches du projet (**OTP**).

```
Projet
├── Phase 1
│   ├── Livrable 1.1
│   └── Livrable 1.2
│       ├── Lot de travail 1.2.1
│       └── Lot de travail 1.2.2
├── Site 2
│   ├── Livrable 2.1
│   └── Livrable 2.2
└── Sous-projet 3
    ├── Livrable 3.1
    │   ├── Lot de travail 3.1.1
    │   └── Lot de travail 3.1.2
    └── Livrable 3.2
```

### Règles de construction
- Elle est créée **par l'équipe**.
- Finaliser le **1er niveau** avant de le détailler.
- Tout le projet est inclus au niveau le plus haut (le titre du projet).
- Elle inclut **uniquement le travail nécessaire** pour créer les livrables.

### Quand s'arrêter ? Au lot de travail, qui :
- logiquement, ne peut plus être subdivisé ;
- peut se réaliser rapidement (**petit projet : 40 h, grand projet : 300 h**) ;
- peut se réaliser sans interruption ;
- a une conclusion logique et un livrable ;
- peut être sous-traité.

### À quoi sert-elle ?
La WBS permet une meilleure planification pour : l'identification des activités, l'estimation des ressources, l'estimation des coûts, la budgétisation, les ressources humaines, la qualité, les communications, le management des risques et les approvisionnements.

Elle sert aussi de référence pour la **validation du contenu** : obtenir l'**acceptation formelle** du contenu achevé et des livrables correspondants.

## 5. Vérification du contenu ou contrôle qualité ?

| Vérification du contenu | Contrôle qualité |
|---|---|
| Concerne l'**acceptation** des livrables | Vise à satisfaire les **exigences qualité** spécifiées |

- Le contrôle qualité est généralement effectué **avant** la vérification du contenu.
- La validation de la qualité est une condition **sine qua non** pour valider le contenu. Le contraire n'est pas toujours vrai.
- Les deux processus peuvent être exécutés **en parallèle**.

## 6. Exemple complet : le vélo

- **PBS (Product Breakdown Structure) :** découpe le **produit** (cadre, pédalier, roues, freins, vitesses, intégration).
- **WBS :** découpe le **travail** en tâches, avec une estimation de durée.

```
Vélo (total des durées : 100 j)
├── Montage du CADRE (15 j)
│   ├── Soudure du cadre (7 j) : 4 tubes à 1 j, haubans 1 j, bases 2 j
│   ├── Montage de la fourche (3 j)
│   ├── Montage du guidon (2 j)
│   └── Montage de la selle (3 j)
├── Montage du PÉDALIER (5 j)
│   └── Préparation pédalier (3 j), pédales gauche et droite (2 j)
├── Montage des ROUES (30 j)
│   ├── Roue avant (13 j) : jante 3 j, rayons 7 j, moyeu 2 j, pneu 1 j
│   └── Roue arrière (17 j) : jante 3 j, rayons 7 j, moyeu 6 j, pneu 1 j
├── Montage des FREINS (5 j)
│   └── Leviers (1 j), frein avant (2 j), frein arrière (2 j)
├── Montage des VITESSES (5 j)
│   └── Système de changement (4 j), manette (1 j)
└── Tâches d'INTÉGRATION (40 j)
    └── Design et conception (8 j), notice (15 j), essais banc et route (17 j)
```

> Le total de 100 j additionne le temps de travail (estimation ascendante). Ce n'est pas la durée du projet : certaines tâches peuvent se faire en parallèle.
> L'intégration et le management font partie de la WBS, car **tout** le travail y figure.
