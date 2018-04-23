# Session 2018 du cours "Exploration du Web" IMT Atlantique [ELU 525](https://portail.telecom-bretagne.eu/portal/pls/portal/pkg_df.programmes.SHOW_FICHE?p_id_mod_er=32168)
Avril - Juin 2018

* Breaking news : 17 avril 2018 les étudiants du cours prennent le pouvoir et le renomme "le Tour du Web en 80 jours" et décident qu'ils sont leurs propres étudiants !

![Le tour du monde en 80 jours](https://upload.wikimedia.org/wikipedia/commons/6/64/%27Around_the_World_in_Eighty_Days%27_by_Neuville_and_Benett_02.jpg)

# Déroulé du cours
* [6 avril 2018 - Séance 1](seances/seance1.html)
* [9 avril 2018 - Séance 2](seances/seance2.html)
* [13 avril 2018 - Séance 3](seances/seance3.html)
* [16 avril 2018 - Séance 4](seances/seance4.html)
* [17 avril 2018 - Séance 5](seances/seance5.html)

# Les bases du web 




## HTML
 Le HTML, ou « HyperText Markup Language », est un langage permettant d’écrire de l’hypertexte pour afficher des pages web. Tout site web a besoin de HTML pour s’afficher.
* Le HTML est un langage utilisant des balises permettant de décrire la structure d’une page web et de l’afficher.
> Le langage HTML est un langage structuré qui décrit un document grâce à des balises. Les balises sont des valeurs entourées de deux caractères, *<* et *>*, qui décrivent, à partir de paramètres propres à la balise appelés 'attributs', le contenu sémantique de la donnée.
> 
 ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/retour-ligne-espace-html.png)
> 
> La première balise de la paire de balises est la balise ouvrante *<nom>*, et l'autre est la balise fermante *</nom>*. Les informations au milieu de la paire de balises sont les éléments qui sont affichés sur le site web. Les éléments peuvent être un texte, une image, une vidéo, un lien, etc. 

