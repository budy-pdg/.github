# Architecture

L'architecture est décomposée en plusieurs parties.

## Backend

![Architecture Backend](./images/budy-archi.drawio.png)

Ici nous avons la partie Backend. Le GitHub reçoit les changements qui seront analysés par GitHub actions, qui vérifie donc que nous sommes conformes à nos requirements, et que nos tests passent.

Nous avons ensuite 2 environnements Render qui ont chacune une instance de base de donnée PostgreSQL provenant de l'application Neon. C'est cet environnement Render qui sert de serveur, et qui contient notre landing page. C'est aussi Render qui s'occupe directement d'aller faire le déploiement continu. Il surveille une branche et quand un changement qui passe les tests est fait, il applique le changement.

De la sorte, la partie GitHub est déjà séparée entre la partie **main** et **dev** (les branches), qui correspondent respectivement à la partie *production* et *développement* de Render et Neon.

## Frontend

FIXME avec l'image

Ici nous avons la partie Frontend, l'application. La structure est similaire à celle de la Backend. GitHub reçoit les changements, toujours analysés par les GitHub actions (on fait les tests ici).

FIXME avec le reste de la procédure de déploiement
