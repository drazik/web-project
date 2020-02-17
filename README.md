# Projet tutoré

## Infos générales

### Contacts

Vous pouvez poser toutes vos questions sur le projet via message privé sur Slack ou sur le channel #projet-web.

### Date et modalités de rendu

Le rendu peut se faire en m'invitant en tant que collaborateur sur votre repository git si vous en avez un (conseillé, mais pas obligatoire), ou en m'envoyant votre code source (sans les dossiers `node_modules`) par mail.

La date de rendu est la même que celle de la soutenance. Celle-ci se tiendra le .../04/2019 (encore à déterminer).

Lors de la soutenance (environ 20 minutes), vous présenterez le résultat de votre travail, expliquerez la manière dont vous avez travaillé, quelles ont été les difficultés que vous avez rencontrées, comment vous les avez résolues ou contournées. L'objet principal de la soutenance n'est pas le code que vous aurez produit, même si vous pouvez en montrer si vous estimez que c'est nécessaire pour illustrer votre propos.

### Objectif

L'objectif de ce projet est d'évaluer votre capacités à développer une application web complète en utilisant les technologies et concepts de développement web client et serveur vus en cours.

## Cahier des charges

Vous travaillez pour une entreprise qui décide de créer une application web de gestion de _TODO List_. L'application doit permettre à une personne de créer un compte, puis de créer et gérer des listes de tâches à effectuer. L'application doit être développée en tant qu'application client riche communiquant avec une API.

Les fonctionnalités ont été découpées en deux parties :

* les fonctionnalités *core* : ce sont les fonctionnalités sans lesquelles l'application n'est pas considérée comme étant viable et ne pourra donc pas être déployée en production
* les fonctionnalités *secondaires* : ces fonctionnalités ne sont pas requises pour passer l'application en production. Elles pourront être développées plus tard, mais il sera tout de même très apprécié qu'elles soient présentes dès le premier jour

### Fonctionnalités *core*

#### Inscription

L'utilisateur doit pouvoir créer un nouveau compte sur l'application. Pour cela, il devra fournir son adresse e-mail ainsi qu'un mot de passe. Un formulaire d'inscription lui permettra de saisir ces informations. Le mot de passe de l'utilisateur devra être stocké en base de données de manière sécurisée. Les éventuelles erreurs (champ vide, e-mail déjà utilisé...) devront être affichées à l'utilisateur. Une fois l'utilisateur inscrit, un message de succès lui sera affiché, et un e-mail de confirmation contenant un lien lui permettant d'activer son compte lui sera envoyé sur l'adresse e-mail qu'il aura saisi.

Maquettes :

