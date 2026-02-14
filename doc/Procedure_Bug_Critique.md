# Procédure simple – Bug critique

## 1) Trois indicateurs de suivi

1. **MTTA (Mean Time To Acknowledge)**
   - Temps entre la création de l’alerte et la prise en charge.
   - Objectif conseillé : **< 15 min**.

2. **MTTR (Mean Time To Resolve)**
   - Temps entre la détection et le retour à un service stable.
   - Objectif conseillé : à définir selon le SLA (ex. **< 4 h**).

3. **Taux de réouverture des incidents critiques**
   - Pourcentage d’incidents critiques rouverts après correction.
   - Objectif conseillé : **< 5 %**.

## 2) Procédure simple en cas de bug critique

### Étape 1 — Déclarer et qualifier (immédiat)
- Ouvrir un ticket « Critique / P1 ».
- Décrire : impact utilisateur, périmètre, heure de début, symptômes.
- Nommer un pilote d’incident.

### Étape 2 — Contenir l’impact (0–30 min)
- Activer un contournement si possible (rollback, désactivation feature, mode dégradé).
- Informer rapidement les parties prenantes (métier + technique).

### Étape 3 — Corriger (priorité absolue)
- Identifier la cause racine (logs, reproductions, dernier déploiement).
- Produire un correctif minimal et sûr.
- Faire une validation rapide ciblée (tests critiques).

### Étape 4 — Remettre en service et vérifier
- Déployer le correctif.
- Contrôler les fonctions critiques pendant 30–60 min.
- Confirmer le retour à la normale.

### Étape 5 — Clôturer et prévenir la récidive (J+1 max)
- Documenter : cause, correction, délais MTTA/MTTR, impact.
- Créer les actions préventives (test de non-régression, monitoring, alerte).
- Partager un mini RETEX (10 min) avec l’équipe.
