# QVEMA - Plateforme de Financement de Projets

Une API RESTful construite avec NestJS et Fastify pour connecter entrepreneurs et investisseurs.

## Description

QVEMA est une plateforme qui permet aux entrepreneurs de présenter leurs projets et aux investisseurs de les financer. Le système inclut :
- Gestion des utilisateurs et authentification
- Gestion des projets
- Système d'investissement
- Recommandations basées sur les centres d'intérêt
- Interface d'administration

## Installation

```bash
$ npm install
```

## Configuration

Créez un fichier `.env` à la racine du projet avec les variables suivantes :

```env
DB_HOST=localhost
DB_PORT=3306
DB_USERNAME=votre_username
DB_PASSWORD=votre_password
DB_DATABASE=qvema
JWT_SECRET=votre_secret_tres_securise_ici
```

## Lancement de l'application

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Endpoints API

### Authentification
- `POST /api/auth/register` - Inscription
- `POST /api/auth/login` - Connexion

### Utilisateurs
- `GET /api/users/profile` - Voir son profil
- `PUT /api/users/profile` - Modifier son profil
- `POST /api/users/interests` - Associer des intérêts
- `GET /api/users/interests` - Voir ses intérêts

### Projets
- `POST /api/projects` - Créer un projet
- `GET /api/projects` - Liste des projets
- `GET /api/projects/:id` - Détails d'un projet
- `PUT /api/projects/:id` - Modifier un projet
- `DELETE /api/projects/:id` - Supprimer un projet
- `GET /api/projects/recommended` - Projets recommandés

### Investissements
- `POST /api/investments` - Investir dans un projet
- `GET /api/investments` - Voir ses investissements
- `GET /api/investments/project/:id` - Voir les investissements d'un projet
- `DELETE /api/investments/:id` - Annuler un investissement

### Administration
- `GET /api/admin/users` - Voir tous les utilisateurs
- `DELETE /api/admin/users/:id` - Supprimer un utilisateur
- `GET /api/admin/investments` - Voir toutes les transactions

## Rôles et Permissions

- **Entrepreneur** : Gestion de ses propres projets
- **Investisseur** : Investissements et gestion de portefeuille
- **Admin** : Supervision complète du système

## Sécurité

- Authentification JWT
- Contrôle des rôles
- Validation des données
- Gestion des erreurs

## Run tests

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```