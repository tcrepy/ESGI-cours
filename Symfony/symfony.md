# Symfony 4

[Symfony 4.1 Documentation](https://symfony.com/doc/current/index.html)

**CRUD** : Create Reade Update Delete

## Historique
--- 
> 2 milliard de téléchargements

> 13 ans déjà (18 octobre 2005

## Idéologie
--- 
- Framework php
- Communauté très forte
- Documentation très complète
- Best practice (Données par le framework et par PSR

## Concept
--- 
- Système de commande
- Composer : utilisé pour récupéré les bundle
- Flex : Automatisation de l'installation des bundle avec ses configurations
- Profiler : débugger avancé en mode dev

## Requête type
---
1. http request (exemple : http://mon-site.fr/article/show/7)
2. Controller frontal  (envoi au kernel et checkup de secu)
3. Kernel (noyau)
4. Routing : décomposition de l'uri (url sans nom de domaine). 
   1ère partie : quel controller -> _articles_
   2ème partie : méthode -> _show_
   3ème partie : Paramètres -> _7_
5. Controller
5.1. Model doctrine qui récupère les donénes dans la bdd
5.2. View qui renvoi tout ça

## Composer & Symfony 
___

L'ensemble des bundles :
[composer/symfony - Packagist](https://packagist.org/packages/symfony/symfony)

- Avoir symfony sans rien : **skeleton**
- Avoir symfony avec des lib front : **skeleton webapp**

Le composer.json est utilisé pour configuré l'ensemble d'un projet symfony. Il va récupéré l'ensemble des packages, recipes ou bundle inscrit dessus.

## Flex
---
Flex utilisé des **recettes** (recipes) pour installer/utiliser les bundles symfony
exemple : recipes/symfony/framework-bundle/3.3
utilisation : composer require symfony/console

Un **package** est utilisé par felx pour installer un regroupement de recettes
exemple : orm-pack
utilisation : composer require orm-pack

Il y en a des officiels, validées par symfony et contribs, créées par la communauté symfony.

L'ensemble des recettes :
[Symfony Recipes Server](https://symfony.sh/)

## Utilisation
---

.env : utiliser pour les indentifiants de base de données etc
.env.dist : env distributé, donc versionné avec des fausses données

### Routing
Il est basé sur de la regex (expression régulière)

### Entitée

= 1 table

### Repository

permet de faire des requêtes

## Docker et Symfony : 

Ajout du docker-compose.yml à la racine : 
```yml
version: '3.2'

services:
    db:
        image: postgres:9.6-alpine
        environment:
            - POSTGRES_DB=iw43-symfony
            - POSTGRES_USER=api-platform
            - POSTGRES_PASSWORD=lmdpe
        ports:
            - "5432:5432"

volumes:
    db-data: {}
```

ensuite modifier le fichier `app/config/packages/doctrine.yml`

```yml
doctrine:
    dbal:
        # configure these for your database server
        driver: 'pdo_pgsql'
        server_version: '5.7'
        charset: utf8
        default_table_options:
            charset: utf8
            collate: utf8mb4_unicode_ci
```

et changer le .env
```
###> doctrine/doctrine-bundle ###
DATABASE_URL=pgsql://api-platform:lmdpe@<container_id>:5432/iw43-symfony
```

 on lance la commande : 
```
    docker-compose up -d`
```

pour avoir l'id du container : 

```
    docker inspect <container_id> | grep "IPAddress"
```
ou
```
    `docker-machine ip default`
```

On doit avoir ce message : 
```
Status: Downloaded newer image for postgres:9.6-alpine
Creating 4aiw3-symfony_db_1 ... done
```


## Commandes 

- Créer la bdd : 
```
php bin/console d:d:c
```
- Afficher la requête sql de l'update du schema de la bdd : `$ 
```
php bin/console doctrine:schema:update --dump-sql
```
- Update le schema de la bdd :  
```
php bin/console doctrine:schema:update --force
```



## AUTO-autowiring
Le fait de passer en paramètre un service symfony

## Param convertor
passer une variable dans le paramètree d'une méthode et le transformer en objet

## persist
permet de mettre en cache l'ensemble des modifications des entity (uniquement sur du create et pas sur du update)

## Flush
modifie la bdd selon les persist

## Twig

`~` : concaténation twig
