```bash
docker compose down --volumes --rmi all --remove-orphans
docker rm -f $(docker ps -a -q)

# pour voir la configuration de l'orchestration des conteneurs
docker compose config

# nom de l'image postgres_db 
docker ps
# accès au variable d'env dans le fichier docker compose
docker exec postgres_db env

# se connecter à la base de données depuis le terminale
docker-compose exec db psql -U user -d db -W

# connection au container 
docker exec -it php-apache /bin/bash

# build une image 
docker build . 

docker tag d92eaef2b929c antoine/php8.4-apache

docker run -d -p 8741:80 --name my-php-apache-container my-php-apache-image

# configuration git 
git config --global user.name "Alan"
git config --global user.email "alan.alan@alan.fr"

# api platform
# alan@alan.fr
# password
$2y$13$tmaPG8t9Xm6IvlT8zk.DXeLcA9A0hgfB2yFgE/dioEKeruEWQAuDG 

a2enmod headers

# création du fichier htaccess
omposer require symfony/apache-pack

# si init 
docker compose run init 

# refresh token
composer require doctrine/orm doctrine/doctrine-bundle gesdinet/jwt-refresh-token-bundle

# sans la partie build pour l'instant
docker compose up --no-build -d

# en mode développement
docker-compose -f docker-compose.yml up -d --build

# en mode production 
docker-compose -f docker-compose.dev.yml up -d --build
```

- ingress
En Docker et Kubernetes, un Ingress est un composant qui gère l'accès aux services depuis l'extérieur du cluster. 

L'Ingress est un type de réseau virtuel utilisé pour :

Routage du trafic externe : Il permet d'exposer un service Docker sur un port spécifique et de router le trafic vers les conteneurs appropriés.
Load Balancing (Répartition de charge) : Il répartit automatiquement le trafic entrant entre toutes les instances d'un service (réplication de conteneurs).
Accès aux services depuis l'extérieur : Il facilite l'accès aux services depuis l'extérieur du cluster Swarm, même si les conteneurs sont répartis sur plusieurs nœuds.
