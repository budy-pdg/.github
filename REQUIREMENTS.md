# Exigences du projet Budy

## Définitions

- **Budy** : Nom de l’application, jeu de mots entre « Bud » (bourgeon) et « Buddy » (copain), qui reflète l’aspect social du projet.
- **Budies** : Capteurs physiques permettant de surveiller les plantes. Ils doivent être placés dans la terre, conformément au manuel fourni avec le capteur.
- **Alerte** : Règle définissant quand un incident doit être envoyé.
- **Incident** : Information liée au déclenchement d’une alerte.

---

## Exigences fonctionnelles

1.	Un utilisateur devrait avoir la capacité de se créer un compte sur l’application à l’aide d’un nom d’utilisateur unique, d’une adresse email unique, et d’un mot de passe.
2.	Un utilisateur devrait pouvoir se connecter à l’application via son adresse email et son mot de passe.
3.	Un utilisateur devrait être capable de changer son mot de passe, son nom d’utilisateur, et de se rajouter une/retirer son/changer son image de profile.
4.	Un utilisateur devrait pouvoir se déconnecter.
5.	Un utilisateur devrait avoir un aperçu rapide de ses plantes dans une liste sur une page dédiée, où des informations basiques sur chaque plante et leur état devrait être mentionné.
6.	Un utilisateur devrait pouvoir générer une entrée dans sa liste de plantes
    1.	Obligatoire : lui attribuer un nom unique (unique parmi sa propre liste, plusieurs utilisateurs peuvent avoir le même nom de plante).
    2.	Optionnel : renseigner le type de la plante parmi celles de notre database, si présente, afin d’obtenir des alertes préconfigurées
7.	Un utilisateur devrait pouvoir filtrer/trier la liste de plantes selon plusieurs critères (« A un budy assigné », « Ordre alphabétique », etc.).
8.	Un utilisateur devrait pouvoir, depuis cette liste, accéder à une page présentant les détails quant à la plante, ainsi que des options. Ces détails et options devraient inclure :
    1.	Image(s), si assignée(s), ou/et de quoi ajouter une image
    2.	Son nom
    3.	Ses statistiques actuelles (selon informations récoltées)
    4.	Des graphes de ses statistiques au cours du temps
    5.	De quoi ajouter un budy si aucun budy n’est assigné, ou de quoi libérer le budy assigné s’il y en a un
    6.	De quoi supprimer la plante de sa liste
        1.	Si un budy est associé, le libère
        2.	Les données des statistiques sont supprimées
        3.	L’image est supprimée
    7.	Configurer les alertes (voir plus loin pour les détails des alertes)
9.	Un utilisateur devrait être capable, en ayant un budy pas encore assigné, de l’enregistrer à une plante (chaque budy ne peut être lié qu’à une plante à la fois).
10.	Pour chaque plante ayant un budy assigné, l’application devrait faire de la collecte de données de manière régulière (configurable, pas inférieur à fréquence min.), et de stocker ces données pour une utilisation et un affichage ultérieur.
11.	L’utilisateur devrait pouvoir, pour chaque plante, créer des alertes.
    1.	Une alerte peut être active ou inactive. Une alerte ne peut être active que s’il y a un budy assigné. Une alerte peut être rendue inactive par l’utilisateur, supprimée par l’utilisateur, ou rendue active si elle respecte la condition ci-dessus.
    2.	Quand une alerte active se déclenche, elle envoie une notification d’incident à l’appareil sur lequel l’application est installée (si l’application a le droit d’envoyer des notifications). Elle rajoute aussi dans tous les cas la notification au stockage interne à l’application.
    3.	L’alerte est définie par un nom unique (par plante), et des conditions d’activation vérifiées périodiquement. Elle a aussi une sévérité. 
12.	Un incident contiendra toutes les informations quant au déclenchement d’une alerte. Ceci inclut :
    1.	La plante concernée
    2.	Le nom de l’alerte
    3.	La sévérité de l’alerte
    4.	La période d’activation (début, et si applicable, fin)
13.	Un utilisateur devrait pouvoir aller sur la partie communautaire de l’application, et voir les postes de ses amis, sous la forme d’une liste contenant des informations minimales sur chacun des postes.
14.	Un utilisateur devrait avoir l’options de faire des demandes d’amitié, et d’accepter ou refuser de telles demandes qui lui seraient faites.
15.	Un utilisateur devrait pouvoir supprimer des gens de sa liste d’amis.
16.	Recevoir une demande, la réception d’une réponse à une demande faite, ou se faire retirer de la liste d’amis de quelqu’un devrait envoyer une notification sur lequel l’application est installée (si l’application a le droit d’envoyer des notifications). Elle rajoute aussi dans tous les cas la notification au stockage interne à l’application.
17.	Un utilisateur devrait pouvoir mettre un poste comme favori.
18.	Un utilisateur devrait pouvoir filtrer pour ne voir que ses postes mis en favoris (ajout d’autres options de filtrage plus tard).
19.	Un utilisateur devrait pouvoir retirer un poste de ses favoris.
20.	Un utilisateur devrait pouvoir aller sur la page d’un de ces postes, et obtenir le poste détaillé, contenant toutes les informations du poste. Ceci pourrait inclure :
    1.	Un titre au poste
    2.	Une image reliée
    3.	Une plante reliée
    4.	Un message
    5.	Les commentaires et réponses au poste
21.	L’utilisateur devrait pouvoir commenter sur un poste, ou répondre à un commentaire, sous la forme de texte.
22.	L’utilisateur devrait pouvoir supprimer son commentaire ou sa réponse, laissant un message à la place semblable à « Message supprimé ».
23.	L’utilisateur recevra des notifications sur l’appareil sur lequel l’application est installée (si l’application a le droit d’envoyer des notifications) si/quand un autre utilisateur répond à un de ses commentaires/à une de ses réponses. Elle rajoute aussi dans tous les cas la notification au stockage interne à l’application.
24.	L’utilisateur devrait pouvoir ajouter un poste, contenant toutes ou seulement certaines des informations mentionnées ci-dessus (obligatoire : titre, message ; optionnel : plante reliée, image).
25.	L’utilisateur devrait recevoir des notifications sur l’appareil sur lequel l’application est installée (si l’application a le droit d’envoyer des notifications) si/quand un autre utilisateur commente sur le poste. Elle rajoute aussi dans tous les cas la notification au stockage interne à l’application.
26.	L’utilisateur devrait pouvoir supprimer son poste, supprimant toutes les informations, commentaires, réponses, images, etc. y étant relié.
27.	L’utilisateur devrait avoir une visualisation sur les notifications reçues dans l’application, permettant un accès rapide aux informations concernées. 

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
