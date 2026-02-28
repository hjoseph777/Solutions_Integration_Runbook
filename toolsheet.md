# Technical Validation Toolsheet
## Xerox — AP & ECM Integration (M-Files)

Use this as a one-page scoring workflow during technical validation.

## 0.1 Quick Start — Evaluator Checklist (5-Step Triage)

| Step | What to do | Evidence to capture | Pass Criteria | Target Time |
|---|---|---|---|---|
| 1. Scope the incident | Record affected function (Scan, Workflow, SQL/ODBC, Vault, OCR), impacted users, and start time | Ticket/update note with symptom + timestamp | Problem scope is clearly classified into one scenario | 5 min |
| 2. Verify platform health | Run baseline checks: `Get-Service "MFiles Server"`, `Get-Service XeroxConnectApp`, `Test-NetConnection SQLSVR -Port 1433`, `Test-NetConnection MFILESSVR -Port 2266` | Command output showing service state and port reachability | Required services are confirmed and network path is validated | 5–10 min |
| 3. Execute scenario playbook | Go to Scenario 1–5 decision tree and complete step-by-step resolution path | Notes of branch taken + actions performed + root cause | Root cause is identified and corrective action applied | 10–45 min |
| 4. Validate business recovery | Run one end-to-end test invoice (capture → metadata → approval path → ERP/SQL update) | Test object ID/invoice number + resulting workflow state + SQL confirmation | Transaction completes without error and reflects expected state | 10–20 min |
| 5. Close with audit trail | Document fix, owner, residual risk, and prevention action (automation/monitoring/update) | Final incident summary with sign-off and next-step owner | Incident is reproducible, auditable, and ready for handoff | 5–10 min |

**Evaluator Scoring (Quick):**
- **5/5:** Complete triage, validated recovery, strong evidence trail.
- **4/5:** Recovery complete, minor documentation gap.
- **3/5:** Partial recovery or limited validation evidence.
- **≤2/5:** No confirmed root cause or no end-to-end verification.

## 0.1-FR Démarrage rapide — Checklist évaluateur (triage en 5 étapes)

Utilisez cette section comme flux de notation rapide pendant une validation technique.

| Étape | Action à réaliser | Preuve à capturer | Critère de réussite | Durée cible |
|---|---|---|---|---|
| 1. Définir le périmètre | Identifier la fonction impactée (numérisation, workflow, SQL/ODBC, coffre M-Files, OCR), les utilisateurs touchés et l’heure de début | Note d’incident avec symptôme + horodatage | Le problème est classé clairement dans un scénario | 5 min |
| 2. Vérifier la santé de la plateforme | Exécuter les contrôles de base : `Get-Service "MFiles Server"`, `Get-Service XeroxConnectApp`, `Test-NetConnection SQLSVR -Port 1433`, `Test-NetConnection MFILESSVR -Port 2266` | Sorties de commandes (état des services + connectivité) | Les services requis et le chemin réseau sont validés | 5–10 min |
| 3. Exécuter le scénario du runbook | Suivre l’arbre de décision du Scénario 1 à 5 et appliquer la résolution étape par étape | Notes sur la branche suivie + actions + cause racine | Cause racine identifiée et correction appliquée | 10–45 min |
| 4. Valider la reprise métier | Exécuter un test de bout en bout (capture → métadonnées → approbation → mise à jour ERP/SQL) | ID document/facture + état workflow final + validation SQL | La transaction se termine sans erreur avec l’état attendu | 10–20 min |
| 5. Clôturer avec piste d’audit | Documenter la correction, le responsable, le risque résiduel et l’action préventive (automatisation/surveillance) | Résumé final avec approbation et responsable du suivi | Incident reproductible, auditable et prêt pour handoff | 5–10 min |

**Notation rapide (évaluateur) :**
- **5/5 :** Triage complet, reprise validée, preuves solides.
- **4/5 :** Reprise complète, léger manque documentaire.
- **3/5 :** Reprise partielle ou preuves de validation incomplètes.
- **≤2/5 :** Cause racine non confirmée ou validation bout en bout absente.

## 0.2 Evaluation Sign-off Template

Print or copy this block for technical validation handoff.

```text
============================================================
EVALUATION SIGN-OFF — SOLUTIONS INTEGRATION RUNBOOK
============================================================

Incident ID: ______________________________________________
Scenario Used (1-5): ______________________________________
Date/Time (Local): _________________________________________
Evaluator Name: ____________________________________________
Team/Department: ___________________________________________

Checklist Completion:
[ ] Step 1 Scope confirmed
[ ] Step 2 Platform health verified
[ ] Step 3 Scenario path executed
[ ] Step 4 End-to-end validation completed
[ ] Step 5 Audit trail documented

Outcome:
[ ] PASS
[ ] FAIL

Evidence References (ticket IDs, logs, screenshots, query output):
1) _________________________________________________________
2) _________________________________________________________
3) _________________________________________________________

Root Cause Summary:
____________________________________________________________
____________________________________________________________

Corrective Actions Applied:
____________________________________________________________
____________________________________________________________

Residual Risk / Follow-up Actions:
____________________________________________________________
____________________________________________________________

Approver / Reviewer: _______________________________________
Sign-off Date: _____________________________________________

============================================================
```

## 0.3 Modèle de validation — Français

Imprimez ou copiez ce bloc pour la validation technique en français.

```text
============================================================
VALIDATION FINALE — RUNBOOK D’INTÉGRATION DES SOLUTIONS
============================================================

ID de l’incident : _________________________________________
Scénario utilisé (1-5) : ___________________________________
Date/Heure (locale) : ______________________________________
Nom de l’évaluateur : ______________________________________
Équipe/Département : _______________________________________

Vérification de la checklist :
[ ] Étape 1 Périmètre confirmé
[ ] Étape 2 Santé de la plateforme vérifiée
[ ] Étape 3 Parcours du scénario exécuté
[ ] Étape 4 Validation de bout en bout terminée
[ ] Étape 5 Piste d’audit documentée

Résultat :
[ ] RÉUSSI
[ ] ÉCHEC

Références de preuve (ID ticket, journaux, captures, requêtes) :
1) _________________________________________________________
2) _________________________________________________________
3) _________________________________________________________

Résumé de la cause racine :
____________________________________________________________
____________________________________________________________

Actions correctives appliquées :
____________________________________________________________
____________________________________________________________

Risque résiduel / actions de suivi :
____________________________________________________________
____________________________________________________________

Approbateur / Réviseur : ___________________________________
Date de validation : _______________________________________

============================================================
```
