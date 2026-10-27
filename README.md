# Prérequis

- Avoir Docker d'installé sur votre poste

## Lancer le projet

### 1 - Mettre en place les .env

Au niveau du dossier "back" ET au niveau du `docker-compose.yml`

Créer un fichier `.env`, faite un copier coller du `.env.exemple` qui se trouve au même niveau. Compléter les variables avec les valeurs approprié pour votre environnement local.

### 2 - Lancer le projet

Dans un terminal au niveau du `docker-compose.yml` lancer la commande :

`docker compose up -d`

## Les migrations

Pour mettre en place la base de donnée côté backend, lancer les migrations avec la commande :

`docker exec <NOM_DU_CONTENEUR> php bin/console doctrine:migrations:migrate`

Pour obtenir le nom du conteneur back vous pouvez lancer la commande :

`docker ps`
