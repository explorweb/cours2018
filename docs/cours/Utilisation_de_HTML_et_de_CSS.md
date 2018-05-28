# Utilisation de HTML ET de CSS

## HTML

L'objectif de ce cours  est de permettre aux lecteurs , d'être capable de créer leur propre site web avec HTML, et de pouvoir apporter des modifications de mises en forme sur leur site pour le rendre plus jolie à l'aide de CSS.

Le langage HTML est un langage structuré qui décrit un document grâce à des balises. Les balises sont des valeurs entourées de deux caractères, < et >, qui décrivent, à partir de paramètres propres à la balise appelés ‘attributs’, le contenu sémantique de la donnée.

Afin de vous guider dans l'élaboration, pour certains de votre première page web, nous allons vous présenter les notions structurantes de HTML et de CSS, plutôt que de vous donner un catalogue de balises dans lequel vous iriez piochez pour réaliser votre site.
### Structures de bases d'un page en HTML 

En guise d'introduction, voici un rappel de la structure de toutes les pages html. Elles se présentent toutes sous la même forme.
> * `<!DOCTYPE html>`
Tous les documents HTML doivent commencer par une déclaration de type de document: `<!DOCTYPE html>`.
> * `<html>` et `</html>`
Le document HTML lui-même commence par `<html>` et se termine par `</html>`.
> * `<head>` et `</head>`
Le titre du site web est entre `<head>` et `</head>`.
> * `<body>` et `</body>`
La partie visible du document HTML est entre `<body>` et `</body>`.
> * En-têtes HTML
> Les en-têtes HTML sont définis avec les balises `<h1>` à `<h6>`. `<h1>` définit l'en-tête le plus important. `<h6>` définit l'en-tête le moins important.
> * `<p>` et `</p>`
> Les paragraphes HTML sont définis avec la balise `<p>`.
>
La structure de base d’une page en html5 se présente ainsi sous cette forme :
> 
>![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/premier-fichier-html.png)
>

### Titre de votre page web

* Le plus important avant de créer votre page html est de lui donner un titre, qui sera affiché dans votre onglet et qui permettra de vous trouvez sur les différents moteurs de recherche. C'est l'objectif de la balise "title" que vous trouvez sur l'image précédente. Choisissez donc un titre qui permettra de décrire de la manière la plus fidèle le contenu de votre page html.

* Après cette première étape, qui permettra aux utilisateurs de trouver votre page html, il est nécessaire de donner un titre qui apparaîtra directement sur la page html et non plus dans l'onglet. Cette tâche est réalisée par la balise "h1".
* Pour informations, il existe d'autres balises, numérotées de "h2" à "h6" permettant d'ajouter des sous titres.

### Insérer du texte

* Autre notion indispensable à savoir maîtriser : l'insertion de texte. La manière la plus simple est d'ajouter petit à petit des paragraphes, entourés de la balise "p". De cette manière, vous allez pouvoir, de façon très simple ajouter du contenu à votre première page web.


### Insérer une Image

* L’élément **img**, servant à insérer une image dans une page HTML, va avoir besoin de deux attributs : src et alt.
* L'attribut **src** va prendre comme valeur le nom et            l’emplacement de l’image tandis que l'attribut **alt** va afficher un texte alternatif dans le cas où l’image ne serait pas disponible.
* Notez que cet élément n'est constitué que d'une seule       balise orpheline.![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/element-img-exemple-html.png)

### Insérer un Lien
  * L’élément "a" (pour "anchor") sert à créer des liens vers d’autres sites ou d’autres pages. Pour ce faire, nous aurons besoin d’un attribut href ("hypertexte reference") qui va prendre comme valeur l'adresse (relative ou absolue) de la page vers laquelle on souhaite se diriger. Voci un exemple :![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/element-a-exemple-html.png)
  * Remarque : Vous pouvez également créer un lien vers une autre page html que vous allez créer en mettant, à la place de l'url de la page web, le nom d'un autre fichier html sur lequel vous voulez vous diriger.

Les  deux prochaines parties s'adressent aux personnes qui auront finis le TP en moins d'une heure et qui voudront continuer à personnaliser leur site.
### Insérer un tableau

Le tableau est défini par les balises `<table>` et `</table>`.

`<tr>` formate une ligne dans un tableau et nécessite un marqueur de fin.

