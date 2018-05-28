# CMS & Wordpress
#### 
## INTRODUCTION
Dans le cadre de l' UV élective exploration du web, nous travaillons sur le deployement d'un cms en local et la mise en oeuvre de quelques fonctionnalités d'un site de vente sur ce cms. Pour se faire, nous avons opté pour Wordpress.
Dans ce travail, nous allons commencer par présenter de manière génerale ce qu'est un cms, ensuite presenter wordpress  et finir par installer et utiliser wordpress en local.

## 1- Définition d’un CMS

Un SGC(**système de gestions de contenu** ) ou CMS(**content management system**).Les CMS ont été pensés pour créer des sites web sans avoir besoin de connaissances informatiques.Le CMS est une famille de logiciels destinés à la conception et à la mise à jour dynamique de sites Web ou d'applications multimédia. Ce sont des outils qui apportent une très grande aide aux persones qui veulent réaliser sans coder.

 **Ils partagent les fonctionnalités suivantes**[1]:

- ils permettent le travail collaboratif
- ils fournissent une chaîne de publication (workflow) offrant par exemple la possibilité de mettre en ligne le contenu des documents 
- ils permettent de séparer les opérations de gestion de la forme et du contenu 
- ils permettent de structurer le contenu (utilisation de FAQ, de documents, de blogs, de forums de discussion, etc.) 
- ils permettent de hiérarchiser les utilisateurs et de leur attribuer des rôles et des permissions (utilisateur anonyme, administrateur, contributeur, etc.) .

## 2- Pourquoi utiliser  les CMS?

Si vous n’utilisez pas un CMS open source, le processus de création de votre site internet se déroule ainsi[2]:

- L'écriture d’un code source de A à Z
- Le développement des fonctionnalités attendues
- La création intégrale d’un thème sur mesure et  une conception graphique supplémentaire du site
- Intégration de contenu, gestion de contenu web et back office
- Mise en place d’une sécurité sans faille.

Les CMS sont qualifiés d’open source parce qu’ils respectent des critères comme la possibilité de libre redistribution, l’accès au code source...


## 3- CMS e-commerce!
Les CMS e-commerce sont de plus en plus utilisés pour la création de boutiques en ligne. Les avantages sont énormes à savoir la rapidité de deployement, la simplicité d'utilisation  et l'aspect moins coûteux qu'un développement spécifique. 
Dans le cadre de ce cours, nous allons en dire plus sur le CMS  **wordpress**. 

**En quoi cet outil de gestion de contenu vient-il répondre à vos attentes ?**

**Le Wordpress** propose une offre large, des simples blogs aux plateformes e-commerce, en passant par les sites publics. Il organise aussi des manifestations régulièrement pour dynamiser la communauté. Le programme gratuit recherche une expérience client intuitive et agile.

 L’outil vous décharge du codage, et vous aide dans votre gestion de sites, ce qui vous permet de créer un portail professionnel facilement, pour de petites et grandes entreprises. C’est aussi un moyen de vulgariser la pratique et  de publier rapidement sur un site e-commerce, des applications web et autres.




#  Etapes d'installation d'un cms wordpress en local

Pour developper un site Web en utilisant CMS wordpress, on peut soit utiliser directement le site de Wordpress en ligne ou on peut utiliser le serveur local avec Bitnami qui est capable de vous aider à créer votre propre site web sur votre machine local.
Pour y arriver dans ces étapes suivantes:

