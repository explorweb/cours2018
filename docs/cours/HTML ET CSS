# HTML ET CSS

## HTML

L'objectif de ce cours  est de permettre aux lecteurs , d'être capable de créer leur propre site web avec html, et de pouvoir apporter des modifications de mises en forme sur leur site pour le rendre plus jolie.

Le langage HTML est un langage structuré qui décrit un document grâce à des balises. Les balises sont des valeurs entourées de deux caractères, < et >, qui décrivent, à partir de paramètres propres à la balise appelés ‘attributs’, le contenu sémantique de la donnée.
### Structures de bases d'un page en HTML 
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
>* La structure de base d’une page en html5 est comme suit
> 
>![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/premier-fichier-html.png)

### Insérer un Lien
  * l’élément a (pour "anchor") serve à créer des liens vers d’autres sites ou d’autres pages, on aura besoin d’un attribut href ("hypertexte reference") qui va prendre comme valeur l'adresse (relative ou absolue) de la page vers laquelle on souhaite faire un lien. Comme dans l'exemple ci-dessous ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/element-a-exemple-html.png)
### Insérer une Image 
    * L’élément **img**, servant à insérer une image dans une page HTML, va lui demander deux attributs : src et alt.
     L'attribut **src** va prendre comme valeur le nom et            l’emplacement de l’image tandis que l'attribut **alt** va afficher un texte alternatif dans le cas où l’image ne serait pas disponible (pour les non voyants par         exemple).

     Notez que cet élément n'est constitué que d'une seule       balise orpheline.![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/element-img-exemple-html.png)
     
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

Source : [HTML-W3SCHOOLS](https://www.w3schools.com/html/)

## CSS
* Pour changer l'apparence de votre page web , voir la rendre plus jolie , on va devoir utiliser CSS.
* Pour appliquer un style à un élément HTML, nous allons devoir au préalable le **sélectionner** ou le **cibler**.
  * Les propriétés vont nous permettre de choisir quel(s) aspect(s) (ou "styles") d’un élément HTML on souhaite modifier.
  * Une propriété va être accompagnée d’une ou plusieurs valeurs qui vont définir le comportement de cette propriété.
  * Prenons un premier exemple, afin d’illustrer ce que nous venons de dire et de bien voir comment le CSS fonctionne.
      * ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/selecteur-propriete-css.png)
       Dans l’exemple ci-dessus, nous utilisons le sélecteur CSS simple **p** qui va cibler tous les paragraphes de notre page HTML.
      Ensuite, vous remarquez que nous utilisons deux           propriétés **color** (couleur) et **font-size** (taille de la police d'écriture) pour modifier nos paragraphes.
  * Pour faire une déclaration sur CSS avec n'importe quelles propriétés de html afin d'apporter des modifacations , il va falloir respecter la régle de déclaration comme dans l'exemple préccedent.
   * Rappel : Il faut écrire votre code CSS dans un fichier séparé portant l’extension  **.css**. C’est la méthode recommandée, qui sera utilisée autant que possible.
   * Les sélecteurs **#id** et **.class** vont nous permettre de cibler un élément en particulier plutôt qu’un type d’élément.
  * Nous allons tout simplement écrire nos attributs **id** et / ou **class** à l’intérieur de la balise ouvrante d’un élément HTML et leur attribuer une valeur.   
     
   * Comme dans l'exemple suivant ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/attributs-html-id-class.png)
        
       * Comme vous pouvez le voir ci-dessus, j’ai attribué un attribut id à mon premier paragraphe et un attribut class à mon deuxième paragraphe.
       * En effet, pour cibler un élément possédant un attribut id, en CSS, il faudra préciser la valeur de l’attribut précédée d’un dièse (#).

     * Pour cibler un élément possédant un attribut class, en revanche, il faudra en CSS préciser la valeur de l’attribut précédée d’un point (.).

      * Ainsi, on peut tout à fait donner la même valeur à un attribut class et id : il n’y a aucun risque de confusion en CSS si vous faites bien attention à bien faire précéder la valeur par le dièse ou le point. 
      * ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/selecteurs-css-id-class.png) 
      * Voilà comment votre page va afficher les modifications ![](https://i.imgur.com/nDGIQD1.png)
  * Le modèle des boîtes est un concept essentiel et central pour la mise en page d’une page web.Ce modèle nous dit que **tout élément HTML** peut être considéré comme une **boîte rectangulaire **, qu’il soit de type **block** ou **inline**.
  * Vous devez absolument comprendre le modèle des boîtes pour ensuite pouvoir **positionner** les différents éléments de votre page où vous le **souhaitez** et créer de belles pages web.
     * exemple:
     * ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/creation-div-modele-des-boites-css.png)
     * ![](http://www.pierre-giraud.com/html-css/cours-complet/imgs/illustration-modeles-boites-css.png)
     * ce qui s'affichera sur le site 
     * ![](https://i.imgur.com/uX42VP7.png)

* creer un menu sur css
* id et tag 



* Sources : 
[site web ](https://openclassrooms.com/courses/apprenez-a-creer-votre-site-web-avec-html5-et-css3)
* Pour aller plus loin , vous pouvez regarder le cours d'open classrooms sur [creer un site web](https://openclassrooms.com/courses/apprenez-a-creer-votre-site-web-avec-html5-et-css3)


