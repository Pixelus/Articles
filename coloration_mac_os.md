# Activer la coloration syntaxique dans le terminal de Mac OS X

Sur un Mac, il est parfois utile de pouvoir faire la différence entre les dossiers, les fichiers et les instructions tapées dans le terminal. L'activation de la coloration syntaxique permet de mieux distinguer chaque élément, et par la même occasion elle apporte un réel confort de lecture. Sans cette activation de couleur, le terminal ressemble à l'image ci-dessous :

<p align="center">
  <img width="480" src="https://github.com/Pixelus/Articles/blob/master/assets/terminal-default.jpg" "Terminal">
</p>

Pour activer la couleur dans notre terminal, il va nous falloir modifier le fichier *.bash_profile* dans lequel sont placées les variables d'environnement. Les **variables d'environnement** permettent d'influencer le comportement des applications du système, comme par exemple ici l'application Terminal.
Ce fichier $.bash_profile$ est ce que l'on appelle un **fichier caché**, reconnaissable au point placé devant le nom du fichier. Il est exécuté au lancement de la session de l'utilisateur.

## Activation de la couleur dans le terminal

* ouvrez votre terminal – vous devriez avoir un affichage basique avec le nom de votre Mac suivi de l'identifiant de connexion de votre session

<p align="center">
  <img width="480" src="https://github.com/Pixelus/Articles/blob/master/assets/terminal.jpg" "Terminal">
</p>

* vérifiez que le fichier *.bash_profile* existe en tapant dans la console l'instruction suivante

Vous pouvez collier-coller l'instruction : 

```
ls -la | grep ".bash_profile"
```

Cette ligne de commande liste les fichiers du répertoire courant, en incluant les ficiers cachés, et ne conserve que les lignes contenant la clé *.bash_profile*. Si le terminal affiche un message indiquant que le fichier n'existe pas, vous pouvez le créer avec l'instruction suivante :

```
touch .bash_profile
```

* éditez votre fichier *.bash_profile* afin de modifier les variables d'environnement – l'instruction suivante permet d'ouvrir votre fichier dans l'application [TextEdit](https://fr.wikipedia.org/wiki/TextEdit), l'éditeur de texte par défaut sur Mac :

```
open -a "TextEdit" .bash_profile
```

TextEdit ouvre une page vide que l'on va pouvoir remplir.

* si vous utilisez un terminal avec un arrière-plan clair, ajoutez les paramàtres suivants au fichier *.bash_profile* :

```
export CLICOLOR=1
export LSCOLORS=ExFxCxDxBxegedabagacad
```

* si vous utilisez un terminal avec un arrière-plan noir ou foncé, préférez les paramètres suivants :

```
export CLICOLOR=1
export LSCOLORS=gxBxhxDxfxhxhxhxhxcxcx
```

Voici le résultat avec la couleur activée dans un terminal de couleur claire.

<p align="center">
  <img width="480" src="https://github.com/Pixelus/Articles/blob/master/assets/terminal-light.jpg" "Terminal">
</p>
