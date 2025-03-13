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

## Deployment

When you're ready to deploy your NestJS application to production, there are some key steps you can take to ensure it runs as efficiently as possible. Check out the [deployment documentation](https://docs.nestjs.com/deployment) for more information.

If you are looking for a cloud-based platform to deploy your NestJS application, check out [Mau](https://mau.nestjs.com), our official platform for deploying NestJS applications on AWS. Mau makes deployment straightforward and fast, requiring just a few simple steps:

```bash
$ npm install -g mau
$ mau deploy
```

With Mau, you can deploy your application in just a few clicks, allowing you to focus on building features rather than managing infrastructure.

## Resources

Check out a few resources that may come in handy when working with NestJS:

- Visit the [NestJS Documentation](https://docs.nestjs.com) to learn more about the framework.
- For questions and support, please visit our [Discord channel](https://discord.gg/G7Qnnhy).
- To dive deeper and get more hands-on experience, check out our official video [courses](https://courses.nestjs.com/).
- Deploy your application to AWS with the help of [NestJS Mau](https://mau.nestjs.com) in just a few clicks.
- Visualize your application graph and interact with the NestJS application in real-time using [NestJS Devtools](https://devtools.nestjs.com).
- Need help with your project (part-time to full-time)? Check out our official [enterprise support](https://enterprise.nestjs.com).
- To stay in the loop and get updates, follow us on [X](https://x.com/nestframework) and [LinkedIn](https://linkedin.com/company/nestjs).
- Looking for a job, or have a job to offer? Check out our official [Jobs board](https://jobs.nestjs.com).

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://twitter.com/kammysliwiec)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](https://github.com/nestjs/nest/blob/master/LICENSE).
#   q v e m a  
 