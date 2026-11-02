# Séance 3 : Dimension temporelle et échéancier

> **À retenir :** aller → calcule ES et EF (on prend le **Max**). Retour ← calcule LF et LS (on prend le **Min**). Une tâche avec **TF = 0** est **critique**.

## 1. Les étapes

1. **Identifier les activités**, à partir du niveau le plus bas de la WBS.
2. **Les séquencer** selon leurs dépendances (prédécesseur → successeur). Ce processus se poursuit tout au long du projet.
3. **Estimer les durées.**
4. **Calculer les dates clés et les marges**, puis tracer le réseau et le Gantt.

## 2. Les notions, avec l'exemple du DS

Mardi à 12h, on annonce un DS pour mercredi à 12h. Il faut 2 h de révision.

```
Mardi 12h ─ 14h ........................ Mercredi 10h ─ 12h
   ES        EF                              LS          LF
```

| Sigle | Sens | Exemple |
|---|---|---|
| **ES** (Early Start) | Début au plus tôt | Mardi 12h (étudiant motivé) |
| **EF** (Early Finish) | Fin au plus tôt | Mardi 14h |
| **LS** (Late Start) | Début au plus tard | Mercredi 10h (étudiant non motivé) |
| **LF** (Late Finish) | Fin au plus tard | Mercredi 12h |

Présentation d'une tâche (celle du modèle du cours) :

```
┌────┬────┬────┐
│ ES │ TF │ EF │    D  = durée
├────┼────┴────┤    TF = marge totale (Total Float)
│ D  │ Activité│    FF = marge libre (Free Float)
├────┼────┬────┤
│ LS │ FF │ LF │    Le modèle ajoute aussi des tâches « Début » et « Fin » de durée 0.
└────┴────┴────┘
```

## 3. Les formules

| Attribut | Formule | En clair |
|---|---|---|
| **ES** | `ES(X) = Max{EF(prédécesseurs)}` | La tâche attend que **tous** ses prédécesseurs soient finis |
| **EF** | `EF(X) = ES(X) + D` | |
| **LF** | `LF(X) = Min{LS(successeurs)}` | Elle ne doit retarder **aucun** successeur |
| **LS** | `LS(X) = LF(X) − D` | |
| **FF** | `FF(X) = ES(1er successeur) − EF(X)` | « 1er successeur » = celui qui a le plus petit ES |
| **TF** | `TF(X) = LS(X) − ES(X) = LF(X) − EF(X)` | |

### Les deux marges

| | Marge libre (FF) | Marge totale (TF) |
|---|---|---|
| **Définition** | Retard maximal **sans retarder le début au plus tôt des successeurs** | Retard maximal **sans retarder la fin du projet** |
| **Effet** | **Local** | **Global** |

- Si `TF = 0`, alors `FF = 0`. **L'inverse n'est pas toujours vrai.**
- Tâche à `TF = 0` = **tâche critique**.
- L'ensemble des tâches critiques forme le ou les **chemins critiques**, c'est-à-dire le chemin le plus long.
- Pour une tâche finale, on calcule `FF = Fin du projet − EF`.

## 4. Méthode d'examen

1. **Niveaux :** niveau 1 = pas de prédécesseur. Niveau d'une tâche = 1 + le plus grand niveau de ses prédécesseurs. (En cours : on barre les tâches déjà placées dans le tableau des antériorités, et celles qui n'ont plus d'antériorité forment le niveau suivant.)
2. **Réseau :** placer les tâches par niveau, de gauche à droite.
3. **Aller :** ES et EF de gauche à droite. Le premier ES vaut 0.
4. **Durée du projet :** plus grand EF.
5. **Retour :** LF et LS de droite à gauche. Les tâches finales ont LF = durée du projet.
6. **Marges**, puis **chemin critique** (TF = 0).
7. **Gantt :** barres de ES à EF, marge de EF à LF.

**Contrôle rapide :** la somme des durées du chemin critique doit être égale à la durée du projet.

## 5. Exemple : la clôture et la porte

