# Documentation du Projet TP Docker

Ce document détaille les étapes que j'ai suivies pour réaliser le TP Docker, qui implique le développement d'une application de gestion d'utilisateurs avec une architecture microservices utilisant Docker.

## Construction des Images Docker

### Service BFF

Pour construire l'image Docker pour le service BFF, j'ai exécuté la commande suivante :

```bash
docker build -t anabrnrd/tp_docker_ab_bff_v3:latest ./bff
```

### Frontend

Pour construire l'image Docker pour le frontend, j'ai utilisé la commande suivante :

```bash
docker build -t anabrnrd/tp_docker_ab_front_v2:latest ./front
```

## Publication des Images sur Docker Hub

Pour publier les images sur Docker Hub, j'ai d'abord tagué les images avec les noms appropriés, puis je les ai poussées sur Docker Hub à l'aide des commandes suivantes :

```bash
docker tag tp_docker_ab_bff_v3:latest anabrnrd/tp_docker_ab_bff_v3:latest
docker push anabrnrd/tp_docker_ab_bff_v3:latest

docker tag tp_docker_ab_front_v2:latest anabrnrd/tp_docker_ab_front_v2:latest
docker push anabrnrd/tp_docker_ab_front_v2:latest
```

## Utilisation du Docker Compose

J'ai utilisé Docker Compose pour orchestrer mes services. Le fichier .env contient les identifiants de la base de données.

Pour démarrer les services, j'ai exécuté la commande suivante :

```bash
docker-compose up -d
```

Pour arrêter les services, j'ai utilisé la commande suivante :

```bash
docker-compose down
```

## Informations Supplémentaires

- L'application Frontend est publiée sur Docker Hub sous le nom :
```bash
anabrnrd/tp_docker_ab_front_v2:latest.
```
- Le service BFF est publié sur Docker Hub sous le nom :
```bash
anabrnrd/tp_docker_ab_bff_v3:latest.
```
https://hub.docker.com/repository/docker/anabrnrd/tp_docker_ab

### Accès à phpMyAdmin
http://localhost:8081/
![homepage phpMyAdmin](https://github.com/AnBrnd/TP_DOCKER/assets/137530989/60fef3e4-77f7-4c5c-900a-c4f5c2ae8359)

### Accès au Front
http://localhost:80/
![homepage front](https://github.com/AnBrnd/TP_DOCKER/assets/137530989/b3aec2d1-3990-45b3-9569-49af8852eed8)

### Fichier .env
![fichier .env](https://github.com/AnBrnd/TP_DOCKER/assets/137530989/304df27c-72e2-4474-b59c-4f4ecad0ea66)

