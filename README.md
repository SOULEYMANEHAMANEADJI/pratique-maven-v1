Ce projet est organisé en modules Maven et se divise en trois parties distinctes selon les différentes configurations :

## 1. Modules Maven avec Spring Boot

### Description
Ce module met en place un projet parent Spring Boot appelé `commandes`, qui contient les modules suivants :
- **services** : Gestion de la logique métier de l'application.
- **web** : Gestion des contrôleurs API Rest.
- **start** : Projet de démarrage de l'application.

### Structure du projet
```
commandes (parent)
├── services
├── web
└── start
```

### Technologies
- Spring Boot
- Maven

### Installation
Pour installer le projet, clonez le dépôt et exécutez la commande suivante :
```bash
mvn clean install
```

### Lancer l'application
À partir du module `start`, exécutez :
```bash
mvn spring-boot:run
```

### Tutoriel
Vous pouvez suivre cette [série de vidéos](https://www.youtube.com/watch?v=l6G8KKYiZxA&list=PLzT281RbfHAYHJ-pIULFeDvMIRxdPwrGt&index=1) pour compléter le projet.

---

## 2. Modules Maven avec les applications web

### Description
Dans ce module, le projet parent `commandes` est un projet Maven simple. Il contient les modules :
- **services** : Gère le métier de l'application.
- **web** : Application Tomcat contenant les services web.
- **batch** : Projet Spring Boot pour le traitement par lot.

### Structure du projet
```
commandes (parent)
├── services
├── web
└── batch
```

### Technologies
- Spring Boot
- Maven
- Tomcat

### Installation
Clonez le dépôt et exécutez :
```bash
mvn clean install
```

### Lancer l'application
Pour démarrer l'application web depuis le module `web`, utilisez :
```bash
mvn tomcat7:run
```

Et pour le module `batch` :
```bash
mvn spring-boot:run
```

---

## 3. Modules Maven avec gestion des plugins

### Description
Ce module se concentre sur la création du projet parent `commandes`, qui est également un projet Maven simple. Il inclut les modules :
- **services** : Gère la logique métier de l'application.
- **web** : Application Angular.

### Structure du projet
```
commandes (parent)
├── services
└── web
```

### Technologies
- Maven
- Angular

### Installation
Clonez le dépôt et exécutez :
```bash
mvn clean install
```

### Démarrer l'application
Accédez au dossier `web` et exécutez Angular :
```bash
npm install
ng serve
```

---

## Contribuer
Si vous souhaitez contribuer à ce projet, n'hésitez pas à ouvrir une issue ou à soumettre une pull request !
