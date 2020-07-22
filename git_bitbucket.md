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

