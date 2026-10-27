# Prérequis

- Avoir Docker d'installé sur votre poste

## Lancer le projet

### 1 - Mettre en place les .env

Au niveau du dossier "back" ET au niveau du `docker-compose.yml`

Créer un fichier `.env`, faite un copier coller du `.env.exemple` qui se trouve au même niveau. Compléter les variables avec les valeurs approprié pour votre environnement local.

### 2 - Lancer le projet

Dans un terminal au niveau du `docker-compose.yml` lancer la commande :

`docker compose up -d`

### 3 - Créer les clef SSL

Générer les clefs SSL pour le JWT dans le back

`docker exec <NOM_DU_CONTENEUR_BACK> php bin/console lexik:jwt:generate-keypair`

## Les migrations

Pour mettre en place la base de donnée côté backend, lancer les migrations avec la commande :

`docker exec <NOM_DU_CONTENEUR_BACK> php bin/console doctrine:migrations:migrate`

Pour obtenir le nom du conteneur back vous pouvez lancer la commande :

`docker ps`
