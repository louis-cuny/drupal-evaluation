# Drupal evaluation

Ce projet est l'objet d'une évaluation technique.

## Objectifs

Consulter la liste de produits avec une pagination de 5 produits par page
Ajouter de nouveaux produits
Modifier chaque champs du produit
Supprimer chaque ligne de produit
Trier les produits par prodRef, prodName, prodCity, prodPrice par ordre croissant et décroissant
Filtrer la liste par prodRef et prodName
Filtrer la liste par une fourchette de prodPrice
Filtrer la liste par une ou plusieurs prodCity


## Installation

### Option 1 - Ddev

Cette option consiste à utiliser ddev pour utiliser un environnement conteneurisé adapté à Drupal.

1. Installer ddev
Pour mac : `brew install drud/ddev/ddev`
Pour les autres système d'opération, consulter cette page : https://ddev.readthedocs.io/en/stable/users/install/ddev-installation/
2. Se placer dans le projet et lancer la commande : `ddev start`
3. Puis 'ddev composer install'
4. Puis 'ddev import-db dump.sql.gz'
5. Consulter le site depuis un des urls proposé par ddev.
   `ddev describe` pour retrouver l'url si perdu.

### Option 2 - En utilisant le serveur built-in a php.

Il est nécessaire d'avoir php d'installé 8.0 ou supérieur, une base de donnée à disposition et composer.

1. Renseigner les info de connexion dans le fichier .env.
2. Y ajouter la variable d'environnement `USE_DDEV_DB=0`.
3. `composer install`.
4. Se placer dans le dossier web et lancer le serveur `php -S localhost:8090 .ht.router.php`.
5. Consulter le site.