| Tâche | D (j) | Prédécesseur | ES | EF | LS | LF | TF | FF |
|---|---|---|---|---|---|---|---|---|
| 1 Définir les dimensions | 1 | - | 0 | 1 | 0 | 1 | **0** | 0 |
| 2 Finir les murs | 2 | 1 | 1 | 3 | 4 | 6 | 3 | 3 |
| 3 Acheter la porte | 5 | 1 | 1 | 6 | 1 | 6 | **0** | 0 |
| 4 Monter la porte | 1 | 2, 3 | 6 | 7 | 6 | 7 | **0** | 0 |

**Durée : 7 jours. Chemin critique : 1 → 3 → 4.**

## 6. Estimer les durées

| Technique | Principe |
|---|---|
| **Jugement d'expert** | Expérience antérieure d'un membre de l'équipe |
| **Analogie** | Données historiques d'un projet précédent |
| **Ascendante (bottom-up)** | Estimer les activités du bas de la WBS, puis additionner. Utilisée quand on **exige les caractéristiques** |
| **Descendante (top-down)** | Estimer le global, puis détailler vers le bas de la WBS. Utilisée quand on **exige le budget** |
| **Paramétrique** | Calculs ou mesures, pour les tâches simples et répétitives |
| **Trois points** | Plage entre optimiste, plus probable et pessimiste |

**Paramétrique, exemple :** 1 h par trou et par personne, 10 trous = 10 h. Avec 2 personnes : 5 h. Avec une machine deux fois plus rapide que ces 2 personnes : 2,5 h.

**Trois points :**

$$DE = \frac{d_O + 4\,d_{PP} + d_P}{6}$$

- `dO` optimiste : conditions idéales, temps minimum.
- `dPP` plus probable : conditions normales.
- `dP` pessimiste : pires conditions, temps maximum.

*Exemple (non tiré du cours) :* dO = 4, dPP = 6, dP = 14, donc DE = (4 + 24 + 14) / 6 = **7 jours**.

## 7. Exercice 1 du cours, corrigé

| Tâche | Prédécesseurs | D (mois) | Niveau | ES | EF | LS | LF | TF | FF |
|---|---|---|---|---|---|---|---|---|---|
| **A** | - | 1 | 1 | 0 | 1 | 0 | 1 | **0** | 0 |
| B | A | 1 | 2 | 1 | 2 | 3 | 4 | 2 | 0 |
| **C** | A | 2 | 2 | 1 | 3 | 1 | 3 | **0** | 0 |
| D | B, C | 1 | 3 | 3 | 4 | 4 | 5 | 1 | 0 |
| J | B | 1 | 3 | 2 | 3 | 4 | 5 | 2 | 1 |
| **F** | C | 2 | 3 | 3 | 5 | 3 | 5 | **0** | 0 |
| E | D, J | 2 | 4 | 4 | 6 | 5 | 7 | 1 | 0 |
| **G** | F | 2 | 4 | 5 | 7 | 5 | 7 | **0** | 0 |
| **H** | E, G | 1 | 5 | 7 | 8 | 7 | 8 | **0** | 0 |
| I | E | 1 | 5 | 6 | 7 | 7 | 8 | 1 | 1 |

**Durée : 8 mois. Chemin critique : A → C → F → G → H.**

**Calculs à refaire pour s'entraîner :**
- `ES(D) = Max{EF(B) = 2 ; EF(C) = 3} = 3`
- `ES(E) = Max{EF(D) = 4 ; EF(J) = 3} = 4`
- `ES(H) = Max{EF(E) = 6 ; EF(G) = 7} = 7`
- `LF(C) = Min{LS(D) = 4 ; LS(F) = 3} = 3`
- `LF(E) = Min{LS(H) = 7 ; LS(I) = 7} = 7`
- `FF(J) = ES(E) − EF(J) = 4 − 3 = 1`
- `FF(I) = Fin − EF(I) = 8 − 7 = 1`

Le cas de projet complet est corrigé dans [07_cas_projet_corrige.md](07_cas_projet_corrige.md).