* Le HTML possède de nombreux contrôles qui sont notamment utilisés pour la saisie de données dans des formulaires.
> Les contrôles sont les zones à remplir sur un site web, et un ou plusieurs zones de contrôles définissent un formulaire. Après remplir les zones, un formulaire sera généré.
> 
![](https://sdz-upload.s3.amazonaws.com/prod/upload/01_04_03_01_formulaire.png)

> Un formulaire c’est une balise *<form>* qui contient une méthode pour envoyer les paramètres (méthode *GET* ou *POST*) et l’adresse d’un script (ou d’une action) qui sera appelé avec ces paramètres et vers lequel sera redirigé l’utilisateur.

* En plus du langage HTML, les pages web contiennent du CSS, langage permettant de modifier le style des pages, et du JavaScript, langage permettant d’ajouter de l’interactivité à ces pages.

* Pour plus d'information : [Introduction au HTML](https://openclassrooms.com/courses/apprendre-asp-net-mvc/introduction-au-html) et [HTML5 Tutorial](https://www.w3schools.com/html/)




## CSS
CSS (Cascading Style Sheets), c'est un autre langage qui vient compléter le HTML. Il gére la mise en forme de notre site web.
Dans ce chapitre, nous allons voir la théorie sur le  CSS:
   * qu'est ce que c'est ?
     * vous permet de choisir la couleur du texte.
     * vous permet de sélectionner la police utilisée sur votre site.
     * c'est lui encore qui permet de définir la taille du texte, les bordures, le fond etc.
     * Et aussi, c'est lui qui permet de faire la mise en page de votre site.
     * Exemple d'une page web écrit en HTML(sans css) et la même page web écrit en HMTL+CSS
      
     ![](https://user.oc-static.com/files/339001_340000/339428.png)
     
     Grâce au HTML,vous pouvez rédiger le contenu de la page web mais qui sera exempt de style et brut.Le CSS vient compléter ce code pour mettre en forme tout cela et donner au contenu l'apparence que l'on souhaite.
   * Où est ce qu'on écrit du code css?
     Vous avez le choix car on peut écrire du code en langage CSS à trois endroits différents :

      * dans un fichier.css(méthode la plus recommandée) car cela nous évite de mélanger les codes css et html dans tout un même fichier ;
      * dans l'en-tête<head>du fichier HTML ;

      * directement dans les balises du fichier HTML via un attribut 'style'(méthode la moins recommandée);
* vous noterez le contenu de la ligne 5,<link rel="stylesheet" href="style.css" />: c'est elle qui indique que ce fichier HTML est associé à un fichier appelé style.css qui est chargé de la mise en forme.
      ![](https://i.imgur.com/gqPeQzL.png)

* Il faut noter que les navigateurs ne connaissent pas toutes les propriétés de CSS qui existent. Plus le navigateur est vieux, moins il connaît de fonctionnalités CSS qui sont mis à jour.

* **exemple pratique: Mettre tous les paragrpahes de votre page web en bleue** 
     * Maintenant, créez un nouveau fichier vide dans votre éditeur de texte et copiez-y ce bout de code CSS
        * la balise p signifie paragraphe en html 
      * ![](https://i.imgur.com/eAPaE81.png)
      * Enregistrez le fichier en lui donnant un nom qui se termine par .css , comme style.css.Placez ce fichier.css dans le même dossier que votre fichier.html comme dans l'image ci-dessous.
      ![](https://i.imgur.com/rJPdtq6.png)
       * Ouvrez maintenant votre fichier page_web.html dans votre navigateur pour le tester, comme vous le faites d'habitude. Regardez,vos paragraphes sont écrits en bleu, comme dans la figure suivante !
       ![](https://user.oc-static.com/files/342001_343000/342657.png)
* Pour aller plus loin sur les notions de CSS, voir les liens suivant: [openclassrooms](https://openclassrooms.com/courses/apprenez-a-creer-votre-site-web-avec-html5-et-css3/mettre-en-place-le-css) et le cours de [pierre-giraud](http://www.pierre-giraud.com/html-css/cours-complet/selecteurs-proprietes-css.php).
## PHP

**- Les sites statiques et les sites dynamiques**
* On peut distinguer deux types de sites internet : Les sites **statiques** et les sites **dynamiques**. Les sites statiques sont écrits uniquement en HTML et CSS et par conséquent, leur contenu ne peut être modifié qu'en accédant directement au code source => Les sites statiques ne permettent donc pas l'interaction ! 
![](https://i.imgur.com/8toeezp.png)
* Les sites dynamiques, sont les sites dont le contenu peut changer sans l'intervention d'un webmaster. Ils nécessitent d'autres langages en plus de HTML et CSS. Nous verrons ici le cas du php.

**- Fonctionnement d'un site web écrit en php (notion de langage "server-side")**
![](https://i.imgur.com/3dUnKFq.png)
* Ceci est un premier exemple de code php. Comme vous le voyez, c'est une balise php qui s'intègre dans le corps du fichier HTML basique.
*NB : Dès le moment où on intègre une balise php dans un script HTML, il faut changer l'extension du fichier en .php*
* Le navigateur interprète le code HTML et CSS mais il ne comprends pas le php. En effet, le php est interprété côté **serveur**, là où la page est générée. 

**- Environnement de travail et pré-requis**
* Comme avec HTML et CSS, vous n'aurez besoin que d'un éditeur de texte pour écrire des scripts php. Néanmoins, pour tester le résultat en local, on doit recréer une architecture serveur. Pour cela plusieurs logiciels sont disponibles (suivant l'os que vous utilisez)
    
    --Pour Windows privilégiez [Wamp](https://www.wampserver.com/).
    
    --Pour Mac Os, il y a [Mamp](https://www.mamp.info/).
    
    --Pour Linux, [Xampp](https://www.apachefriends.org/) est disponible.

* Ces logiciels permettront d'interpréter le code php et le transformer en HTML à fin que le navigateur puisse le comprendre.

**- Enregistrer un fichier php et l'afficher**
* Pour que le code php soit interprété par le logiciel dédié, il faudra enregistrer le fichier dans le dossier correspondant  au logiciel utilisé.

* Pour Wamp, il s'agit du sous dossier "wamp", pour mamp et xampp, ce sera le sous dossier "htdocs".

* Pour afficher ensuite le résultat, il faut accéder depuis votre navigateur au dossier dans lequel a été stocké le fichier php. Il suffit pour cela de renseigner l'adresse localhost (ou localhost:8888 selon votre système) directement dans vores navigateur.

- Documentation Php : Liste des fonctions et méthodes
http://php.net/manual/fr/indexes.functions.php
## Javascript
**- Qu'est ce que c'est ?**
* Le Javascript est un langage inventé en 1995 par Brendan Eich (ancien de Nestcape). C'est un langage de programmation du Web conçu pour rendre interactifs et dynamiques les sites Web, très simplistes auparavant. 
* Le Javascript est devenu de plus en plus populaire avec le Web 2.0, basé sur des pages riches et interactives, et les concepteurs Web ont optimisé la rapidité d'éxécution du code, jusqu'à en faire un langage très performant, notamment avec l'arrivée de la plate-forme [Node.js ](https://https://nodejs.org/en/)qui permet de coder des applications Web très rapides et [MongoDB](https://https://www.mongodb.com/fr) avec qui Javascript à pénétrer le monde des bases de données.
 
**- Configurer son environnement de travail**
* Certains sites web appelés "bac à sable" ou *sandbox* en anglais, permettent d'écrire du code HTML/CSS/JavaScript et de tester directement le code. Les plus connus sont : [JSFiddle](https://jsfiddle.net), [JS Bin](https://jsbin.com) ou encore [CodePen](https://codepen.io).

* Pour une utilisation plus avancée du JavaScript, il est tout de même conseillé de coder sur sa propre machine, avec un environnement de travail adapté, tels des IDE comme [Eclipse](https://www.eclipse.org/downloads/), [Webstorm](https://www.jetbrains.com/webstorm/) et [Visual Studio](https://msdn.microsoft.com/fr-fr/library/hh334522.aspx), ou sur de "simples" éditeurs de code comme [Sublime Text](https://www.sublimetext.com/), [Atom](https://atom.io) ou [Brackets](http://brackets.io/).

**- Premiers Pas en JavaScript**
* La syntaxe du Javascript n'est pas très complexe. Il s'agit d'une suite d'instructions séparés par un point-virgule ou un retour à la ligne.
![](https://i.imgur.com/Xe7kuSd.png)

* Les codes JavaScript sont insérés au moyen de la balise <script> </script>, et ce, dans le corps même du code HTML. Ils peuvent, par ailleurs, être écrits dans des fichiers externes (d'extension .js) et appelés ensuite par l'attribut src de l'élément <script>.
*ex* : <script src="VotreScript.js"></script>

**- Instructions Javascript basiques**
* [ Très bonne docu Javascript](https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference).


## REFERENCEMENT


Toute entreprise moderne, qui se respecte se veut etre visible sur la toile. C'est ainsi qu'on assiste à la prolifération des sites web au cours des dernières années et de divers métiers associés tels que le webDesign pour attirer les visiteurs. Dans une optique de générer toujours plus de trafic sur leurs sites web favoris, les webmasters se sont penchés sur une techniques qui permettra non seulement à un internaute de visiter un site donné en passant mais que celui-ci y revient très souvent voire s'y abonné: c'est la naissance du referencement dont l'objet capital est de rendre un site web donnée le plus visible possible sur Internet.

**Référencement VS Positionnement**

Qu'est-ce-que le referencement ?

Le referencement désigne l'action de conférer un index à un site ou une plateforme afin de l'inscrire dans la base de donnée d'un moteur de recherche tel que google. 
Mais l'on ne compte pas seulement être présents, mais aussi avoir une bonne place dans l'ordre de ces résultats pour que le site attire un maximum de visiteurs.

Ainsi le vrai terme pour désigner ce dont on vous parle ici est le terme 'Positionnement'. Mais pourquoi referencement ? Simplement parce-qu-il s'est vite imposé par abus et est devenu générique.


**Les techniques de référencement**

 Pour mieux référencier un site web il y a en gros deux grandes pistes qui sont le « white Hat » ou le « Black Hat ».
La premiére chose qui vient à l’esprit pour mieux positionner une page est de comprendre le fonctionnement d’un moteur de recherche et d’essayer de tromper les robots d’indexation en utilisant tous les moyens disponibles, quitte à courir le risque de voir son site retiré de l'index de Google ou d'un autre moteur de recherche. C'est le "Black hat".
Mais le probléme est que  ces algorithmes de classement sont constamment améliorés et changent tout le temps pour lutter contre ces sites web  qui cherchent à flouer les robots des moteurs pour faire remonter le site dans les résultats.
Donc ça sera beaucoup mieux de choisir la deuxième piste de « White Hat » et de concevoir un site agréable et pertinent pour l'utilisateur plutôt que de chercher à créer un site pour un robot d'indexation
Alors quelles sont les techniques à faire pour optmiser votre site?
Il y a différents techniques de référencement naturels :
   - il y a l’aspect externe ou ce qu’on appelle le Link Building càd d’avoir le maximum des liens qui pointent vers votre site. 
En fait Les liens de qualité de sites et blogs externes aident les moteurs de recherche à trouver votre site à comprendre la thématique de votre site et de vos pages. Plus vous obtiendrez de liens provenant de sites internet de qualité en relation avec votre thématique, mieux votre site se positionnera.
   - l'autre aspect est l’optimisation du contenu,parce que si votre site est intéressent google peut voir que les gens passe du temps sur votre site et ils continuent pas à chercher le meme sujet après qu’ils entrent le site. Alors le site répond aux besoins des utilisateurs et il sera mieux référencé par le moteur de recherche. Au-delà des moteurs de recherche, le fait d’avoir un contenu de qualité va encourager les autres site à vous mentionner en faisant des liens vers vous. 
En résumé le contenu doit etre :
     - Simple
     - à valeur ajouté
     - unique,  écartez donc tout action de plagiat consistant à copier-coller du texte trouvé sur un autre site internet parceque Les moteurs de recherche identifient aisément le plagiat à partir d’autres sites web. La conséquence est de vous retrouver pénalisé.
     - Concentrez-vous sur les mots-clés en relation direct à votre activité. Puis construisez une liste que vous utiliserez dans : 
         * les titres des pages de vos sites ( Indiquez vos mots-clés au niveau des balises de titre de vos textes en les hiérarchisant)  
        * les descriptions de vos pages (incorporer des mots clés dans la description des pages)
       * vos images (Utilisez vos mots-clés pour nommer les images que vous utilisez et également dans leurs balises < alt >)
       * et bien-sûr le contenu de vos pages.
     - Contenu mise à jour réguliérement vue que l’objectif des moteurs de recherche est de livrer une information de qualité récente et pertinente.
     - Créer un espace interactif pour vos internautes.

## Les sources:
-les différents techniques de référencement naturels: (https://www.youtube.com/watch?v=XdT9Gys_Ou4)
-les technique d'optimisation du contenu d'un site:
(http://larecetteduweb.fr/referencement-web/top-10-des-techniques-referencement-naturel/)
-Débuter en php : http://www.pierre-giraud.com/php-mysql/cours-complet/php-demarrer.php
-Fonctionnement d'un site internet écrit en php : https://openclassrooms.com/courses/concevez-votre-site-web-avec-php-et-mysql/fonctionnement-d-un-site-ecrit-en-php
-MDN web docs - Introduction au HTML (https://developer.mozilla.org/fr/Apprendre/HTML/Introduction%C3%A0HTML)
-Openclassrooms - Introduction au HTML (https://openclassrooms.com/courses/apprendre-asp-net-mvc/introduction-au-html)
-Openclassrooms - Premiers pas en JavaScript
https://openclassrooms.com/courses/dynamisez-vos-sites-web-avec-javascript/premiers-pas-en-javascript
-Openclassrooms - Apprendre à coder avec le JavaScript
https://openclassrooms.com/courses/apprenez-a-coder-avec-javascript
