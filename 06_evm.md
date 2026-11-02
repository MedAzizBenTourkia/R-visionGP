# Séance 5 : Suivi du projet par la valeur acquise (EVM)

> **À retenir :** l'EVM mesure coût, délai et contenu **ensemble**. Toute analyse part de **EV**. Écart **négatif** ou indice **< 1** : c'est défavorable.

## 1. Pourquoi l'EVM ?

Comparer séparément le délai réel au délai planifié, le coût réel au coût estimé et le contenu réalisé au contenu planifié ne suffit pas. L'**Earned Value Management (gestion par la valeur acquise)** tient compte de l'équilibre entre les trois contraintes.

> **Attention : ne jamais comparer PV avec AC.** Exemple : PV = AC = 1 600 TND semble parfait, mais si EV = 1 200, on a en réalité 2 jours de retard et 400 TND de dépassement.

## 2. Les 3 valeurs de base

| Sigle | Nom | Question | Coût | Travail |
|---|---|---|---|---|
| **EV** | Earned Value, Valeur Acquise | Que **vaut** le travail fait, au prix prévu ? | Estimé | **Réalisé** |
| **PV** | Planned Value, Valeur Planifiée | Que devrait-on avoir fait à cette date ? | Estimé | **Planifié** |
| **AC** | Actual Cost, Coût Réel | Combien a-t-on vraiment dépensé ? | **Réel** | Réalisé |

## 3. Toutes les formules

| Sigle | Nom | Formule | Lecture |
|---|---|---|---|
| **BAC** | Budget initial | Somme des coûts | |
| **SAC** | Délai initial | Durée planifiée | |
| **PAR** | Taux de réalisation planifié | `BAC / SAC` | Coût planifié d'une journée |
| **EV** | Valeur acquise | `% avancement réel × BAC` | |
| **PV** | Valeur planifiée | `% planifié × BAC` (= `PAR × t` si le coût est régulier) | |
| **CV** | Écart de coût | `EV − AC` | < 0 : dépassement |
| **SV** | Écart de délai | `EV − PV` | < 0 : retard |
| | Écart en jours | `SV / PAR` | |
| **CPI** | Indice de performance coût | `EV / AC` | < 1 : on perd de l'argent |
| **SPI** | Indice de performance délai | `EV / PV` | < 1 : on est en retard |
| **ETC** | Estimation pour compléter | Selon le scénario | Coût restant |
| **EAC** | Estimation fin de projet | `AC + ETC` | Nouveau coût total |
| **VAC** | Écart à la fin | `BAC − EAC` | < 0 : perte |

### Interprétation

| Résultat | Sens |
|---|---|
| CV > 0, CPI > 1 | Sous le budget |
| CV = 0, CPI = 1 | Conforme au budget |
| CV < 0, CPI < 1 | **Dépassement** du budget |
| SV > 0, SPI > 1 | En avance |
| SV = 0, SPI = 1 | Dans les temps |
| SV < 0, SPI < 1 | **Retard** |

## 4. Les 3 scénarios de fin de projet

| | Scénario 1 : la tendance continue | Scénario 2 : retour au plan initial | Scénario 3 : finir comme prévu |
|---|---|---|---|
| **Hypothèse** | La performance actuelle reste la même | Cause corrigée, le **reste** se fait aux conditions initiales | Respecter BAC et SAC |
| **ETC (coût)** | `(BAC − EV) / CPI` | `BAC − EV` | `BAC − AC` |
| **Durée restante** | `Travail restant / vitesse réelle` | `Travail restant / vitesse planifiée` | `SAC − t` |
| **EAC** | `AC + ETC` (= `BAC / CPI`) | `AC + ETC` | `= BAC` |
| **Délai total** | `t + reste` (= `SAC / SPI`) | `t + reste` | `= SAC` |
| **Écarts** | Aggravés | Écarts du jour t conservés | **Récupérés** (0) |

> Dans le scénario 2, VAC est égal au **CV actuel**, et l'écart de délai au **retard actuel**. Dans le scénario 3, on demande le **rythme** et le **coût** à tenir sur le reste du projet.

