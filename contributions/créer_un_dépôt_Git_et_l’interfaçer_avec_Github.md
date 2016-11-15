## Créer un dépôt Git et l’interfaçer avec Github

### Les raisons
  
Nous souhaitons lié le code écrit en *local* pour le publier sur *Github*. Nous devons donc créer un dépôt *Git* et le configurer pour qu’il interagisse avec le dépôt *distant*.

### Créer et configurer le dépôt Git local
  
On commence par créer un dépôt.  
On y ajoute les fichiers, en commentant.

``` bash
$ git init .
$ git add .
$ git commit -m "Création d'une application Meteor"
```

Reste à lier le dépôt avec *Github*.  
Et finalement, publier les fichiers.

``` bash
$ git remote add origin git@github.com:barbapapa/daktary-meteor
$ git push --set-upstream origin master
```

### Liens
- [Installer Git][1]
- [Découvrir Git avec Thibault][2]
- [Démarrer un dépôt Git][3]

[1]:	https://git-scm.com/book/fr/v2/D%C3%A9marrage-rapide-Installation-de-Git
[2]:	http://www.miximum.fr/blog/decouvrir-git/
[3]:	https://git-scm.com/book/fr/v2/Les-bases-de-Git-D%C3%A9marrer-un-d%C3%A9p%C3%B4t-Git
