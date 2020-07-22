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
