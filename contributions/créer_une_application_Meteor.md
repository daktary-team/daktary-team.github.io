## Création d’une application Meteor

### Les raisons
  
À cette étape, nous avons besoin de pouvoir coder sans trop nous engager sur la plateforme technologique.
Les besoins apparaitrons au fur et à mesure. Nous pensons que nos décisions seront plus pertinentes quand nous aurons commencer à explorer le produit.

Pour commencer le développement du produit, nous choisissons de partir sur *[Meteor][1]*. C’est une décision arbitraire qui devrait nous permettre de gagner du temps au début. Cet outil propose une solution simple et relativement complète pour développer un projet sans se préoccuper des choix pour constituer un environnement *JavaScript* simple mais consistant.

### Éléments requis
  
L’interaction avec *Meteor* se fera en ligne de commande et avec le navigateur. La [documentation][2] est plutôt bien faite et fréquemment actualisée.

Avant de commencer il faut installer *Meteor* :
- accéder à un terminal
- puis installer le *framework*
``` bash
`$ curl https://install.meteor.com/ | sh
```

### Créer une application Meteor
  
Pour créer un projet, ouvrir le terminal et :
``` bash
$ meteor create daktary-meteor
$ cd daktary-meteor
$ meteor
```
`  
La commande *meteor* lance un serveur Web accessible à l’adresse :
[http://localhost:3000][3]

### Configurer une structure de fichiers minimales

On peut commencer par supprimer les fichiers de démonstration.
``` bash
$ rm daktary-meteor.js daktary-meteor.html daktary-meteor.css
```

Puis créer une nouvelle structure :
``` bash
$ mkdir client
$ touch client/index.html client/main.js client/style.css
```

Par convention *Meteor*, les fichiers placés dans le dossier */client* ne seront exécutés que par le navigateur.

### Liens

- [Meteor][1]
- [Documentation Meteor][2]


[1]:	http://www.meteor.com
[2]:	http://docs.meteor.com/#/full/
[3]:	http://localhost:3000
