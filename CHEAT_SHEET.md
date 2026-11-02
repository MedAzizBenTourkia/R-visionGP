# Project Management Cheat Sheet

Explanations are in English. Terms in **bold** are the ones used in the course and on the exam.

## 1. Theory in 60 seconds

- **Projet:** temporary work that creates a unique result. It has 3 traits: **temporaire, livrable unique, élaboration progressive**.
- **Opération:** continuous, repetitive work. Projects have negative cash flow, operations positive.
- **Triple contrainte:** **contenu, coût, délai**. Changing one affects at least one other. Quality depends on their balance.
- **4 couches:** **système, management, projet, produit**.
- **5 groupes de processus:** **démarrage, planification, exécution, maîtrise, clôture**. They overlap.
- **10 domaines:** **intégration, périmètre, délai, coût, qualité, ressources, communication, risques, approvisionnements, parties prenantes**.
- **49 processus:** each belongs to exactly 1 group and 1 area.
- **WBS:** breaks down all the work by deliverable, down to the **lot de travail**. The team creates it.
- **Scope creep:** scope keeps growing because it isn't controlled.
- **Risque:** uncertain event, positive or negative. **EMV = probabilité × impact**.

| Easily confused | Remember |
|---|---|
| Assurance vs. contrôle qualité | **AQ:** before, in exécution. **CQ:** after, in maîtrise |
| Charte vs. énoncé du périmètre | The difference is the level of detail: charter is high-level |
| Contrôle qualité vs. vérification du contenu | CQ checks quality requirements. Vérification is about acceptance |
| Bottom-up vs. top-down | Bottom-up when characteristics are imposed. Top-down when the budget is imposed |
| Coût du risque | The cost of the **response** (the tarps), not of the delay |

## 2. Schedule: forward, then backward

1. **Niveaux:** no predecessor = level 1. Otherwise, highest predecessor level + 1.
2. **Forward:** `ES = Max(EF of predecessors)`, then `EF = ES + D`. The first ES is 0.
3. **Project duration:** the largest EF.
4. **Backward:** `LF = Min(LS of successors)`, then `LS = LF − D`. Final tasks have LF = project duration.
5. **Floats:** `TF = LS − ES`. `FF = Min(ES of successors) − EF`. For a final task, `FF = project duration − EF`.
6. **Critical path:** every task with TF = 0.

Task box: top row `ES | TF | EF`, middle `D | Activité`, bottom `LS | FF | LF`.

**Traps:** TF = 0 forces FF = 0, but FF = 0 doesn't force TF = 0. Forward uses Max, backward uses Min.

**Three-point estimate:** `(dO + 4dPP + dP) / 6`. For costs, beta uses the same formula and triangular is `(CO + CPP + CP) / 3`.

## 3. Budget and cash flow

1. **Activity cost** = (sum of resource rates) × duration.
2. **BAC** = sum of activity costs.
3. **Expenses per period:** spread the costs using the earliest dates.
4. **Income:** package cost × (1 + margin), received after the payment delay.
5. **Net flow** = income − expenses. **Cumul** = previous cumul + net flow.
6. **Besoin de financement** = the absolute value of the lowest cumul.
7. **Financement externe** = besoin − fonds propres.
8. **Check:** final cumul = margin % × BAC.

**Repayment plan used in the notes:** spend own funds first, repay external funding first.

## 4. EVM: always start from EV

| Value | Meaning | Formula |
|---|---|---|
| **EV** | What the finished work is worth at planned cost | `real % × BAC` |
| **PV** | What should be done by now | `planned % × BAC`, or `PAR × t` if the cost is regular |
| **AC** | What was really spent | Given |
| **PAR** | Planned cost per time unit | `BAC / SAC` |

| Indicator | Formula | Bad when |
|---|---|---|
| **CV** (cost) | `EV − AC` | < 0 |
| **SV** (schedule) | `EV − PV`; in time units: `SV / PAR` | < 0 |
| **CPI** (cost) | `EV / AC` | < 1 |
| **SPI** (schedule) | `EV / PV` | < 1 |

**Never compare PV with AC.** Both comparisons go through EV.

| Scenario | ETC | Time remaining | End result |
|---|---|---|---|
| **a) Trend continues** | `(BAC − EV) / CPI` | `remaining % ÷ (real % / t)` | `EAC = BAC / CPI`, total time `= SAC / SPI` |
| **b) Back to the plan** | `BAC − EV` | `remaining % × SAC` | VAC = current CV, delay = current delay |
| **c) Finish as planned** | `BAC − AC` | `SAC − t` | VAC = 0. Give `remaining % / (SAC − t)` and `(BAC − AC) / (SAC − t)` per time unit |

Every scenario: `EAC = AC + ETC`, `VAC = BAC − EAC`, time gap `= SAC − total time`.

### Worked example: the fence

BAC 3,000, SAC 15 days, day 8, 40% done, AC 1,800.

| Step | Result |
|---|---|
| PAR = 3,000 / 15 | 200 per day |
| EV = 40% × 3,000 | 1,200 |
| PV = 8 × 200 | 1,600 |
| CV = 1,200 − 1,800 | −600: over budget |
| SV = 1,200 − 1,600 | −400, so −2 days: late |
| CPI = 1,200 / 1,800 | 0.667 |
| SPI = 1,200 / 1,600 | 0.75 |

| Scenario | ETC | EAC | VAC | Total time |
|---|---|---|---|---|
| a) Trend | 1,800 / 0.667 = 2,700 | 4,500 | −1,500 | 20 days |
| b) Plan | 3,000 − 1,200 = 1,800 | 3,600 | −600 | 17 days |
| c) As planned | 3,000 − 1,800 = 1,200 | 3,000 | 0 | 15 days |

## 5. On the exam

- Write the formula, then the calculation, then the result with its unit.
- Add one sentence of interpretation, for example: **« Le projet est en retard de 2 jours et en dépassement de budget de 600 DT. »**
- Check your work: the critical path adds up to the project duration, and the final cumul equals the profit.