## 5. Exemple complet du cours : la clôture

**Données :** 150 m, 20 TND/m, 10 m/jour. Après **8 jours** : avancement réel 40 %, coût réel 1 800 TND.

### Base

| Calcul | Résultat |
|---|---|
| `BAC = 150 × 20` | **3 000 TND** |
| `SAC = 150 / 10` | **15 jours** |
| `PAR = 3 000 / 15` | **200 TND/jour** |
| `EV = 40 % × 150 m × 20 = 60 × 20` | **1 200 TND** |
| `PV = 8 × 10 m × 20 = 80 × 20` | **1 600 TND** |
| `AC` | **1 800 TND** |

### Analyse à J8

| Calcul | Résultat | Sens |
|---|---|---|
| `CV = 1 200 − 1 800` | **−600 TND** | Dépassement de budget |
| `SV = 1 200 − 1 600` | **−400 TND** | Retard |
| `SV / PAR = −400 / 200` | **−2 jours** | Retard de 2 jours |
| `CPI = 1 200 / 1 800` | **0,667** | On récupère 667 millimes par dinar dépensé, on en perd 333 |
| `SPI = 1 200 / 1 600` | **0,75** | Avancement à 75 % du plan : 8 jours de travail n'en valent que 6 |

### Scénarios (il reste 90 m)

| | S1 : tendance | S2 : plan initial | S3 : finir comme prévu |
|---|---|---|---|
| **Performance sur le reste** | 30 TND/m et 7,5 m/j | 20 TND/m et 10 m/j | 13,33 TND/m et 12,86 m/j |
| **D'où vient-elle ?** | 1 800 / 60 m et 60 m / 8 j | Plan initial (ex. : le seau troué qui gaspillait le mortier est remplacé) | 1 200 TND / 90 m et 90 m / 7 j (ex. : permuter les équipes) |
| **ETC** | 90 × 30 = **2 700** | 90 × 20 = **1 800** | 3 000 − 1 800 = **1 200** |
| **Durée restante** | 90 / 7,5 = **12 j** | 90 / 10 = **9 j** | 15 − 8 = **7 j** |
| **EAC** | **4 500 TND** | **3 600 TND** | **3 000 TND** |
| **Délai total** | **20 j** | **17 j** | **15 j** |
| **VAC** | **−1 500 TND** | **−600 TND** | **0** |
| **Écart de délai** | **−5 j** | **−2 j** | **0** |

## 6. Les courbes en S

Elles permettent de **lire** les indicateurs directement sur le graphe, et de voir l'effet d'une variation par simple glissement.

```
TND
 │                                      ╭── AC prolongée → EAC
BAC ┤- - - - - - - - - - - - - - ╭──── PV
 │                         ╭─────╯
 │             AC ●───╮  ╭─╯
 │                │CV │ ╱
 │             PV ●   │╱
 │                │SV ╱
 │             EV ●──╯
 │              ╱
 └──────────────┬─────────────┬─────────► temps
              date t         SAC
```

**Lecture à la date t (écarts verticaux) :**
- Écart entre EV et AC = **CV**.
- Écart entre EV et PV = **SV**.
- Fin de la courbe AC prolongée = **EAC** et nouveau délai.

**Autre lecture des diapos :** avec AC = 2 550, EV = 1 800, PV = 2 120, on a SV = −320 et CV = −750.

## 7. Cas à analyser

**Cas A, le projet va bien :** après 8 jours, 70 % réalisé, coût réel 1 400 TND.
- EV = 2 100, PV = 1 600, AC = 1 400.
- Réalisé 105 m, soit 13,33 TND/m et 13,125 m/j.
- SV = **+500** (en avance), CV = **+700** (économie).

**Cas B, le piège :** après 8 jours, 40 % réalisé, coût réel 1 600 TND.
- PV = 1 600 = AC, mais EV = 1 200.
- SV = **−400** (2 jours de retard), CV = **−400** (dépassement).
