# Processus de contribution au projet Budy

## Gestion du code source

Le code source du projet est hébergé sur GitHub, au sein de l’organisation [Budy-PDG](https://github.com/budy-pdg).
Il est réparti en plusieurs dépôts pour séparer clairement les parties techniques :

- Backend (Render) : [budy-backend](https://github.com/budy-pdg/budy-backend)
- Application mobile (Flutter) : [budy-app](https://github.com/budy-pdg/budy-app)
- Capteurs (probes) : [budy-probes](https://github.com/budy-pdg/budy-probes)
- Documentation : [.github](https://github.com/budy-pdg/.github)

Cette séparation permet de limiter les rechargements aux seules parties modifiées et de garder une organisation claire.

## Rôles

Deux rôles principaux existent dans notre organisation :

- `devs` : développeurs responsables de la création de l’application
- `watchers` : responsables du suivi et de la surveillance du processus de création

Ces rôles guident la répartition des responsabilités. Certaines fonctionnalités GitHub permettant de les imposer nécessitent un plan payant, c’est pourquoi nous définissons ces règles formellement dans cette documentation.

## Gestion des branches

- **Branche `main`**
  - Contient la version en production.
  - Stable et mise à jour uniquement par des *Pull Requests* depuis `dev`.
  - Nécessite la validation par 2 développeurs (hors auteur du changement).

- **Branche `dev`**
  - Contient la version de développement.
  - Toutes les PR (des autres branches) doivent pointer vers `dev`.
  - Chaque modification doit passer les tests et pipelines.
  - Validation requise par 1 développeur (hors auteur du changement).

- **Branches de fonctionnalités**
  - Créées pour chaque modification.
  - Basées sur `dev`.
  - Fusionnées vers `dev` via PR.

## Communication

- **GitHub** : communication traçable (issues, PR).  
- **Discord** : discussions informelles entre développeurs.  
- **Teams** : communication avec les *watchers* (enseignants, assistants) et documents administratifs.  

## Langues utilisées

- **Anglais** : code (dont commentaires), visuels, application
- **Français** : Documentation hors code, communication entre développeurs (et avec enseignants et assistants)

## Gestion des tâches

Les tâches sont gérées via les *issues* GitHub et le [Projet/Canvas](https://github.com/orgs/budy-pdg/projects/1).  

Labels utilisés :
- **Backlog** : tâche à faire
- **En cours** : tâche en cours
- **Review** : tâche en révision
- **Terminé** : tâche terminée
- **Question**, **Bug**, **Documentation** : pour discussions et signalements spécifiques  

## Méthodologie (Scrum)

- **Réunions** : 2–3 fois par semaine à la HEIG-VD, + présence obligatoire pour les présentations.  
- **Daily Scrum** : point rapide chaque matin (à distance).  
- **Sprint planning** : défini lors des rencontres physiques.  
- **Sprint retrospective** : fin de la 2ᵉ semaine.  
- **Sprint review** : rapport journalier via Teams pour les enseignants/assistants.  

## Spécialisations des développeurs

- Vuilleumier Thomas : Product Owner + Scrum Master  
- Diaz Sebastian : Responsable graphisme  
- Richard Aurélien : Responsable architecture  
- Chollet Florian : Responsable sécurité  
