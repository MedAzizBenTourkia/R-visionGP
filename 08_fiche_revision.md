# Fiche de révision

## Les chiffres et listes à connaître

- **3** caractéristiques d'un projet : temporaire, livrable unique, élaboration progressive.
- **3** contraintes : contenu, coût, délai. La qualité dépend de leur équilibre.
- **4** couches : système, management, projet, produit.
- **5** groupes de processus : démarrage, planification, exécution, maîtrise, clôture.
- **10** domaines : intégration, périmètre, délai, coût, qualité, ressources, communication, risques, approvisionnements, parties prenantes.
- **49** processus : chacun dans 1 seul groupe et 1 seul domaine.
- Stats : **29 %** réussite, **53 %** dépassement, **18 %** échec.

## Définitions express

| Terme | Définition |
|---|---|
| **Projet** | Entreprise temporaire pour un produit, service ou résultat unique |
| **Management de projet** | Connaissances, compétences, outils et techniques appliqués pour respecter les exigences et atteindre les objectifs |
| **PMP** | Document décrivant comment le système de management sera utilisé |
| **Risque** | Événement incertain à effet positif ou négatif sur un objectif |
| **Scope creep** | Périmètre non maîtrisé, qui ne cesse d'augmenter |
| **WBS** | Décomposition hiérarchique orientée livrables de tout le contenu |
| **Partie prenante** | Personne, groupe ou organisation qui affecte le projet ou est affecté par lui |
| **Validation du contenu** | Acceptation formelle du contenu achevé et des livrables |
| **Tâche critique** | TF = 0 |

## Pièges fréquents

| Faux | Vrai |
|---|---|
| Le produit est temporaire | Seul le **projet** est temporaire |
| Un risque est toujours négatif | Il peut être positif (**opportunité**) |
| FF = 0 implique TF = 0 | C'est **TF = 0 qui implique FF = 0** |
| AQ et CQ, c'est pareil | AQ : **avant**, en exécution. CQ : **après**, en maîtrise |
| Comparer PV et AC | **Jamais** : toujours passer par EV |
| Coût du risque = coût du retard | C'est le coût de la **réponse** au risque |
| Les groupes de processus se suivent | Ils **se chevauchent** |
| Charte et énoncé du périmètre, c'est pareil | La différence est le **niveau de détail** |
| Contrôle qualité = vérification du contenu | CQ : exigences qualité. Vérification : **acceptation** |
| ES se calcule avec Min | ES : **Max** des prédécesseurs. LF : **Min** des successeurs |

## Formules : échéancier

```
ES = Max{EF prédécesseurs}          LF = Min{LS successeurs}
EF = ES + D                         LS = LF − D
TF = LS − ES = LF − EF              FF = Min{ES successeurs} − EF
Durée estimée (3 points) = (dO + 4 dPP + dP) / 6
```

## Formules : coûts et trésorerie

```
Coût activité = (somme des taux) × durée
BAC = somme des coûts
EMV = probabilité × impact
CE triangulaire = (CO + CPP + CP) / 3
CE bêta = (CO + 4 CPP + CP) / 6
Recette d'un lot = coût × (1 + marge), encaissée avec le décalage
Besoin de financement = |cumul de trésorerie le plus négatif|
Financement externe = besoin − fonds propres
Bénéfice final = marge % × BAC (sert de contrôle)
```

## Formules : EVM

```
EV = % réel × BAC        PV = % planifié × BAC        AC = dépensé
PAR = BAC / SAC          Écart en temps = SV / PAR
CV = EV − AC             SV = EV − PV
CPI = EV / AC            SPI = EV / PV
EAC = AC + ETC           VAC = BAC − EAC
```

| Scénario | ETC | Durée restante | Résultat |
|---|---|---|---|
| **Tendance** | `(BAC − EV) / CPI` | `% restant / (% réel / t)` | `EAC = BAC / CPI`, délai `= SAC / SPI` |
| **Plan initial** | `BAC − EV` | `% restant × SAC` | `VAC = CV`, écart de délai `= SV / PAR` |
| **Finir comme prévu** | `BAC − AC` | `SAC − t` | Rythme `= % restant / (SAC − t)`, coût `= (BAC − AC) / (SAC − t)` |

**Mémo :** < 0 ou < 1 = **mauvais**. C = coût (budget), S = schedule (délai).

## Déroulé type d'un sujet

1. **Niveaux → réseau → ES/EF → LS/LF → TF/FF → chemin critique → Gantt.**
2. **Coût de chaque activité → BAC par lot → BAC total.**
3. **Dépenses par période → recettes décalées → flux net → cumul → besoin → plan de financement.**
4. **EV, PV, AC → SV, CV, SPI, CPI + interprétation → 3 scénarios.**

Toujours écrire la **formule**, le **calcul**, le **résultat avec unité**, puis **une phrase d'interprétation**.
