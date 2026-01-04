# Pipeline CI/CD avec Jenkins, GitHub, Docker et ngrok

## Description

Ce projet est une application Spring Boot simple qui sert de démonstration pour un pipeline CI/CD complet utilisant Jenkins, GitHub, Docker et ngrok.

## Résultats du TP

Ce projet de travaux pratiques (TP) permet de mettre en place et de comprendre :

1. **Intégration Continue (CI)** : Configuration d'un pipeline Jenkins pour automatiser les builds et les tests à chaque commit GitHub
2. **Déploiement Continu (CD)** : Automatisation du déploiement de l'application via Docker
3. **Containerisation** : Dockerisation de l'application Spring Boot pour un déploiement standardisé
4. **Exposition locale** : Utilisation de ngrok pour exposer l'application déployée localement via un tunnel sécurisé
5. **Webhooks GitHub** : Configuration des webhooks GitHub pour déclencher automatiquement les pipelines Jenkins

## Technologies utilisées

- **Spring Boot 3.2.1** : Framework Java pour le développement de l'application
- **Maven** : Gestionnaire de dépendances et outil de build
- **Docker** : Containerisation de l'application
- **Jenkins** : Serveur d'intégration continue
- **ngrok** : Tunnel sécurisé pour exposer l'application localement
- **GitHub** : Hébergement du code source et gestion des webhooks

## Endpoints de l'application

L'application expose les endpoints REST suivants sur le port **8282** :

- `GET /` : Retourne "hello , testing webhooks , jenkins"
- `GET /user` : Retourne "Users"
- `GET /presentation` : Retourne "presentation"

## Prérequis

- Java 17
- Maven 3.x
- Docker
- Jenkins (si déploiement local)

## Build et exécution

### Build avec Maven
```bash
mvn clean package
```

### Exécution locale
```bash
mvn spring-boot:run
```

### Build et exécution avec Docker
```bash
docker build -t point-of-sale:latest .
docker run -p 8282:8282 point-of-sale:latest
```

L'application sera accessible sur `http://localhost:8282`

