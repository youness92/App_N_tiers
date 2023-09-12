
---

# Mon Application N-tiers

## Présentation

Cette application est un exemple d'architecture N-tiers comprenant un frontend statique servi via Nginx et un backend Spring Boot. L'application est conçue pour être déployée en utilisant Docker et Docker Compose.

### Structure du projet

```
.
├── LICENSE
├── README.md
├── backend
│   ├── Dockerfile
│   ├── pom.xml
│   └── src
│       └── main
│           ├── java
│           │   └── fr
│           │       └── ntiers
│           │           └── app
│           │               ├── App.java
│           │               └── HelloWorldController.java
│           └── resources
│               └── application.properties
├── docker-compose.yml
└── frontend
    ├── Dockerfile
    └── nginx.conf
```

## Fonctionnalités

- **Frontend**: Une page web statique basique hébergée par un serveur Nginx.
- **Backend**: Une API REST simple construite avec Spring Boot, déployée dans un conteneur Docker et connectée à une base de données PostgreSQL.

## Comment démarrer?

1. Assurez-vous d'avoir installé Docker et Docker Compose.
2. Clonez ce dépôt:

   ```
   git clone <URL_DU_REPO>
   cd <NOM_DU_DOSSIER>
   ```

3. Construisez et démarrez les conteneurs:

   ```
   docker-compose build
   docker-compose up
   ```

4. Accédez à l'application:

   - Frontend: `http://localhost`
   - Backend: `http://localhost:8080` ou `http://localhost/api`

---