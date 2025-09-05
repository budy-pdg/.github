# Exigences du projet Budy

## Définitions

- **Budy** : Nom de l’application, jeu de mots entre « Bud » (bourgeon) et « Buddy » (copain), qui reflète l’aspect social du projet.
- **Budies** : Capteurs physiques permettant de surveiller les plantes. Ils doivent être placés dans la terre, conformément au manuel fourni avec le capteur.
- **Alerte** : Règle définissant quand un incident doit être envoyé.
- **Incident** : Information liée au déclenchement d’une alerte.

---

## Exigences fonctionnelles

1.	Un utilisateur devrait avoir la capacité de se créer un compte sur l’application à l’aide d’un nom d’utilisateur unique, d’une adresse email unique, et d’un mot de passe (6 charactères ou plus).
2.	Un utilisateur devrait pouvoir se connecter à l’application via son username et son mot de passe.
3.	Un utilisateur devrait être capable de se rajouter une/retirer son/changer son image de profile.
4.	Un utilisateur devrait pouvoir se déconnecter.
5.	Un utilisateur devrait avoir un aperçu rapide de ses plantes dans une liste sur une page dédiée, où des informations basiques sur chaque plante et leur état devrait être mentionné.
6.	Un utilisateur devrait pouvoir générer une entrée dans sa liste de plantes
    1.	Obligatoire : lui attribuer un nom
    2.	Optionnel : renseigner le type de la plante parmi celles de notre database, si présente, afin d’obtenir des alertes préconfigurées
7.	Un utilisateur devrait pouvoir, depuis cette liste, accéder à une page présentant les détails quant à la plante, ainsi que des options. Ces détails et options devraient inclure :
    1.	Image, si assignée
    2.	Son nom
    3.	Ses statistiques actuelles (selon informations récoltées)
    4.	Des graphes de ses statistiques au cours du temps
    5.	Configurer les alertes (voir plus loin pour les détails des alertes)
8.	Pour chaque plante ayant un budy assigné, l’application devrait faire de la collecte de données de manière régulière, et de stocker ces données pour une utilisation et un affichage ultérieur.
9.	L’utilisateur devrait pouvoir, pour chaque plante, voir ses alertes.
    1.	Une alerte peut être active ou inactive. Une alerte peut être rendue inactive par l’utilisateur, supprimée par l’utilisateur, ou rendue active par l'utilisateur.
    2.	Quand une alerte active se déclenche, elle envoie un incident au stockage interne à l’application.
    3.	L’alerte est définie par un nom, et des conditions d’activation vérifiées à l'arrivée de données. Elle a aussi une sévérité.
    4. Une alerte ne devrait pas pouvoir se déclencher si elle s'est déjà déclenché récemment (période de 6h).
10.	Un incident contiendra toutes les informations quant au déclenchement d’une alerte. Ceci inclut :
    1.	La plante concernée
    2.	Le nom de l’alerte
    3.	La sévérité de l’alerte
    4.	La date d'activation
11.	Un utilisateur devrait pouvoir aller sur la partie communautaire de l’application, et voir les postes des personnes qu'il suit, sous la forme d’une liste contenant des informations minimales sur chacun des postes.
12.	Un utilisateur devrait avoir l’options de suivre des gens (via leur username), et ce de manière unilattérale (pas de notions d'accepter des demandes).
13.	Un utilisateur devrait pouvoir arrêter de suivre des gens.
14.	Un utilisateur devrait pouvoir mettre un poste comme favori.
15.	Un utilisateur devrait pouvoir retirer un poste de ses favoris.
16.	Un utilisateur devrait pouvoir aller sur la page d’un de ces postes, et obtenir le poste détaillé, contenant toutes les informations du poste. Ceci pourrait inclure :
    1.	Un titre au poste
    2.	Une image reliée
    3.	Une plante reliée
    4.	Un message
    5.	Les commentaires et réponses au poste
17.	L’utilisateur devrait pouvoir commenter sur un poste, ou répondre à un commentaire, sous la forme de texte.
18.	L’utilisateur devrait pouvoir supprimer son commentaire ou sa réponse, laissant un message à la place semblable à « Message supprimé ».
19.	L’utilisateur recevra des notifications dans le stockage interne à l'application si/quand un autre utilisateur répond à un de ses commentaires/à un de ses posts/dans un post qu'il suit.
20.	L’utilisateur devrait pouvoir ajouter un poste, contenant toutes ou seulement certaines des informations mentionnées ci-dessus (obligatoire : titre ; optionnel : message, plante reliée, image).
21.	L’utilisateur devrait pouvoir supprimer son poste, supprimant toutes les informations, commentaires, réponses, images, etc. y étant relié.
22.	L’utilisateur devrait avoir une visualisation sur les notifications reçues dans l’application, permettant un accès rapide aux informations concernées. 
23. L'utilisateur devrait pouvoir, de la même manière, accéder à ses incidents.

## Exigences non-fonctionnelles

1.	Le groupe de travail doit être de 3 ou 4 personnes (4)
2.	Le groupe doit documenter sa composition dans un fichier excel disponible dans le canal « Général » Teams de l’équipe PDG Classroom 2025 (Groupe 9)
3.	Le travail doit être effectué dans un délai de 3 semaines
4.	Le projet doit inclure les étapes intermédiaires et rendus aux dates indiquées dans la présentation initiale
    1.	Semaine 1
        1.	Description du projet (objectif, requirements fonctionnels, requirements    non    fonctionnels)
        2.	Description préliminaire de l’architecture
        3.	Mockups (Figma, papier-crayon, etc.)
        4.	Landing page mise en ligne
        5.	Description des choix techniques
        6.	Description du processus de travail (p.ex. : git flow, devops, etc.)
        7.	Mise en place des outils de développement (Issue tracker … etc.)
        8.	Mise en place d’un environnement de déploiement
        9.	Mise en place d’une pipeline de livraison et de déploiement (CI/CD)
        10.	Démonstration du déploiement d’une modification
    2.	Semaine 3
        1.	Description du problème et de la solution
        2.	Code source du projet
        3.	Instructions reproductibles pour lancer le projet en local
        4.	Instructions reproductibles pour déployer une nouvelle fonctionnalité avec  la   pipeline de CI/CD
        5.	Instructions de contribution au projet (quel est le workflow adopté,    comment    quelqu’un d’externe peut contribuer)
        6.	Vidéo de présentation de 1-4 minutes
        7.	Présentation et démonstration en classe la dernière semaine (15 minutes, dont 5 minutes de questions et la vidéo)
5.	Le groupe doit être à disposition pour travailler à 100% durant ces 3 semaines
6.	Le groupe doit rester en contact avec le groupe des enseignants et assistants pour un suivi de leur travail
    1.	Les groupes doivent, chaque matin, remplir le formulaire de point journalier à rendre dans le canal Teams créé pour chaque groupe
7.	Les outils utilisés devraient minimiser les coûts du projet, sinon ne pas engendrer de coûts du tout. Certaines ressources sont à disposition des groupes.
8.	La gestion de l’authentification des utilisateurs devrait être gérée selon les pratiques classiques de la cybersécurité.
9.	Autres mesures de cybersécurité générales à déterminer pour empêcher de potentielles attaques sur l’application.
