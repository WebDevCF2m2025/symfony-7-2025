# symfony-7-2025

## Menu

- [Retour à la partie 3](README.md)
- [Vue d'ensemble des entités et relations](db11.md)

## Exercice 16 : Création des slugs à la volée

Nous continuerons le projet commencé dans les exercices précédents: `blog_symfony_{TON PRENOM}`.

### Étapes à suivre :

1. **Créez une branche git** nommée `exe16` depuis la branche `exe15` (après validation de la branche `exe15`) pour cet exercice. **N'oubliez pas de faire des commits régulièrement après chaque étape importante !**

   ```bash
   git checkout -b exe16
   ```

# PROBLEME ICI

2. **Installer la bibliothèque Slugify** :
    Nous allons utiliser la bibliothèque `cocur/slugify` pour générer des slugs à partir des titres des articles et des catégories.
    
    Exécutez la commande suivante pour installer la bibliothèque via Composer :
    
    ```bash
    composer require cocur/slugify
    ```
3. **Modifier les entités Article et Category** :

    Ouvrez les fichiers `src/Entity/Article.php` et `src/Entity/Category.php` et ajoutez une méthode pour générer le slug à partir du titre avant de persister ou de mettre à jour l'entité.
    
    Exemple pour l'entité Article :
    
    ```php
    // src/Entity/Article.php
    // ...
    use Cocur\Slugify\Slugify;
    
    class Article
    {
         // ...
    
         public function generateSlug(): void
         {
              $slugify = new Slugify();
              $this->slug = $slugify->slugify($this->title);
         }
    
         // ...
    }
    ```
    
    Faites de même pour l'entité Category.
   




**Envoyez-moi le lien vers votre repository github** avec la branche `exe16` finie à `gitweb@cf2m.be` dans `Teams`.

   

[Retour au menu de la partie 3](README.md)
ou

[Exercice 17 : Affichage dans l'accueil](exe17.md)