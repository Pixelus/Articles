# Gestion de version avec Git et Bitbucket

Le gestionnaire de version est l'outil indispensable du développeur qui souhaite enregistrer et conserver les différentes versions de ses fichiers, images, codes sources... Ce système de contrôle des versions (SCV ou SCV en anglais) permet notamment au développeur de :
* gérer un projet seul ou avec d'autres développeurs
* garder une trace des changements effectués dans le projet en cours
* revenir à une version antérieure d'un document
* faciliter la collaboration avec les autres personnes intervenant dans le projet
* partager les fichiers avec les autres développeurs du projet

Pour contrôler les versions de ses fichiers, le développeur utilise un logiciel de gestion de version et un hébergeur de dépôt. Un **logiciel de version décentralisé** comme [Git](https://git-scm.com/) permet à chaque développeur de travailler de son côté, à son rythme et de façon asynchrone des autres développeurs. Il existe ainsi plusieurs dépôts venant de chaque intervenant.

<p align="center">
  <img width="100" src="https://github.com/Pixelus/Articles/blob/master/assets/git.png" "Git">
</p>

À l'inverse, dans une **gestion de version centralisée**, il n'existe qu'un seul dépôt des versions sur lequel tout le monde travaille, ce qui peut être un risque dans le sens où l'expérimentation sur un fichier peut casser tout le projet. Un service web d'hébergement de dépôt est également nécessaire afin que les développeurs disposent d'un canal d'échange pour leurs travaux respectifs.
[Bitbucket](https://bitbucket.org/) est un hébergeur gratuit pour les dépôts Git et [Mercurial](https://www.mercurial-scm.org/) (un autre logiciel de version décentralisé).

<p align="center">
  <img width="200" src="https://github.com/Pixelus/Articles/blob/master/assets/bitbucket.png" "Bitbucket">
</p>

Il existe un autre service web d'hébergement plus connu, [GitHub](https://github.com/), qui permet lui aussi de stocker en ligne les dépôts publics ou privés.

## Comparatif entre Bitbucket et GitHub

|  | Bitbucket | Git |
| :---         |     :---      |          :--- |
| Dépôt public   | gratuit     | gratuit    |
| Dépôt privé    | gratuit       | payant      |
| Nombre de développeurs   | 5 maximum     | illimité    |
| Conclusion    | Plus économique pour les projets nécessitant une petite équipe ou pour les projets privé.       | Mieux adapté pour les grands projets ou les projets open source.      |

**GitHub** est payant pour l'hébergement des dépôts privés, et est plus focalisé sur les dépôts publics et l'open source. **Bitbucket** est gratuit pour l'hébergement des dépôts privés de façon illimitée et permet d'héberger ses fichiers privés. À vous de déterminer quel est l'aspect le plus important pour vous, être visible et privilégier l'open source ou travailler en équipe sur de petits projets ou des dépôts privés.

## Fonctionnement de Git

Git se comporte comme un arbre avec des branches. La base du tronc est le dossier parent auquel sont rattachés les dossiers enfants. Les différentes branches de l'arbre sont les bifurcations. Travailler sur une **branche** permet de faire une bifurcation sur la branche principale, cela sert pour intégrer une nouvelle fonctionnalité ou un nouveau module dans son projet par exemple.
On construit cet arbre en créant des commits. Un [commit](https://git-scm.com/docs/git-commit) est un instantané d'un fichier, c'est comme un maillon de notre chaîne, une sorte de checkpoint. La construction d'un **commit** est définitif car son contenu ne pourra jamais être modifié, on travaillera toujours avec une copie de ce contenu.

Git utilise 3 zones de travail :

* le [Working Directory](https://git-scm.com/book/fr/v2/D%C3%A9marrage-rapide-Rudiments-de-Git#Les-trois-%C3%A9tats) qui est le dossier de travail contenant les fichiers dans leur version actuelle
* l'[index](https://git-scm.com/book/fr/v2/Les-bases-de-Git-Enregistrer-des-modifications-dans-le-d%C3%A9p%C3%B4t) qui permet de stocker les modifications, l'index s'appelle aussi [Cache](https://git-scm.com/book/fr/v2/Les-bases-de-Git-Enregistrer-des-modifications-dans-le-d%C3%A9p%C3%B4t) ou [Staging Area](https://git-scm.com/book/fr/v2/Les-bases-de-Git-Enregistrer-des-modifications-dans-le-d%C3%A9p%C3%B4t)
* l'[HEAD](https://git-scm.com/book/fr/v2/Les-tripes-de-Git-R%C3%A9f%C3%A9rences-Git#La-branche-HEAD) qui pointe vers le dernier commit

## Création d'un projet avec Git et Bitbucket

Git s'utilise en ligne de commande mais il existe des interfaces graphiques comme par exemple [SourceTree](https://www.sourcetreeapp.com/) de Atlassian, qui permet de se connecter à un serveur distant pour cloner des dépôts existants.

Pour créer votre premier projet avec Git et Bitbucket, vous devez au préalable :

* créer un compte chez [Atlassian](https://fr.atlassian.com/software/bitbucket)
* télécharger et installer la dernière version de [Git](https://git-scm.com/)
* exécutez les commandes suivantes dans votre terminal pour paramétrer vos identifiants d'utilisation de Git

```
git config --global user.name "Votre pseudo"
git config --global user.email "Votre email"
```

Relancez votre terminal et vérifier que git fonctionne en tapant

```
git
```

Un guide d'utilisation de Git devrait s'afficher en anglais dans votre console.

* connectez-vous sur le site de bitbucket et créer un dépôt en allant sur *Créer > Créer un dépôt*
* remplissez le formulaire pour créer votre nouveau dépôt (donnons lui le nom de Projet) en n'oubliant pas de cocher les cases *Gestion de bug* et *Wiki*, puis cliquez sur *Créer un dépôt*
* cliquez sur Cloner le dépôt en haut à gauche et copier l'adresse HTTPS
* ouvrez votre terminal et placez vous dans le dossier de stockage de vos dépôts en utilisant la ligne de commande

Si vous ne savez pas utiliser le langage Shell en ligne de commande, je vous recommande le très bon tutoriel [Reprenez le contrôle à l'aide de Linux](https://openclassrooms.com/fr/courses/43538-reprenez-le-controle-a-laide-de-linux/38076-entrer-une-commande) sur le site d'OpenClassrooms.

* lorsque vous êtes positionné dans votre dossier de dépôt dans votre terminal, collez l'adresse HTTPS que vous avez copié précédemment
* tapez ensuite les commandes suivantes :
 
```
git status
```
→ détermine l'état des fichiers dans le dépôt et indique s'ils sont suivis
```
git add projet
```
→ ajoute le dossier *projet* à l'index, on place le dossier sous version, cela indique à Git de suivre le dossier projet
```
cd projet
```
→ ce paramètre vous place dans le dossier *projet*
```
git init nouveau dossier
```
→ crée un nouveau dépôt ou [repository](https://fr.wikipedia.org/wiki/D%C3%A9p%C3%B4t_(informatique)) vide s'appelant *nouveau_dossier*
```
ls
```
→ liste les fichiers et dossiers du répertoire courant, vous pouvez constater qu'un nouveau dossier appelé *nouveau_dossier* existe maintenant dans votre dossier *projet*
```
git status
```
→ le terminal nous indique qu'il y a un nouveau dossier, le dossier *nouveau_dossier*, et que ce fichier n'est pas suivi par la gestion de version
```
git add nouveau_dossier
```
→ ajoute le dossier *nouveau_dossier* à l'index, Git nous indique qu'il y a un nouveau dossier suivi
```
git commit -m "Premier commit"
```
→ crée un commit avec le message "Premier commit" et valide les modifications enregistrées
```
git log
```
→ inspecte l'historique des commits, vous pouvez voir que votre commit apparaît avec la date, l'heure, le nom du commit et votre message
```
git push
```
 → envoie les commits sur le serveur sinon vos commits restent en local

* retournez sur votre compte Bitbucket et actualisez la page de votre premier dépôt, celle où vous avez copié l'adresse HTTPS du dépôt. Vous pouvez constater que votre dépôt a bien été envoyé sur votre serveur, et vous pouvez voir les dossiers créés dans l'onglet *Source* situé sous l'onglet *Vue d'ensemble* dans le menu de gauche.

Vous venez de créer votre premier dépôt. A vous maintenant d'explorer les possibilités offertes avec la gestion de version. Voici quelques autres commandes utiles qui pourront vous servir :

```
git commit -a
```
→ place tout fichier déjà en suivi de version dans la zone d'index afin d'éviter de faire un *add*
```
git rm -f mon_fichier
```
→ supprime et désindexe le fichier *mon_fichier*
```
git rm --cached mon_fichier
```
→ arrête le suivi du fichier *mon_fichier* mais le conserve dans la copie de travail
```
git mv mon_fichier monnouveaufichier
```
→ renomme le fichier *mon_fichier* en *mon_nouveau_fichier*
```
git show
```
→ affiche les détails d'un objet Git
```
git diff
```
→ affiche les modifications indexées et non indexées entre deux fichiers
```
git branch ma_branche
```
→ crée une nouvelle branche avec le nom *ma_branche*
```
git checkout
```
→ se positionne sur la branche voulue
```
git checkout -b ma_branche
```
→ crée la branche *ma_branche* et se positionne immédiatement dessus
```
git merge ma_branche
```
→ fusionne la branche *ma_branche* avec la branche sur laquelle on se trouve
```
git pull
```
→ récupère et télécharge les nouveaux commits présents sur le serveur

## Ressources

Voici quelques liens qui pourront vous initier plus en détails à Git :

* Aide–mémoire interactif sur Git (en français) : [http://ndpsoftware.com/git-cheatsheet.html](http://ndpsoftware.com/git-cheatsheet.html)
* Application en ligne Learn Git Branching (en français !) : [http://pcottle.github.io/learnGitBranching/](http://ndpsoftware.com/git-cheatsheet.html)
* Vidéos d'apprentissage sur le site de Git (en anglais) : [http://git-scm.com/videos](https://git-scm.com/videos)
* Cours d'Udacity sur Git (en anglais) : [Version Control with Git](https://www.udacity.com/course/version-control-with-git--ud123)
* Conférence d'Anna Whitney dans le cadre du cours Computer Science CS50 de Harvard (en anglais) : [How (and Why) You Should Use Git](https://www.youtube.com/watch?v=71WzH4inmkg&feature=youtu.be)
* Conférence de Brian Yu dans le cadre du cours Computer Science CS50 de Harvard (en anglais) : [An Introduction to Git and GitHub](https://www.youtube.com/watch?v=MJUJ4wbFm_A&feature=youtu.be)
