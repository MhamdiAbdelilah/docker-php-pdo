# README

## Utilisation de Docker Compose pour l'environnement PHP/MySQL

Ce fichier `docker-compose.yml` est utilisé pour créer un environnement de développement PHP avec MySQL et phpMyAdmin.

### Services Définis:

- **db**: Le service de base de données MySQL.
- **phpmyadmin**: Une interface web pour gérer la base de données MySQL.
- **webserver**: Un serveur web Apache servant les fichiers PHP.

### Démarrage des services:

Pour démarrer tous les services définis dans ce fichier, exécutez la commande suivante dans votre terminal :

```bash
docker-compose up -d
```
Cela va télécharger les images nécessaires et démarrer les conteneurs en arrière-plan.

### Emplacement des fichiers PHP:
Les fichiers PHP doivent être sauvegardés dans le dossier ./php  ce dossier sera synchronisé avec le dossier /var/www/html à l’intérieur du conteneur du serveur web.

### Volumes des autres conteneurs:
Pour persister les données et configurer d’autres aspects des services, vous pouvez utiliser des volumes comme indiqué sous chaque service. Par exemple, pour MySQL (db), un volume est mappé à /var/lib/mysql.

Assurez-vous que vos chemins locaux correspondent aux chemins attendus par les conteneurs et que vous avez les permissions nécessaires pour y écrire.

### Arrêt des services:
Pour arrêter tous les services en cours d’exécution liés à ce fichier compose, utilisez :
```bash
docker-compose down
```

Cela arrêtera et supprimera tous les conteneurs associés aux services définis.