* [Desktop](https://www.figma.com/proto/LoLePFa8ZKBR4SZ8pLQz9B/Projet-iut?node-id=61%3A1&scaling=min-zoom)
* Mobile : à venir

#### Connexion

Une fois inscrit, l'utilisateur doit pouvoir se connecter sur son compte. Le formulaire de connexion est d'ailleurs la page sur laquelle un utilisateur non authentifié arrive par défaut lorsqu'il tente d'accéder à l'application.

Sur cette page, l'utilisateur peut saisir son adresse e-mail et son mot de passe pour se connecter à l'application. Un lien lui permet d'accéder à une page "mot de passe oublié" (voir fonctionnalités secondaires), et un autre lui permet d'accéder à la page d'inscription.

Maquettes :

* [Desktop](https://www.figma.com/proto/LoLePFa8ZKBR4SZ8pLQz9B/Projet-iut?node-id=53%3A1&scaling=min-zoom)
* Mobile : à venir

#### Page d'accueil

Une fois authentifié, l'utilisateur arrive automatiquement sur la page d'accueil. Sur cette page sont listées toutes les tâches (peu importe à quelle liste elles sont rattachées) qui ont une date d'échéance définie (plus de détails dans la description ci-dessous), par ordre croissant de date. Chaque tâche peut être définie comme terminée (en la cochant) ou éditée (en cliquant dessus) directement à partir de cette page.

Maquettes :

* [Desktop](https://www.figma.com/proto/LoLePFa8ZKBR4SZ8pLQz9B/Projet-iut?node-id=61%3A192&scaling=min-zoom)
* Mobile : à venir

#### Page d'édition d'une liste

Pour accéder à cette page, l'utilisateur doit cliquer sur une liste dans le menu.

Sur cette page, l'utilisateur peut ajouter, définir comme terminée, éditer ou supprimer des tâches dans une liste, ainsi que supprimer une liste.

Pour ajouter une tâche, l'utilisateur peut cliquer sur "Ajouter une tâche". Il peut alors saisir le nom de la nouvelle tâche et appuyer sur Entrée, ou cliquer sur le bouton "+". L'ajout d'une tâche remet automatiquement le focus sur le champ "Ajouter une tâche", de manière à ce que l'utilisateur puisse ajouter plusieurs tâches d'affilé facilement.

Pour définir une tâche comme terminée, l'utilisateur doit la cocher en cliquant sur la checkbox située à gauche de la ligne d'une tâche. L'utilisateur peut cocher et décocher la tâche à sa guise.

Pour éditer une tâche, l'utilisateur doit cliquer dessus. Un volet s'ouvre alors pour lui permettre de renseigner les différentes caractéristiques d'une tâche :

* Nom (ce qu'il a saisit lors de la création de la tâche)
* Liste d'étapes (voir fonctionnalités secondaires)
* Date d'échéance : une date à laquelle l'utilisateur estime que cette tâche doit avoir été effectuée
* Note : un champ de texte libre dans lequel l'utilisateur peut saisir des informations quelconques à propos de la tâche

Pour supprimer une tâche, l'utilisateur doit cliquer sur le picto "poubelle" situé sur la ligne d'une tâche. La suppression est immédiate, sans confirmation.

Pour supprimer la liste, l'utilisateur doit cliquer sur le bouton "Supprimer" situé à côté du nom de la liste. Une modale de confirmation doit s'afficher, et l'utilisateur peut alors cliquer sur "confirmer" ou "annuler". La confirmation supprime la liste et renvoie l'utilisateur sur la page d'accueil. L'annulation ferme simplement la modale.

Maquettes :

* [Desktop](https://www.figma.com/proto/LoLePFa8ZKBR4SZ8pLQz9B/Projet-iut?node-id=76%3A1&scaling=min-zoom)
* Mobile : à venir

#### Page paramètres

Sur cette page, l'utilisateur peut modifier ses informations : adresse e-mail et mot de passe.

Pour modifier son adresse e-mail, l'utilisateur doit saisir sa nouvelle adresse e-mail et la confirmer, puis cliquer sur "modifier l'adresse e-mail".

Pour modifier son mot de passe, l'utilisateur doit saisir son mot de passe actuel ainsi que le nouveau mot de passe et le confirmer, puis cliquer sur "modifier le mot de passe".

Lorsqu'une information a été modifiée avec succès, un message indiquera que le changement a été effectué. Les erreurs doivent être gérées et indiquées à l'utilisateur (adresse e-mail invalide, mauvais mot de passe actuel, nouveau mot de passe et confirmation qui ne correspondent pas...)

Maquettes :

* [Desktop](https://www.figma.com/proto/LoLePFa8ZKBR4SZ8pLQz9B/Projet-iut?node-id=77%3A582&scaling=min-zoom)
* Mobile : à venir

#### Menu

Sur chaque page, un menu est affiché (dans un volet à gauche de la page en desktop, via le click sur un bouton dans le header en mobile, voir maquettes de la page d'accueil). Dans ce menu, on trouve :

* Un lien permettant de revenir à la page d'accueil
* Une section "mes listes" dans laquelle se trouve l'ensemble des listes de l'utilisateur (le click sur une liste renvoie sur la page d'édition de cette liste). Pour chaque liste est aussi affiché le nombre de tâches qu'il reste à effectuer. Ainsi qu'un formulaire permettant de créer une nouvelle liste (en saisissant son nom). La création d'une nouvelle liste envoie automatiquement sur la page d'édition de cette liste
* Un lien "paramètres" qui renvoie vers la page paramètres
* Un lien "déconnexion" qui déconnecte l'utilisateur et le renvoie sur le formulaire de connexion

### Fonctionnalités secondaires

#### Page "mot de passe oublié"

Lorsque l'utilisateur est sur le formulaire de connexion mais a oublié son mot de passe, il peut cliquer sur un lien "j'ai oublié mon mot de passe". Il arrive alors sur une page qui lui demande son adresse e-mail. Une fois son adresse e-mail saisie, un e-mail lui est envoyé avec un lien lui permettant d'accéder à une page sur laquelle il pourra définir un nouveau mot de passe.

Maquettes :

* [Desktop](https://www.figma.com/proto/LoLePFa8ZKBR4SZ8pLQz9B/Projet-iut?node-id=54%3A101&scaling=min-zoom)
* Mobile : à venir

#### Etapes d'une tâche

L'utilisateur peut définir une liste d'étapes pour chaque tâche. Une étape est en quelques sortes une sous-tâche. L'utilisateur peut ajouter le nombre d'étapes qu'il veut pour chaque tâche, les cocher, les supprimer (sans confirmation).

## Technologies, architecture à utiliser

L'application sera pour le moment disponible uniquement en version web, mais des applications mobiles pourraient être developpées par la suite. Dans ce cadre, la partie serveur doit être développée sous forme d'une API, que la partie client utilisera.

Vous êtes libres d'utiliser les outils et frameworks que vous voulez (ou de ne pas en utiliser). Vos choix pourront être challengés lors de la soutenance.
