# Application Web de Messagerie

Ce projet est une application web de messagerie qui permet aux utilisateurs de communiquer entre eux via des messages texte. L'application est construite avec Node.js et Express.js pour le backend, et utilise une base de données relationnelle (probablement PostgreSQL, vu la présence de Sequelize) pour stocker les informations.

## Fonctionnalités

* **Envoi et réception de messages**: Les utilisateurs peuvent envoyer et recevoir des messages texte.
* **Groupes de discussion**: Les messages sont organisés en groupes, permettant à plusieurs utilisateurs de participer à une conversation.
* **Gestion des utilisateurs**: L'application gère l'authentification et l'autorisation des utilisateurs (voir `auth.middleware.js` dans le référentiel).
* **API REST**: L'application expose une API REST pour l'interaction avec le frontend.

## Technologies utilisées

* **Node.js**: Environnement d'exécution JavaScript côté serveur.
* **Express.js**: Framework web Node.js minimaliste et flexible.
* **Sequelize**: ORM (Object-Relational Mapper) pour Node.js, utilisé pour interagir avec la base de données.
* **PostgreSQL**: Système de gestion de base de données relationnelle (probablement utilisé, vu la présence de Sequelize).
* **Helmet**: Collection de middlewares Express pour améliorer la sécurité de l'application.
* **Swagger**:  Générateur de documentation d'API pour faciliter la compréhension et l'utilisation de l'API.

## Structure du projet

Le projet est structuré de manière modulaire, avec différents fichiers et dossiers pour organiser le code :

* **`app.js`**: Fichier principal de l'application, contenant la configuration et le lancement du serveur Express.
* **`messages.js`**: Définit le modèle Sequelize pour les messages.
* **`users.js`, `groups.js`**:  (présents dans le référentiel) Définissent probablement les modèles Sequelize pour les utilisateurs et les groupes.
* **`routes/`**: Contient les définitions des routes de l'API.
* **`middlewares/`**: Contient les middlewares utilisés pour la gestion des erreurs, l'authentification, etc.
* **`util/`**: Contient les utilitaires tels que le logger.

## Installation et exécution

1. **Cloner le référentiel**: `git clone https://github.com/Bergerghislain/Application-Web-Messageries.git`
2. **Installer les dépendances**: `npm install`
3. **Configurer la base de données**: Créer une base de données PostgreSQL et configurer les informations de connexion dans le fichier de configuration.
4. **Lancer l'application**: `npm start`

## Documentation de l'API

La documentation de l'API est générée avec Swagger et est accessible à l'adresse `/doc` après le lancement de l'application.

## Points importants

* **Gestion des erreurs**: L'application utilise un middleware personnalisé pour gérer les erreurs et fournir des réponses cohérentes.
* **Sécurité**: L'application utilise Helmet pour améliorer la sécurité en définissant divers en-têtes HTTP.
* **Analyse des requêtes**: Express.js est utilisé pour analyser les requêtes JSON et URL codées.
* **En-têtes de réponse**:  L'application définit l'en-tête `Content-Type` sur `application/json` pour toutes les réponses.
* **Routage**: Un routeur séparé est utilisé pour organiser les routes de l'API.

## Contribution

Les contributions sont les bienvenues. Veuillez consulter le fichier CONTRIBUTING.md dans le référentiel pour plus d'informations.