`<td>` formate une colonne dans un tableau et nécessite un marqueur de fin.

Les informations entre les balises `<tr>` `</tr>` et `<td>` `</td>` sont les contenus de tableau. 

> Exemple
    
    <table>
        <tr>
            <td>row 1, cell 1</td>
            <td>row 1, cell 2</td>
        </tr>
        <tr>
            <td>row 2, cell 1</td>
            <td>row 2, cell 2</td>
        </tr>
    </table>

<table>
    <tr>
        <td>row 1, cell 1</td>
        <td>row 1, cell 2</td>
    </tr>
    <tr>
        <td>row 2, cell 1</td>
        <td>row 2, cell 2</td>
    </tr>
</table>


### Insérer un formulaire

Toute page HTML peut être enrichie de formulaires interactifs, qui invitent vos visiteurs à renseigner des informations : saisir du texte, sélectionner des options, valider avec un bouton.

`<form>` et `</form>` sont les balises principales du formulaire, elles permettent d'en indiquer le début et la fin.
> Le texte

    <form>
    First name: <input type="text" name="firstname"><br>
    Last name: <input type="text" name="lastname">
    </form>

>Les mots de passe
    
    <form>
    Password: <input type="password" name="pwd">
    </form>
    
>La sélection unique des options

    <form>
    <input type="radio" name="sex" value="male">Male<br>
    <input type="radio" name="sex" value="female">Female
    </form>
    
>La sélection multiple des options

    <form>
    <input type="checkbox" name="vehicle" value="Bike">I have a bike<br>
    <input type="checkbox" name="vehicle" value="Car">I have a car 
    </form>
    
>Le bouton envoyé 

    <form name="input" action="html_form_action.php" method="get">
    Username: <input type="text" name="user">
    <input type="submit" value="Submit">
    </form>

### Conclusion :
* Nous vous avons détaillé les premières notions structurantes d'HTML, qu'il est nécessaire de savoir maîtriser si l'on veut écrire une page HTML. A ce stade, vous devriez être capable d'ajouter un titre, des images, des paragraphes à votre page et ainsi, faire émerger du contenu. Sachez toutefois que nous ne vous avons présenté que les bases et qu'il existe bien d'autres fonctionnalités avec HTML, afin de créer par exemples des tableaux ou bien encore des formulaires.

