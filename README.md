Lancer le projet : 
docker compose up -d


Lancer les migration côté back : 
docker exec test-auth-php-1 php bin/console doctrine:migrations:migrate
