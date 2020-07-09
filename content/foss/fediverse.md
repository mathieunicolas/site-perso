---
title: Le fediverse
description: Le point sur l'univers des réseaux sociaux décentralisés fédérés, où vos données sont respectées, et où le libre et l'open-source est de rigueur. Une alternative intéressante au monopole de Facebook, Twitter et consorts ?
icon: fab fa-linux
tags:
  - fediverse
  - foss
---

## Le monde selon facebook

Depuis quelques années maintenant, ce n'est plus un secret : facebook propose au monde entier un formidable réseau social qui permet à quelques [2,6 milliards de personnes](https://www.journaldunet.com/ebusiness/le-net/1125265-nombre-d-utilisateurs-de-facebook-dans-le-monde/) à travers le monde d'interagir aussi simplement que s'ils étaient voisins. On échange des photos, on partage des infos, on participe à la promo des artistes que l'on aime, on s'indigne ensemble, on se réjouit ensemble, on organise nos soirées... **Bref, le rêve !**

### Collecte extrême et hypercentralisation

Sauf que le rêve peut rapidement devenir un cauchemar : dans [cet article](https://www.gqmagazine.fr/lifestyle/high-tech/articles/mark-zuckerberg-est-desole-que-vos-donnees-aient-ete-volees-et-il-va-essayer-de-les-securiser/61831), on peut lire quelques témoignages de personnes qui ont fait l'expérience de télécharger l'intégralité de "leurs données facebook" (comprendre les données qui ont été collectées par la plateforme), et qui après examen approfondi ont eu quelques mauvaises surprises. "J'y ai retrouvé le numéro de téléphone de ma grand-mère alors qu'elle n'a jamais eu de compte", "ça a préservé les conversations que j'avais eu avec mon ex, alors même que j'avais rompu tous les liens digitaux avec lui", "j'ai appris que Kate Spade New York et Metlife m'ont dans leur liste en tant qu'annonceur", etc, etc...

Parler de collecte de données est un doux euphémisme : on peut carrément parler de moisson ! Facebook collecte absolument tout, et s'en sert bien volontiers. Aujourd'hui pour vous identifier, savoir quelles publicités vous conviendraient le mieux, faire des liens entre votre profil et celui d'autres personnes... Mais demain ? Qui peut savoir à quoi pourraient bien servir un jour ces quantités astronmiques de données soigneusement stockées et étudiées par l'ami Mark ?

Une chose est sûre, ["quand c'est gratuit, c'est vous le produit"](https://www.youtube.com/watch?v=9CAgWLVdiDE) ! Mais le problème n'est pas simplement lié à facebook, Google étant également un sacré performer dans l'univers de la collecte de données. Et peut-être que finalement, le pire dans tout ça est de concevoir que toutes ces informations qui en disent tant sur nous soient rassemblées en un même endroit ?

La centralisation extrême autour de ces "géants du numérique" fait clairement partie des raisons qui rendent ces abus possibles, au-delà du fait que **la simple utilisation de nos données, volontiers cédées, ne leur permet que de faire de nous des produits commerciaux plus juteux encore**.

#### Deux problèmes, donc : le manque de transparence à propos de la collecte et l'utilisation de nos données, et la centralisation de leur stockage/traitements.

## Une solution : le fediverse

Le terme fediverse est la contraction de _federation_ et _universe_ : il rassemble des logiciels et protocoles qui sont en mesure d'interagir et de parler en quelque sorte une langue commune. La notion de fédération est passionante !

### diaspora\*

Prenons un exemple, celui de [diaspora\*](https://diasporafoundation.org/) : c'est un réseau social comparable à facebook dans son interface, basé sur trois concepts clés (plus largement détaillés sur leur site internet) :

- décentralisation : c'est le principe même du fediverse, nous y reviendrons
- liberté : d'être qui l'on veut, ou ce que l'on veut. Pas de vérification d'identité, vous pouvez adopter le pseudonyme que vous voulez. C'est également un logiciel libre, il est donc possible d'en faire ce que l'on veut.
- confidentialité : vous demeurez l'unique propriétaire de vos données. Vous n'octroyez à personne le droit de disposer de vos données, et vous choisissez parfaitement ceux avec qui vous les partagez.

Cet article s'intitule **fediverse**, nous allons donc aborder la notion de décentralisation. Le principe de diaspora*, c'est que c'est en fait un réseau constitué de plusieurs *instances\* qui sont en mesure d'interagir entre elles. Une instance, c'est simplement l'installation d'une copie du logiciel sur un serveur, maintenue par son créateur (une personne, une association, ...), afin que des utilisateurs puissent s'y créer un compte.

Par exemple, l'association [framasoft](https://framasoft.org) a créé sa propre instance diaspora\* : c'est la [framasphère](https://framasphere.org). N'importe qui peut créer son compte sur cette instance, et l'utiliser à peu de choses près pour les mêmes pratiques que facebook. Il existe des milliers d'instances diaspora\* à travers le monde, et chaque instance peut accueillir ses propres utilisateurs. Là où la magie de la fédération opère, c'est que tous les utilisateurs peuvent interagir entre eux, à travers les frontières des instances !

### Le gros acteur : mastodon

Un autre exemple qui illustre à merveille la fédération est la plateforme [mastodon](https://joinmastodon.org). C'est une plateforme de microblogging, comparable à twitter. Là aussi, on parle d'instances. Certaines accueillent quelques dizaines d'utilisateurs, d'autres plusieurs milliers. Mais tous ces utilisateurs peuvent interagir entre eux, quelle que soit l'instance sur laquelle ils se sont inscrits à la base. [Vous pouvez consulter ici une liste non exhaustive des instances mastodon.](https://joinmastodon.org/#getting-started)

**Mais mastodon va plus loin**. En effet, la plateforme développe le protocole [ActivityPub](https://fr.wikipedia.org/wiki/ActivityPub) qui permet de connecter bien plus de choses qu'un simple service de microblogging. Par exemple, framasoft a développé un service qui s'appelle [PeerTube](https://joinpeertube.org) et qui se veut une alternative libre à YouTube, qui est parfaitement interconnectée à mastodon.

Cela signifie que, depuis votre compte mastodon, vous pouvez vous abonner à une chaîne PeerTube, et voir apparaître dans votre fil d'actualité les vidéos publiées. Encore mieux : il suffit de réagir à la notification _depuis mastodon_ pour que votre réponse soit considérée comme un commentaire, posté sous la vidéo, dans PeerTube ! De la même façon, [pixelfed](https://pixelfed.org/) se veut être une alternative libre à Instagram, et est également interconnecté à mastodon. Il existe ainsi de nombreux [projets libres qui sont basés sur le même protocole](https://fr.wikipedia.org/wiki/Fediverse#Les_membres_du_Fediverse), et qui peuvent interagir avec mastodon ! Imaginez pouvoir vous abonner indifféremment à des chaînes youtube, des comptes instagram, des blogs, etc...

Et bien, le fediverse, c'est cela ! Sans oublier que chaque projet est également décentralisé, et fonctionne sous la forme d'une multitude d'instances disséminées à travers le monde : c'est la protection parfaite contre la centralisation et l'exploitation de vos données et de votre vie privée. Chaque instance est responsable de la protection des données des utilisateurs qui y sont inscrits. Les projets étant **libres**, il est tout à fait possible d'accéder au code source, et donc de s'assurer qu'aucun mouchard n'est implanté pour profiter sournoisement de votre naïveté (supposée).

**À noter** : le petit dernier de framasoft, [Mobilizon](https://joinmobilizon.org/fr/), permettra, toujours en étant compatible avec mastodon via ActivityPub, d'organiser les rassemblements, évènements, goûters d'anniversaires et autres concerts, sur une plateforme libre. À surveiller de près, la beta fonctionne depuis quelques mois maintenant, et la version finale devrait être dispo d'ici la fin de l'année !

### Conclusion

Quand j'ai découvert cet univers, j'ai passé énormément de temps à l'explorer. Je trouve passionnant que grâce aux bonnes volontés de tous une autre façon d'aborder les réseaux sociaux soit possible, une façon à mon sens plus reposante, plus sereine. Il existe quelques points qui font que cette solution n'est pas parfaite, notamment le fait que la démocratisation n'est pas encore tout à fait amorcée (on compte quelques millions d'utilisateurs, face aux milliards présents sur facebook et twitter). Pour certains, c'est une bonne chose car cela permet d'opérer un premier tri sur le volet, mais personnellement je suis toujours un peu déçu de devoir jongler entre mastodon et twitter (même si les abonnements RSS permettent de pallier à cela), ou de devoir retourner sur YouTube pour suivre certaines chaînes que j'affectionne particulièrement. Mais le temps fait son oeuvre, et je suis persuadé que le fediverse a de beaux jours devant lui !

En tous cas, pour ma part, c'est une merveilleuse alternative à facebook, twitter et youtube, le trio que j'utilisais quotidiennement et que je commençais à trouver plutôt oppressant. J'aime la sensation de récupérer le contrôle sur mes données, sur mon temps de cerveau disponible, de sortir de cette cage dorée forgée par Google et Facebook. Vous pouvez donc me rejoindre sur le fediverse, après avoir choisi votre instance mastodon et/ou diaspora\*, en tapant dans la barre de recherche :

- [@mathieu@diaspodon.fr](https://diaspodon.fr/web/accounts/101167) pour mastodon
- [@mathieunicolas@framasphere.org](https://framasphere.org/people/8afe88907bc10138dfca2a0000053625) pour diaspora\*

**Et surtout, si ça vous branche mais que vous ne savez pas trop par où commencer, venez m'en parler, je me ferai un plaisir de vous accompagner !**
