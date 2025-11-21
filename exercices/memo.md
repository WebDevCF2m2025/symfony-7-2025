## Symfony - Memo

Ce mémo regroupe les commandes et concepts essentiels pour travailler avec Symfony.

## Menu
- [Retour à la partie 1](../README.md)
- [Retour à la partie 2](../partie2/README.md)
- [Retour à la partie 3](../partie3/README.md)
- [Les commandes maker les plus courantes](#les-commandes-maker-les-plus-courantes)
- [Les testes unitaires avec PHPUnit](#les-testes-unitaires-avec-phpunit)
- [PHP CS Fixer](#php-cs-fixer)
- [Doctrine - Commandes courantes](#doctrine---commandes-courantes)
- [Autres commandes utiles](#autres-commandes-utiles)

#### Les commandes maker les plus courantes

##### Créer une entité Doctrine (PHP 8 attributes)
```bash
php bin/console make:entity
```

##### Créer un contrôleur Web ou API
```bash
php bin/console make:controller
```

##### Créer un formulaire lié à une entité
```bash
php bin/console make:form
```

##### Créer un formulaire lié à une entité
```bash
php bin/console make:form
```

##### Créer un CRUD pour une entité
```bash
php bin/console make:crud
```

##### Créer un contrôleur Stimulus
```bash
php bin/console make:stimulus-controller
```

##### Créer une migration à partir des modifications d'entités
```bash
php bin/console make:migration
```

##### Exécuter les migrations
```bash
php bin/console doctrine:migrations:migrate
```
##### Créer un utilisateur avec le système de sécurité
```bash
php bin/console make:user
```
##### Créer un système d'authentification (login form)
```bash
php bin/console make:security:form-login
```

[Retour au menu](#menu)

#### Les testes unitaires avec PHPUnit
##### Créer un test unitaire pour une classe ou un contrôleur
```bash
php bin/console make:test
```
##### Exécuter les tests unitaires
```bash
php bin/phpunit
```

[Retour au menu](#menu)

#### PHP CS Fixer
##### Installer PHP CS Fixer
```bash
composer require --dev friendsofphp/php-cs-fixer
```
##### Exécuter PHP CS Fixer pour formater le code
```bash
./vendor/bin/php-cs-fixer fix
```

[Retour au menu](#menu)

#### Doctrine - Commandes courantes
##### Créer la base de données
```bash
php bin/console doctrine:database:create
``` 
##### Mettre à jour le schéma de la base de données (non recommandé en production)
```bash
php bin/console doctrine:schema:update --force
```
##### Générer les getters et setters pour les entités
```bash
php bin/console make:entity --regenerate
``` 

[Retour au menu](#menu)


#### Autres commandes utiles
##### Lancer le serveur de développement Symfony
```bash
symfony server:start
```
##### Arrêter le serveur de développement Symfony
```bash
symfony server:stop
```
##### Afficher les routes définies dans l'application
```bash
php bin/console debug:router
```
##### Afficher les entités Doctrine
```bash
php bin/console doctrine:mapping:info
```
##### Afficher les informations sur la base de données
```bash
php bin/console doctrine:database:info
```
##### Vider le cache de l'application
```bash
php bin/console cache:clear
``` 
##### Afficher les services enregistrés dans l'application
```bash
php bin/console debug:container
```
##### Afficher les paramètres de configuration
```bash
php bin/console debug:config
``` 

[Retour au menu](#menu)