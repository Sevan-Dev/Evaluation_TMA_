# TMA – Maintenance Applicative

Ce document décrit le cadre de TMA (Tierce Maintenance Applicative) pour l’application :

- types de maintenance (corrective, évolutive, préventive)
- processus de traitement d’incident
- gestion des demandes d’évolution

## 1) Types de maintenance

### 1.1 Maintenance corrective

Objectif : corriger un défaut constaté en production ou en recette.

Exemples :
- erreur fonctionnelle (résultat incorrect)
- bug technique (exception, plantage)
- non-conformité par rapport au besoin initial

Livrables attendus :
- analyse de cause racine
- correctif versionné
- test(s) de non-régression
- compte-rendu d’intervention

### 1.2 Maintenance évolutive

Objectif : faire évoluer l’application pour répondre à un nouveau besoin métier ou réglementaire.

Exemples :
- ajout d’une nouvelle fonctionnalité
- modification d’un écran ou d’un workflow
- adaptation à une nouvelle règle métier

Livrables attendus :
- expression de besoin validée
- chiffrage (charge, délai, impacts)
- développement + tests
- documentation utilisateur/technique mise à jour

### 1.3 Maintenance préventive

Objectif : réduire le risque d’incident futur et améliorer la maintenabilité.

Exemples :
- mise à jour de dépendances
- refactoring de code complexe
- amélioration de couverture de tests
- durcissement sécurité et monitoring

Livrables attendus :
- plan de prévention
- interventions planifiées
- indicateurs d’amélioration (stabilité, performance, sécurité)

## 2) Processus de traitement d’incident

### Étape 1 — Détection et qualification
- Enregistrement du ticket (outil de ticketing)
- Qualification initiale : périmètre, impact, fréquence
- Attribution d’une priorité (P1 à P4)

### Étape 2 — Priorisation
- P1 : service indisponible / impact majeur (prise en charge immédiate)
- P2 : fonctionnalité critique dégradée
- P3 : incident mineur avec contournement possible
- P4 : anomalie faible impact

### Étape 3 — Diagnostic
- Analyse des logs, reproductions, vérification environnement
- Identification de la cause racine
- Proposition de correction ou de contournement temporaire

### Étape 4 — Correction
- Développement du correctif
- Revue de code
- Tests unitaires et tests de non-régression ciblés

### Étape 5 — Validation et mise en production
- Validation fonctionnelle (recette)
- Déploiement selon le processus de release
- Vérification post-déploiement

### Étape 6 — Clôture et retour d’expérience
- Clôture du ticket avec cause, action, date, version
- Communication aux parties prenantes
- Action préventive si incident récurrent

## 3) Gestion des demandes d’évolution

### 3.1 Collecte et cadrage
- Enregistrement de la demande
- Description du besoin, objectifs, valeur métier
- Identification des contraintes (délai, budget, conformité)

### 3.2 Analyse d’impact
- Impact fonctionnel, technique et organisationnel
- Dépendances et risques
- Estimation de charge et complexité

### 3.3 Arbitrage et priorisation
- Priorisation via critères : valeur métier, urgence, risque, effort
- Décision : accepté / reporté / refusé
- Planification dans le backlog ou la roadmap

### 3.4 Réalisation
- Rédaction des spécifications (si nécessaire)
- Développement en itérations courtes
- Tests (unitaires, intégration, recette)

### 3.5 Mise en production et suivi
- Déploiement
- Communication des changements
- Suivi des indicateurs d’adoption et de qualité

## 4) Indicateurs recommandés

- Délai moyen de prise en charge (MTTA)
- Délai moyen de résolution (MTTR)
- Taux de réouverture d’incidents
- Nombre d’incidents par criticité
- Respect des délais des évolutions
- Taux de réussite en production (sans rollback)

## 5) Rôles (exemple)

- **Demandeur métier** : exprime le besoin et valide
- **Support / Run** : enregistre et qualifie les incidents
- **Équipe TMA** : analyse, corrige, implémente les évolutions
- **Responsable applicatif / PO** : arbitre les priorités
