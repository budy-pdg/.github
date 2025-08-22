# Processus de travail de groupe

## Gestion du code source

Le code source de notre projet est stocké sur GitHub. Cela nous permet un travail coopératif et versionné. Cela nous permet aussi la vérification de notre travail pour la partie CI/CD.

Au sein de GitHub, notre code est réparti en plusieurs Repositories qui font partie d'une même Organization. Cette séparation nous permet de ne pas faire recharger le projet entier à chaque fois qu'un changement est fait, mais seulement de recharger la partie concernée.

### Structure

Voici notre Organization: [GitHub Budy-PDG](https://github.com/budy-pdg)

Voici les Repositories:

- Backend (Partie Render): [GitHub Budy-Backend](https://github.com/budy-pdg/budy-backend)
- Application (Partie Flutter): [GitHub Budy-App](https://github.com/budy-pdg/budy-app)
- Sondes (Partie des capteurs): [GitHub Budy-Probes](https://github.com/budy-pdg/budy-probes)
- Documentation (Informations générales et communes à tout le projet): [.github]()

### Rôles

Nous avons défini deux rôles pour Budy-PDG:

- devs: les développeurs et responsables de la création de l'application
- watchers: les responsables de la surveillance du processus de création

Chaque utilisateur devrait être classé comme l'un ou l'autre. Les autres utilisateurs ne devraient pas y avoir accès.

Nous allons définir des responsabilités plus précises, et des procédures. Cependant, certaines des fonctions qui nous permettrait de forcer ces procédures demandent un accès payant à GitHub, nous menant à définir ces règles de manière formelles, sans les forces techniquement, directement dans GitHub.

### Procédures de mise à jour

Le changement du contenu fait partie de la responsabilité des devs. Pour ce faire, voici déjà la description générale des branches GitHub et de leur importance:

- Branche main:
	- Version actuellement en production
	- Elle doit être stable et être mise à jour par étapes
	- Personne ne doit push des changements sur main
	- Les changements sur main ne devraient venir que de Pull Requests depuis la branche dev
	- Ces Pull Requests de dev à main nécessitent la review et l'approval de 2 développeurs (autre que celui assigné)
- Branche dev:
	- Version utilisée pour le développement
	- On ne devrait jamais push des changements directement sur cette branche
	- Les PR des autres branches devraient toutes pointer sur celle-ci
	- Tout le contenu ajouté à la branche via des PR devrait avoir été testé, et passer les pipelines
	- Nous avons un environnement de développement pour faire les tests et essais qui ne sont pas automatisés
	- Ces Pull Requests d'autres branches à dev nécessitent la review et l'approval de 1 développeurs (autre que celui assigné)
- Autres branches:
	- Nous allons créer des branches pour faire des modifications au contenu
	- Ces branches devraient être basées sur la branche dev
	- Les Pull Requests reliées à ces branches devraient être dirigées sur la branche dev

## Organisation des développeurs

### Communication

Nous utilisons plusieurs outils pour communiquer:

- GitHub: Canal nous permet d'avoir une communication traçable quand cela est nécessaire.
- Discord: Canal de discussion principal pour les discussions entre les déveoppeurs (que ce soit en groupe, ou entre les individus).
- Teams: Canal permettant la communication avec les watchers (enseignants, assistants), ainsi que le transfert de documents administratifs.

### Définition des tâches

Nos tâches sont définies par le [fichier d'exigences du projet](). Cependant, pour une plus grande granularité et un meilleur suivi, nous allons utiliser les issues.

Une issue représente une tâche, généralement. Ces tâches seront assignées (nous sommes limités à une personne assignée, mais plusieurs personnes peuvent travailler sur la même tâche si besoin est), et les Labels permettront un suivi général d'où on en est dans cette tâche. Voici les Labels utilisés:

- **Backlog** : Tâches a effectuer
- **En cours** : Tâches en train d’être effectuer
- **Review** : Tâches en cours de révision
- **Terminé** : Tâches terminée

Les Labels peuvent aussi être utilisé pour d'autres choses. Voici quelques autres Labels utilisés:

- **Question**: Discussion quant à un point d'incertitude, pas forcément une tâche
- **Bug**: Relevé d'un problème. Peut se voir attribuer un Label de tâche quand on a confirmé le problème et qu'on se met à le régler
- **Documentation**: Signifie que l'issue ne devrait pas impacter le fonctionnement du programme

En plus de cela, nous avons un [Canvas](https://github.com/orgs/budy-pdg/projects/1) qu'on doit mettre à jour pour une visualisation globale du travail à faire. Les nouvelles issues devraient y être ajoutées, et quand on change le Label d'une issue, on devrait mettre à jour le Canvas.

### Gestion du travail selon framework Scrum

Les développeurs doivent avancer dans leurs tâches de manière indépendante, et dans les temps. La présence à la HEIG-VD est obligatoire pour les présentations et autres activités nécessaires au projet qui ne peuvent être faites que sur place.

Les membres du groupe de développeurs se retrouvent aussi entre 2 et 3 fois par semaine (jours obligatoires inclus) à la HEIG-VD afin d'avoir un suivi en direct et une direction commune au projet. Ceci fait office de Sprint Planning. Le Sprint Retrospective se fait à la fin de la deuxième, afin de ne pas perdre trop de temps mais parler de la méthode de travail pour continuer d'avancer.

Un point journalier est fait tous les matins quand les membres sont à distance entre les développeurs pour discuter des avancements, problèmes, et de la suite du travail à faire. Ceci fait office de Daily Scrum. Bien entendu, d'autres rencontres sont possibles si nécessaires en dehors de ceci selon leur nécessité.

Les "parties prenantes", ici les enseignants et assistants, sont tenus au courant via notre équivalent du Sprint review, le rapport journalier via Teams.

Nous estimons qu'un "Sprint" prendra entre 1 et 3 jours de travail avec des équipes de 1 à 2 développeurs.

### Gestion des responsabilités

Étant donné la taille de l'équipe, nous n'allons pas avoir de product owner spécialement dédié à la tâche, ni de scrum master. Certains de nos développeurs seront aussi plus orientés sur ces tâches, mais reste principalement des développeurs.

Ceci étant, voici les spécialisations de nos développeurs initiaux:

- Vuilleumier Thomas: Responsabilité product owner et responsabilité scrum master
- Diaz Sebastian: Responsable graphisme
- Richard Aurélien: Responsable architecture
- Chollet Florian: Responsable sécurité
