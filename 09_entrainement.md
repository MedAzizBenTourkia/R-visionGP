# Entraînement

> Les pages « Quizz » des diapos sont vides. Ces questions ont donc été **rédigées à partir du cours** : ce ne sont pas des questions officielles. Les réponses sont à la fin.

## QCM

**1.** Laquelle n'est pas une caractéristique d'un projet ?
a) Temporaire b) Répétitif c) Livrable unique d) Élaboration progressive

**2.** Un projet a généralement un cash-flow :
a) Positif b) Nul c) Négatif d) Constant

**3.** Une chaîne de montage automobile est :
a) Un projet b) Une opération c) Un programme d) Un livrable

**4.** Combien de groupes de processus, de domaines et de processus dans le PMBOK du cours ?
a) 5, 10, 49 b) 10, 5, 49 c) 5, 9, 47 d) 4, 10, 49

**5.** Obtenir l'autorisation de démarrer une phase relève du groupe :
a) Planification b) Exécution c) Démarrage d) Maîtrise

**6.** L'assurance qualité se situe :
a) Après la réalisation, en maîtrise b) Avant la réalisation, en exécution c) Après la réalisation, en clôture d) Avant la réalisation, en démarrage

**7.** Le scope creep désigne :
a) Un retard de planning b) Un dépassement de budget c) Un périmètre non maîtrisé d) Un risque positif

**8.** La différence principale entre charte et énoncé du périmètre est :
a) L'auteur b) Le niveau de détail c) Le budget d) La date

**9.** Une WBS est orientée vers :
a) Les personnes b) Les coûts c) Les livrables d) Les dates

**10.** Le niveau le plus bas d'une WBS est :
a) Le sous-projet b) La phase c) Le lot de travail d) Le jalon

**11.** Si la marge libre d'une tâche est nulle :
a) Elle est forcément critique b) Sa marge totale peut être positive c) Le projet est en retard d) Elle n'a pas de successeur

**12.** Une estimation de risque : probabilité 25 %, impact 8 000 DT. L'EMV vaut :
a) 800 DT b) 2 000 DT c) 8 000 DT d) 32 000 DT

**13.** L'estimation descendante (top-down) est utilisée quand on exige :
a) Les caractéristiques b) Le budget c) La qualité d) Les ressources

**14.** Si CPI = 1,2 et SPI = 0,8, le projet est :
a) En avance et sous le budget b) En retard et sous le budget c) En avance et au-dessus du budget d) En retard et au-dessus du budget

**15.** Pour une estimation à la fin selon la tendance actuelle, on utilise :
a) `EAC = AC + BAC − EV` b) `EAC = BAC / CPI` c) `EAC = BAC − AC` d) `EAC = EV / AC`

## Exercice 1 : échéancier

| Tâche | D (j) | Prédécesseurs |
|---|---|---|
| A | 2 | - |
| B | 4 | A |
| C | 3 | A |
| D | 5 | B |
| E | 2 | B, C |
| F | 3 | D, E |

Calculez ES, EF, LS, LF, TF et FF. Donnez la durée et le chemin critique.

## Exercice 2 : EVM

BAC = 50 000 DT, SAC = 10 mois, coût régulier. À la fin du mois 4 : avancement 30 %, coût réel 18 000 DT.

1. Calculez EV, PV, AC, SV, CV, SPI, CPI. Interprétez.
2. Tendance actuelle : ETC, EAC, VAC, délai total.
3. Retour au plan initial : ETC, EAC, VAC, délai total.
4. Pour finir comme prévu : avancement et coût par mois.

## Exercice 3 : trésorerie

Un projet coûte 4 000 DT par période sur 3 périodes. Il comporte 2 lots : le lot 1 (coût 4 000 DT) finit en P1, le lot 2 (coût 8 000 DT) finit en P3. La marge est de 25 % et le décalage de paiement de 1 période. Fonds propres : 3 000 DT.

Donnez le tableau, le besoin de financement et le financement externe.

---

## Réponses

**QCM :** 1-b, 2-c, 3-b, 4-a, 5-c, 6-b, 7-c, 8-b, 9-c, 10-c, 11-b, 12-b, 13-b, 14-b, 15-b.

**Exercice 1 :**

| Tâche | ES | EF | LS | LF | TF | FF |
|---|---|---|---|---|---|---|
| **A** | 0 | 2 | 0 | 2 | 0 | 0 |
| **B** | 2 | 6 | 2 | 6 | 0 | 0 |
| C | 2 | 5 | 6 | 9 | 4 | 1 |
| **D** | 6 | 11 | 6 | 11 | 0 | 0 |
| E | 6 | 8 | 9 | 11 | 3 | 3 |
| **F** | 11 | 14 | 11 | 14 | 0 | 0 |

Durée : **14 j**. Chemin critique : **A → B → D → F**.

**Exercice 2 :**
1. EV = 15 000, PV = 20 000, AC = 18 000. SV = −5 000 (−1 mois, car PAR = 5 000). CV = −3 000. SPI = 0,75. CPI = 0,833. **En retard et en dépassement.**
2. ETC = 35 000 / 0,8333 = **42 000**. EAC = **60 000**. VAC = **−10 000**. Délai = 4 + 70 / 7,5 = **13,33 mois**.
3. ETC = **35 000**. EAC = **53 000**. VAC = **−3 000**. Délai = 4 + 7 = **11 mois**.
4. Reste 6 mois, 70 %, 32 000 DT : **11,67 % par mois** et **5 333,33 DT par mois**.

**Exercice 3 :** recettes : lot 1 = 5 000 en P2 ; lot 2 = 10 000 en P4.

| | P1 | P2 | P3 | P4 |
|---|---|---|---|---|
| Dépenses | 4 000 | 4 000 | 4 000 | 0 |
| Recettes | 0 | 5 000 | 0 | 10 000 |
| Flux net | −4 000 | +1 000 | −4 000 | +10 000 |
| Cumul | −4 000 | −3 000 | **−7 000** | +3 000 |

Besoin : **7 000 DT**. Externe : 7 000 − 3 000 = **4 000 DT**. Contrôle : 25 % × 12 000 = 3 000 DT.
