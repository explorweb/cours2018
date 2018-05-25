# Diaporama en JavaScript

**Prérequis : [Bases HTML/CSS](A COMPLETER UNE FOIS LE COURS SUR LES BASES POSTÉES), Programation Orienté Objet**

**INTRODUCTION**

Le langage JavaScript est un langage de programmation orienté objet, interprété (pas besoin de compilateur pour l'exécuter) et se présentant sous la forme de script (morceau de code) inséré dans du code HTML afin d'élargir le spectre de possibilité étroit que présente un site web basique (codé uniquement avec du HTML et CSS).
Ce cours se veut très pratique c'est-à-dire qu'il vous permettra de découvrir le langage Javascript au travers d'un fil rouge intitulé "Conception d'une diapo pour animer un site web " où nous allons voir comment concevoir un diaporama avec défilement automatique pour un site web.

Le principe de ce cours est plus proche de ce que l'on vit en pratique que d'un cours classique. En effet nous avons récupéré un [code existant](https://codepen.io/bradtraversy/pen/boydaE) créé par Brad Traversy dont la vidéo d'explication (en anglais) est disponible [ici](https://www.youtube.com/watch?v=7ZO2RTMNSAY). Ensuite nous l'avons adaptés pour obtenir ce que nous souhaitions. Nous allons donc vous présenter ici les différentes étapes d'adaptation du code récupéré.

**Partie HTML**


## HTML
![](https://i.imgur.com/PRoX2Py.png)


Ce code est du HTML(HyperText Markup Language) et il peut sembler incompréhensible pour un débutant en programmation .... Mais on a choisi ce code parce qu'il utilise que deux types de balises **div et span**. Ça nous permettra de ne pas trop nous disperser dans le monde HTML. 
Alors certains malins diront "Oui mais c'est quoi des balises déjà ?". Une balise est le conteneur qui permet d'écrire du code HTML, elle délimite une instruction ou un bloc d'instructions. C'est comme les points virgules (en fin d'une ligne d'instruction) en Java ou en C. Alors maintenant on peut s'interesser à notre code HTML ci-dessus.
Comme je l'ai dit plus haut, une balise est un conteneur alors à chaque fois qu'on l'ouvre, il est nécessaire de la refermer. 

-- Balise **div**
L'élément HTML < div > (qui signifie division du document) est un conteneur générique qui permet d'organiser le contenu sans représenter rien de particulier. Dans notre cas, il est utilisé afin de grouper d'autres éléments pour leur appliquer un style en utilisant les attributs class ou id. Parlant d'attributs, à quoi servent **id** et **class**?
Premièrement on les utilise pour appliquer des styles CSS(vous saurez ce que c'est plus tard) aux éléments d'une page HTML mais un **id** s'applique à un élément unique (il ne peut pas y avoir deux mêmes id dans une page) tandis qu'une classe peut caractériser plusieurs objets identiques ou non. Plus concrêtement on peut avoir
```<div class="toto"></div>```
```<div class="toto"></div>``` 
mais il ne peut pas y avoir 
```<div id="tata"></div>```
```<div id="tata"></div>```
On peut bien sûr définir autant d'**id** que l'on veut dans la feuille de style(CSS), mais il faut qu'ils soient uniques dans la page html. L'**id** peut servir d'ancre, c'est à dire qu'il permet d'indexer une partie du code dans le fichier CSS (encore une fois vous inquitez pas, vous saurez ce que c'est plus tard). Alors revenons à notre code où il y a ```<div id="slider"></div>``` comme vous l'aurez compris pour les plus malins, on crée juste un "slider" (diapositive ou curseur en français pour les non bilingues) pour contenir nos différentes images et qui sera défini dans le CSS plus tard. À l'intérieur de ce **id**, on utilise l'attribut **class** (aussi un sélecteur CSS) afin de définir des conteneurs pour nos images 1,2 et 3. Ici on en définit deux : 
```<div class="slide slide1">```
```<div class="slide-content">```
Et comme l'attribut **id**, il va falloir définir ces classes dans le fichier CSS. Une dernière chose sur ces attributs, pour faire référence à un **id** en CSS, il faut faire **#nom_id** et pour l'attribut **class**, il faut faire **.nom_classe**.

-- Balise **span**
Cette balise vous offre une ligne vide (à remplir), ça veut dire que vous pouvez écrire ce que vous voulez mais cette chaine de caratère doit être comprise en une ligne. Ici dans notre diaporama, on s'en sert pour ranger les images par ordre (ce n'est pas néessaire on peut les supprimer). On mettra donc ```<span>1</span>``` pour indiquer qu'il s'agit l'image 1. 

On ajoutera```<span>2</span>``` pour l'image 2 ainsi que  ```<span>3</span>``` pour l'image 3.
Vous pouvez remarquer que dans le [code d'origine](https://codepen.io/bradtraversy/pen/boydaE), le developpeur a plutôt utilisé ces balises en écrivant ```<span>Image One</span>```, ```<span>Image Two</span>``` et ```<span>Image Three</span>``` pour nommer ses images.

> **A vous de jouer**
> * Ouvrez un nouveaux document sur [Codepen](https://codepen.io).
> * Créez autant de briques élémentaire que vous voulez de photos dans votre diaporama.
## CSS

On aura aussi besoin d'un code écrit en CSS(Cascading Style Sheets). Il faut retenir que ce langage vient en support au HTML. C'est un fichier(.css) qu'on lie au code HTML. Il permet de faire la mise en forme de la page HTML qui n'est autre que du texte écrit sur page blanche. Ses fonctions permettent d'éditer la couleur, la police des lettres, la largeur ou la hauteur d'un block, la marge... Vous l'avez compris certainement, le HTML c'est un bloc note (pour les fans de Windows) et muni du CSS il devient une slide powerpoint avec des couleurs et un meilleur visuel.

#### Le format des diapositives :
![](https://i.imgur.com/lgrvItB.png)

Ce bloc sert à définir le format des diapositives (marges, hauteur, largeur, police ...).

> **A vous de jouer**
> * Recopiez ce code sur CodePen.
> * Dans le code complet disponible [ici](https://codepen.io/fati-h/pen/mLZRVg) amusez vous à faire des tests pour que le format vous plaise.

#### L'affichage des photos

![](https://i.imgur.com/JGKr4Px.png)

Ce bloc sert à chosir comment on veut que nos images s'affichent (redimentionnement, placement ...)


> **A vous de jouer**
> * Recopiez ce code sur CodePen.
> * Dans le code complet disponible [ici](https://codepen.io/fati-h/pen/mLZRVg) amusez vous à faire des tests pour que le format vous plaise. Par exemple essayez ```contain``` à la place de ```cover``` pour afficher l'image en entier.

#### Le choix des images

![](https://i.imgur.com/t76Hxsu.png)
 
 Il est nécessaire de dupliquer ce bloque autant de fois que vous avez de photos. Faites attention à ce que le nom (ici ```.slider1```) corresponde avec le nom de classe donné dans le code HTML !

> **A vous de jouer**
> * Dupliquez ce bloc autant de fois que vous en avez besoin (attention au noms !).
> * Modifier l'url par celle de la photo que vous désirez afficher(vous pouvez utiliser [pexels](https://www.pexels.com/))

#### Le texte sur les images

![](https://i.imgur.com/mewIjfI.png)

Ces dernier blocs servent à définir le positionnement ainsi que la couleur du texte écrit entre les balises ```<span>```.
Ces derniers blocs ne sont pas nécessaire si vous ne voulez pas afficher de texte chacune de vos diapositive.


> **A vous de jouer**
> Encore une fois, prenez le code en main modifiez le pour obtenir un visuel qui vous plait.


---
> *Pour aller plus loin* : Vous pouvez trouver plus  de fonctions CSS, leur utilité et comment les utilisé sur [W3schools](https://www.w3schools.com/Css/css_margin.asp)

## JavaScript
![](https://i.imgur.com/WS3SIjS.png)

Comme vous pouvez le constater, le code Javascript comporte essentiellement 4 fonctions utiles pour atteindre notre but. 
D'abord après avoir recupéré les images à faire défiler dans **sliderImage** et initialisé les variables **current** et **timeToPass** respectivement pour le stockage de la position (index) de l'image courante dans **sliderImage** et pour le stockage de la durée d'affichage d'une image avant de paser à la suivante (ici 4000 millisecondes). La fonction **reset()** est définie pour la réinitialisation en empêchant l'affichage des images avec la valeur ***block*** donnée à l'attribut **display** de **style** de **sliderImage**. 
Ensuite la fonction **startSlide()** permet d'initialiser le diaporama en affichant la 1ere image de la diapo avec le mot clé **block** après avoir initialisé à l'aide de **reset()**.
La fonction **slideRight()** joue le rôle clé de passer dans le diaporma à une image suivante (**current + 1**) où **current** désigne la position de l'image courante (compteur dans **sliderImage**). Et à la fin de la fonction on vérifie si on est à la dernière image. Si oui, on le réinitialise **current** à -1 afin que le prochain appel d'affichage soit **sliderImage[0]** pour réafficher la 1ere image.

On démarre le diaporama à l'aide de **startSlide()**.
                   
Enfin, à l'aide de la fonction **setInterval()** on exécute **slideRight** toute les **timeToPass** milisecondes. 
Donc dans notre cas on change d'image toutes les 4 secondes.

> **A vous de jouer**
> * Récuperez ce code JavaScript et définissez le temps de transition qui vous convient.
> * *Pour aller plus loin* : essayez de définir des transitions. Pour vous aidez vous pouvez aller voir le blog de [Louisitit](https://www.louistiti.fr/tutoriel-video-javascript-css3-creation-diaporama/46) en autres.