Source : [HTML-W3SCHOOLS](https://www.w3schools.com/html/)

## CSS
* A la suite de la première partie, vous avez dû vous rendre compte que votre page html est peu attrayante. Pour changer l'apparence de votre page web , voir la rendre plus jolie , on va devoir utiliser CSS. Pour ce faire, il faut écrire votre code CSS dans un fichier séparé portant l’extension  **.css**. C’est la méthode recommandée, qui sera utilisée autant que possible. Voici comment est modifié le code html, afin de le faire fonctionner avec un ficher CSS : ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/attributs-html-id-class.png)
* Pour appliquer un style à un élément HTML, nous allons devoir au préalable le **sélectionner** ou le **cibler**.
  * Les propriétés vont nous permettre de choisir quel(s) aspect(s) (ou "styles") d’un élément HTML on souhaite modifier.
  * Une propriété va être accompagnée d’une ou plusieurs valeurs qui vont définir le comportement de cette propriété.
  * Prenons un premier exemple, afin d’illustrer ce que nous venons de dire et de bien voir comment le CSS fonctionne.
       ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/selecteur-propriete-css.png)
       * Rappelez vous de la balise "p" utilisée en HTML. Elle sert à insérer des paragraphes à notre page. Dans l’exemple ci-dessus, nous utilisons le sélecteur CSS simple **p** qui va cibler tous les paragraphes de notre page HTML. 
      *  Ensuite, vous remarquez que nous utilisons deux           propriétés **color** (couleur) et **font-size** (taille de la police d'écriture) pour modifier nos paragraphes. Ca y est vous avez personnaliser votre page web !
  * Pour faire une déclaration sur CSS avec n'importe quelles propriétés de html afin d'apporter des modifications , il va falloir respecter la régle de déclaration comme dans l'exemple précédent.
   * Les sélecteurs **#id** et **.class** vont nous permettre de cibler un élément en particulier plutôt qu’un type d’élément et ainsi nous donner la possibilité de ne modifier qu'une partie de notre page web plutôt que la page dans son ensemble.
  * Nous allons tout simplement écrire nos attributs **id** et / ou **class** à l’intérieur de la balise ouvrante d’un élément HTML et leur attribuer une valeur.   
     
   * Comme dans l'exemple suivant ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/attributs-html-id-class.png)
        
       * Comme vous pouvez le voir ci-dessus, nous avons attribué un attribut id à notre premier paragraphe et un attribut class à notre deuxième paragraphe.

     * Pour cibler un élément possédant un attribut class, il faudra en CSS préciser la valeur de l’attribut précédée d’un point (.). Exemple avec les balises "p", "body", etc...

     * Pour cibler un élément possédant un attribut id, il faudra en CSS préciser la valeur de l’attribut précédée d’un #.
      * ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/selecteurs-css-id-class.png) 
      * Voilà comment votre page va afficher les modifications ![](https://i.imgur.com/nDGIQD1.png)

### Créer un menu :
* A présent, après avoir présenté de façon générale l'utilisation de CSS, nous allons nous en servir pour rendre votre page html plus agréable et plus fonctioUn point. Ainsi, pour faciliter la navigation des utilisateurs sur votre page, il est essentiel de créer un menu. Pour ce faire nous allons considérer le menu de navigation comme une liste de liens. La première étape consiste donc à rajouter cette liste de liens dans votre code html.
* Par exemple, pour un menu comportant 5 items pouvant être utilisé pour un site d'association sportive, vous aurez une liste de ce genre, placée dans la partie "body", avec le nom de la page web vers laquelle vous voulez être redirigée à la place du "#" et le nom qui sera affiché sur votre page html, à la place de "item1":
 ![](https://image.noelshack.com/fichiers/2018/22/1/1527493331-capture2.png)
       
* Toutefois, comme vous l'aurez sans doute remarquez, vous n'avez écris que du code html. Copier ce code suivant  sur votre éditeur de texte, et vous verrez de quelle manière cette liste va se transformer en un menuen jouant sur la couleur de fond, la marge , la bordure etc....
  ![](https://i.imgur.com/a0AYfIK.png)
  
* Dernière étape pour commencer à créer un site web, insérer une image en arrière plan. Pour ce faire, il existe différentes manières. Nous allons vous en présenter ne qui n'utilise que du code CSS :
    ![](https://image.noelshack.com/fichiers/2018/22/1/1527493912-capture3.png)
    Ici, nous allons mettre l'image "sports" en arrière plan, qui ne sera répétée qu'une seule fois et nous allons laisser le navigateur gérer de façon autonome, la taille de l'image. Comme vous pouvez vous en douter, il existe une multitude d'autres options que nous ne détaillerons pas au sein de cours.
    
* Enfin, pour ceux qui veulent aller plus loin le modèle des boîtes est un concept essentiel et central pour la mise en page d’une page web. Ce modèle nous dit que **tout élément HTML** peut être considéré comme une **boîte rectangulaire **, qu’il soit de type **block** ou **inline**.
  * Vous devez absolument comprendre le modèle des boîtes pour ensuite pouvoir **positionner** les différents éléments de votre page où vous le **souhaitez** et créer de belles pages web. Mais cela dépsse le cadre d'un premier TP d'une heure mais devra être intégrer pour continuer à améliorer sa page web.
     * exemple:
     * ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/creation-div-modele-des-boites-css.png)
     * ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/illustration-modeles-boites-css.png)
     * ce qui s'affichera sur le site 
     * ![](https://i.imgur.com/uX42VP7.png)

  
  
### Conclusion

* Nous vous avons présenter les différentes notions structurantes dans la création d'une page html, rendue plus agréable avec l'utilisation de CSS. Bien entendu, nous n'avons présenté que quelques fonctionnalités et options que permettent HTML et CSS, mais qui vous permettront de comprendre comment est coder une page web.

### Sources : 
[Site web](https://openclassrooms.com/courses/apprenez-a-creer-votre-site-web-avec-html5-et-css3)
[Menu ](https://www.alsacreations.com/tuto/lire/574-Creer-des-menus-simples-en-CSS.html)
[Cours html/css](http://www.pierre-giraud.com/html-css/cours-complet/cours-html-css-presentation.php)






