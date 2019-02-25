# Projet web
Informations complètes du projet de programmation web

Questions :
* email à Cyrille / Alexandre / Aymeric, ou #web-project sur Slack
* [ouvrir une issue](https://github.com/drazik/web-project/issues/new)

## Objectif
Évaluer les capacités à développer une application web avec toutes les technologies front
et back (client et serveur) qui ont été vues en cours.

## Cahier des charges
Créer une app de type _TODO List_ avec une gestion de tâches et des utilisteurs.

### Maquette d'interface possible

Donnée à titre d'exemple et pour inspiration seulement. Vous pouvez faire quelque chose
de très ressemblant ou très éloigné.

![Mockup TODOList app](mockup_projet.png)

### Fonctionnalitées demandées

#### Client
- Pré-requis technique
  - Le client doit être une app JS frontend qui tourne dans le navigateur
  - Le client doit être fonctionnel sur les principaux navigateurs récents du marché
  (Firefox, Chrome, Edge)
- Fonctionnalités minimales
  - Créer un compte utilisateur (email, nom d'utilisateur, mot de passe, date de naissance, photo)
  - Envoyer un email lors de la création du compte
  - Connexion et déconnexion à l'app
  - Modifier son profil
  - Créer, modifier et supprimer des listes
  - Créer, modifier et supprimer des tâches
  - Changer le statut d'une tâche (todo / completée)
- Fonctionnalités bonus
  - Créer et supprimer des sous-tâches
  - Définir la progression (%) d'une tâche principale en fonction de ses sous-tâches
  - Inviter des utilisateurs à collaborer sur une liste

#### Serveur
- Créer un serveur d'API avec toutes les routes et fonctionnalités qu'il est nécessaire
d'exposer
- Permettre l'authentification des clients
- Utiliser au minimum Node et PostgreSQL

Bonus
- Authentification par token (Oauth 2, auth0, JWT)
- HTTPS avec Cloudflare

### Technologies utilisées
- Pour le développement, vous pouvez utiliser n'importe quelles solutions techniques (en
tenant compte des pré-requis ci-dessus). Le choix et la justification des outils
utilisés seront cependant pris en compte :eyes:
- Gestion des sources : [Git](https://git-scm.com/) (cf. section [livrables](#livrables))

## Critères d'évaluation
- Pertinence des **choix techniques**
- Attention particulière portée à la **qualité du code** : HTML, CSS, JS
- Développement de composants d'interface réutilisables
- Sécurité des données, de l'application et de l'authentification
- Documentation
- Utilisation de git : organisation du repository et des branches, utilisations de PR/MR,
fréquence et cohérence des commits
- Répartition du travail dans l'équipe
- Clarté et qualité de la présentation du projet (générale, fonctionnelle et technique)

## Livrables
- Projet à envoyer par email au plus tard le **10 avril 2019 à 23h59**.
- Le projet doit être hébergé sur un repository **privé** en ligne, comme [GitLab](https://about.gitlab.com/) ou [Bitbucket](https://bitbucket.org/) (gratuits tous les 2). Il est également possible d'utiliser GitHub gratuitement avec le [student developer pack](https://education.github.com/pack)
- Invitez les 3 enseignants comme _reporters_ ou _contributeurs_ de votre projet
- Pensez à inclure au minimum un `README.md` pour expliquer comment est organisé le projet et les étapes basiques permettant de le faire fonctionner
- Soutenance (**11 avril 2019** à partir de 14h) :
  - Présentation du projet, des choix techniques et de son déroulement (5 minutes)
  - Démo du résultat (15 minutes)
  - Questions/réponses (5-10 minutes)

## Bonus (optionels mais appréciés !)
- Qualité de l'UI (interfaces) et de l'UX (ergonomie)
- Faire une démo avec les clients et le serveur sur 2 machines différentes
- Tests unitaires
- Déploiement en ligne : [Now](https://zeit.co/now), [Heroku](https://devcenter.heroku.com), DigitalOcean
- Utilisation d'un framework ou d'une librairie front-end
