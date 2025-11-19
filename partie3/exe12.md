# symfony-7-2025

## Menu

- [Retour à la partie 3](README.md)
- [Vue d'ensemble des entités et relations](db11.md)

## Exercice 12 : Création du template d'accueil et de la route associée

Dans cet exercice, nous allons créer, depuis un template Twig, la page d'accueil de notre application de blog Symfony. Nous allons également définir la route associée dans un contrôleur. Nous continuerons le projet commencé dans les exercices précédents: `blog_symfony_{TON PRENOM}`


### Étapes à suivre :

1. **Créez une branche git** nommée `exe12` depuis la branche `exe11` (après validation de la branche `exe11`) pour cet exercice.

   ```bash
   git checkout -b exe12
   ```
   
2. **En cas de présence du contrôleur précédent** :

Nous allons le supprimer (ainsi que ses dépendances) pour repartir d'une base propre.

```bash
rm src/Controller/HomeController.php
rm templates/home/index.html.twig
# si on avait un test
rm tests/Controller/HomeControllerTest.php
```

3. **Créez le contrôleur BlogController** :

Utilisez la commande `make:controller` pour générer un nouveau contrôleur nommé `BlogController` avec une vue associée.

```bash
php bin/console make:controller BlogController
```

Mettez 'yes' pour la génération du fichier de test.

Vous devriez obtenir un **Success!** à la fin de la commande.

Cela créera trois fichiers :

```bash
created: src/Controller/BlogController.php
created: templates/blog/index.html.twig
created: tests/Controller/BlogControllerTest.php
```
4. **Modifiez le contrôleur BlogController** :
```php
# src/Controller/BlogController.php
# ...
final class BlogController extends AbstractController
{
    #[Route('/', name: 'homepage')]
    public function index(): Response
    {
        return $this->render('blog/index.html.twig', [
            'controller_name' => 'BlogController',
        ]);
    }
}
```

Vous devriez retourner à la page de base telle que l'image ci-dessous lorsque vous accédez à la racine de votre application Symfony (http://localhost:8000/).

![front homepage](https://raw.githubusercontent.com/WebDevCF2m2025/symfony-7-2025/refs/heads/main/exercices/exe12debut.png)