#### Installation de CMS Wordpress sur une machine locale:
###### Etape1: Telecharger le bitnami suivant son OS(Windows, Mac ou Linux).
[Telecharger Bitnami](https://bitnami.com/stack/wordpress/installer)
###### Etape2: Installer bitnami.

Voici les différentes étapes à suivre pour l'installation de Bitnami. Après avoir telechargé le logiciel on commence l'installation comme les autres applications en faisant double clique sur fichier Bitnami telechargé et le fenetre d'installation s'affiche.Les captures durant l'installation qu'on a faite vous aidera dans la votre.
![](https://i.imgur.com/H4VaVXT.png)
Fig1:installation de bitnami commence en cliquant yes

Ici on continue avec option de next 
![](https://i.imgur.com/JOOvAVO.png)
Fig 2

Ici on coche les deux que ça soit wordpress pour installer l'application wordpress et phpMyAdmin pour gérér les base des données utilisées dans l'application
![](https://i.imgur.com/FDZrWyY.png)
Fig 3
![](https://i.imgur.com/nvlLm8U.png)
Fig 4:Création du compte 

**NB: Il faut garder ces noms d'utilisateur car ils seront utilisée après l'installation**

![](https://i.imgur.com/Sb1Aa59.png)
Fig 5:Port  444 de ssl 444 qui est celle de l'interface web 

![](https://i.imgur.com/FS4eQ9R.png)
Fig 6: Next pour lancer bitnami
![](https://i.imgur.com/Ye7eiYz.png)
Fig 7: Installer wordpress stack

![](https://i.imgur.com/tDtqhCb.png)
Fig 8:Installation en cours ça prend quelques minutes

![](https://i.imgur.com/g030Z8R.png)
Fig 9:Finalisation de Bitnami

![](https://i.imgur.com/LNTu5vz.png)
Fig 10:Bitnami est deja installé on peut acceder à wordpress en cliquant **Access Wordpress**

![](https://i.imgur.com/1mkFfn9.png)
Fig11:Accès de votre site wordpress sur notre machine locale(Rappelez-vous des identifiants  utilisés durant l'installation). 



Pour les prochaines fois,pour acceder au site en utilisant:**127.0.0.1/wordpress**
Pour modifier et developper notre site on utilise:**127.0.0.1/wordpress/wp-admin**

**NB:on oublie pas d'allumer le serveur avant tout**!! 


## 4- Site de vente avec le cms wordpress: Quelques fonctionnalités!

Les exigences du projet sont en gros de présenter un  thème wordpress contenant les éléments de base d'une page web générale (aucune esthétique n'est requise, seules les fonctions de base sont requises) mais aussi des fonctionnalités spécifiques au site de vente en ligne.Nous allons vous montrer comment faire ajouter ces différentes fonctionalités.

    1Tableau de bord de notre site Imt e-store
    
![](https://i.imgur.com/InJNdLu.png)

C'est cette interface qui va nous aider à créer notre site et à le personnaliser. On commence d'abord par choisir le thème que l'on veut utiliser dans l'onglet 'theme' qui se trouve dans 'apparence'.

![](https://i.imgur.com/ORqQTAi.jpg)

Les thèmes diffèrent selon le domaine abordé. Vu que nous travaillons sur un site e-commerce,nous avons choisi ce thème(Access Press Store) qui est cohérent avec ce que nous voulons déveloper.
![](https://i.imgur.com/vJdZxBl.png)

Comme la page de tableau de Bord  le montre tous les onglets de manipulation du site sont apparus.
On peut créer les differents pages et les articles qui doit étre affiche et utilisé sur le site. Le site et son contenu peuvent être organisés dans l'option de personnaliser qui  se trouve dans l'onglet apparence.
![](https://i.imgur.com/FBnzT02.png)
            Creation du page





### Extension "woocommerce" ###
WordPress propose des extensions pour pouvoir faire fonctionné certaines des fonctionnalités du site choisis. 

Comme nous faisons un  site de e-commerce WordPress propose une extention ***"WooCommerce"*** qui  renferme toutes les fonctionalités des sites de commerce.
Une foi cette extension installée, on peut ajouter les produits. les utilisateurs peuvent ajouter des prduits dans le panier, faire une commande, reserver,acheter...en gros toutes les actions pour acheter ou voir les produits sur le site. 

Pour installer ***woocommerce*** il ya deux options:
Telecharger l'extension Bitnami sur ordinateur ou le telecharger directement en passant par l'option des extensions sur un tableau de bord  du site.
![](https://i.imgur.com/WZpmDRE.png)![Uploading file..._ns3lusa7k]()


Au moment l'extension de wooCommerce est bien installé, on organise le site suivant notre volonté.


Pour resumer tout ce que nous avons dit jusque la et meme aller plus loin, vous pouvez regarder le tutorial ci-après. Bonne chance avec votre site de vente en ligne.
[Voir le tutoriel](https://www.youtube.com/watch?v=eVQu-eUwaXw)



## Source
1.https://fr.wikipedia.org/wiki/Syst%C3%A8me_de_gestion_de_contenu
2.https://www.appvizer.fr/magazine/marketing/site-web-cms/plone/11-cms-open-source-en-francais-pour-creer-un-site-web-professionnel
3.https://www.zhihu.com/question/21219196/answer/350380729


