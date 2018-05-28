# **Formulaire Javascript : Site d'objets perdus**
*Auteurs: Jie Song, Samar MAMI, Thabet CHAAOURI, Youssef FEHRI*

#  *Introduction*

Danc ce cours, nous allons traiter en première partie comment écrire un formulaire en HTML puis en deuxième partie nous allons étudier l'interaction avec l'utilisateur grâce aux nombreuses propriétés et méthodes dont sont dotés les éléments HTML utilisés dans les formulaires.


# *Plan du cours*

>1. Ecrire un formulaire en HTML

  1.1. Html pour les texts
  
  1.2. Html pour la date
  
  1.3. Html pour le choix
  
  1.4. Html pour le téléchargement
  
  1.5. Html pour le choix multiple
  
>2. Traitement de la saisie: Propriétés et méthodes du formulaire

   2.1. Entrée d'une valeur au clavier
  
   2.2. Valider un champ du formulaire 
  
   2.3. Choix d'une case
  
   2.4. Listes déroulantes
   
   2.5. Ajouter, insérer et supprimer des lignes dans une liste
  
   2.6. Soumettre un formulaire
  
   2.7. Réinitialiser un formulaire
  
   2.8. Donner ou retier le focus
  
  >3. CSS
  
  3.1. Petits rappels
  
  3.2. Modifier les éléments CSS en Javascript
  
>4. Exemple (TP openclassroom)

# *Partie I. Ecrire un formulaire en HTML*

Pour bien enregistrer les données concernant un objet perdu, nous listons les composants nécessaires au formulaire:
* Tout d’abord, l’utilisateur écrit un titre qu’est bref et clair pour décrire l’objet trouvé;
* La date de cet objet trouvé;
* Le lieu d’où il a trouvé l'objet; 
* La couleur de l'objet pour qu'il soit plus facile de filtrer;
* La manière de contacter;
* Autres remarques à ajouter si nécessaires.

Selon les attributs des  différents composants, html nous offre plusieurs elements à utiliser:
***1.1. Html pour les texts***

Pour laisser l'espace blanc pour mettre les texts, ` <input type='text'>` peut le faire en utilisant `value` et `onfocus`  pour la phrase de guide et ` size` pour limiter la taille. 
![](https://i.imgur.com/1RuHsaW.png)

***1.2. Html pour la date***

Pour choisir une date dans le calendrier, `<input type='date'>` support de prendre le calendrier et faire le choix:
![](https://i.imgur.com/snUtjsN.png)

***1.3. Html pour le choix***

Pour faire la liste et choisir un element `<select>`,` </select>` est un choix:
![](https://i.imgur.com/9hddmWO.png)

***1.4. Html pour le téléchargement***

Pour télécharger les images de l'objet perdu et faire un apperçu, on peut utiliser `<input type="file">` pour permettre le téléchargement et le boutton `<input type="button">`  et l'activité associé avec le button `onclick="nom_fonction()"`. Quand on clique sur le button, la fonction qui permet faire l'aperçu des photos va être activé.

![](https://i.imgur.com/BJEoD8U.png)

***1.5. Html pour le choix multiple***

Pour enregistrer les couleurs de ce objet qui peuvent servir à faire un mieux filitre de la cherche, on peut utiliser 
`<input type="checkbox" onclick="selectSingle()">`. 
![](https://i.imgur.com/uoycCrU.png)

# *Partie II. Traitement de la saisie: Les propriétés du formulaire*

Pour pouvoir utiliser les formulaires, il faut comprendre quelques propriétés de celui-ci.
Dans les formulaires comme pour le HTML, on peut accéder à n'importe quelle propriété en saisissant son nom comme pour les propriétés "value", "disabled", "checked", etc.
Nous allons traiter dans le paragraphe qui suit quelques propriétés de base du formulaire.

***2.1. Propriété 1 : "Value"***
* Cette propriété permet de définir une valeur pour différents éléments d'un formulaire comme les<input>, les<button>, etc. 
* Son fonctionnement: assigner une valeur (une chaîne de caractères) qui sera immédiatement affichée sur l'élément HTML.
* **Exemple:** Afficher le contenu d'une valeur entrée au clavier
 *Code de l'exemple:*
 
***-Saisir le texte au clavier***
><input id=**"text"** type=**"text"** size="60" value="Vous n'avez pas le focus !" />

***-Afficher le texte entré au clavier***
```<script>
     var text = document.getElementById('text');
   
     text.addEventListener('focus', function(e) {
         e.target.value = "Vous avez le focus !";
     });
 
     text.addEventListener('blur', function(e) {
         e.target.value = "Vous n'avez pas le focus !";
     });
</script>
```
***2.2. Propriété 2: "Valider un formulaire" (Contrôle de saisie)***
* Il est souvent très utile de vérifier la saisie d'un formulaire avant de le valider. Par exemple: la saisie d'un nom ne doit pas comporter un chiffre, la saisie d'une adresse mail doit être du type: "------@----.- --" ,etc.

* L'idéal est de créer un bouton qui appelle une fonction javascript qui contrôle la saisie et soumet ou non le formulaire.

* **Exemple:** saisie d'une adresse mail
*Code de l'exemple:*
```
<script type="text/javascript">
     function ValiderMail(formulaire) {
        if (formulaire.mail.value.indexOf("@",0)<0) 
        {alert("Adresse mail saisie invalide.\n
        Le formulaire ne sera pas validé.")}
        else {
           alert("formulaire validé.\nPour valider un formulaire : formulaire.submit()");
           // Pour valider le formulaire en javascript :
           // formulaire.submit()
        }
     }
</script>
```
***2.3. Propriété 3: "Checked" (cocher une case)***
* Cette propriété permet de choisir une case parmis un ensemble de cases proposées.
* **Exemple:** Choisir un nombre parmis 4 choix
*Code de l'exemple:*
***-Première étape: définir les choix proposées***
```
<label><input type="radio" name="check" value="1" /> 10</label><br />
<label><input type="radio" name="check" value="2" /> 11</label><br />
<label><input type="radio" name="check" value="3" /> 12</label><br />
<label><input type="radio" name="check" value="4" /> 13</label><br />
```
***-Afficher la case cochée***

> <input type="button" value="Afficher la case cochée" onclick="check();" />
***-Choix à effectuer selon la case cochée***
```
<script>
     function check() {
         var inputs = document.getElementsByTagName('input'),
             inputsLength = inputs.length;
 
         for (var i = 0; i < inputsLength; i++) {
             if (inputs[i].type === 'radio' && inputs[i].checked) {
                 alert('La case cochée est la n°' + inputs[i].value);
             }
         }
     }
</script>
```
***2.4. Propriété 4: "SelectedIndex+options" (Les listes déroulantes)***
Les listes déroulantes comme les boutons radio possèdent des propriétés bien spécifiques.
Parmis ces propriétés on cite: 
* La propriété "selectedIndex" qui nous retourne l'index (l'identifiant) de la valeur sélectionnée dans une liste de valeurs donnée.
* La propriété "options" qui liste les différents éléments qui composent la liste déroulante.

* **Exemple:** Choisir son sexe (Homme ou Femme)
*Code de l'exemple:*
***-Afficher la liste déroulante (les options possibles)***
```
<select id="list">
     <option>Sélectionnez votre sexe</option>
     <option>Homme</option>  
     <option>Femme</option>
 </select>
 ```
***-Afficher le contenu de la valeur choisie***
```
<script>
     var list = document.getElementById('list');
 
     list.addEventListener('change', function() {
 
         // On affiche le contenu de l'élément <option> ciblé par la propriété selectedIndex
         alert(list.options[list.selectedIndex].innerHTML);
 
     });
</script>
```

***2.5. Propriété 5:  Ajouter, insérer et supprimer des lignes dans une liste***
* Ce script permet d'ajouter dynamiquement des éléments dans une liste, sans rechargement de la page.
* **Exemple:** Ajouter une formation ou une expérience dans un formulaire de candidature à un stage

***2.6. Méthode 1: Submit (Soumettre/Envoyer le formulaire)***
* Les formulaires ne possèdent pas uniquement des propriétés, ils possèdent également des méthodes. L'une des méthodes les plus connues est la méthode submit()
* Cette méthode permet d'envoyer ou de soumettre un formulaire sans l'intervention de l'utilisateur.
* **Code de l'exemple:** assez simple

```
  var element = document.getElementById('un_id_de_formulaire');
  element.submit(); // Le formulaire est expédié
```
***2.7. Méthode 2: Reset (Réinitialiser le formulaire)***
* Cette méthode permet de réinitialiser tous les champs d'un formulaire.
* **Code de l'exemple:** assez simple

```
 var element = document.getElementById('un_id_de_formulaire');
 
 element.reset();  // Le formulaire est réinitialisé
``` 

***2.8. Méthode 3: Focus/Blur (Donner ou retirer le focus)***
* Les méthodes Focus() et Blur() permettent respectivement de donner ou de retirer le focus à un champ, c'est à dire pointer le curseur dans le champ souhaité ou le retirer.
* **Code de l'exemple:** assez simple
***-Définir le texte à saisir au clavier***
```
<input id="text" type="text" value="Entrez un texte" />
```
***-Donner le focus***
``` 
<input type="button" value="Donner le focus" onclick="document.getElementById('text').focus();" />
```

***-Retirer le focus***
```
<input type="button" value="Retirer le focus" onclick="document.getElementById('text').blur();" />
```

# *Partie III. Manipuler le CSS*

***3.1. Petits rappels***
* CSS est l'abréviation de Cascading Style Sheets, et il permet d'éditer graphiquement les éléments HTML (ou XML).
* On peut modifier la propriété d'un seul élément en l'indiquant directement dans la balise de cet élément. 
ex: 
```
<div style="color:red;"> Ici on modifie la couleur du texte en rouge.</div> 
```
* On peut par ailleurs éditer la feuille de style entièrement. ex 
```
div {color : red}; 
``` 
Ici on modifie la couleur de texte de tous les éléments div en rouge.
* Priorité : Les propriétés CSS de l'attribut sont prioritaires sur ceux d'une feuille de style. ex : 

```
<style> div {color:red;}
</style>
<div style="color:blue;"> Ici, le texte est bleu </div>
```




***3.2 Modifier les éléments CSS en Javascript***
* On modifie les propriétés d'un élément CSS en modifiant l'attribut correspondant (attention aux noms composés, Javascript n'accepte pas le tiret : background-color devient backgroundColor). ex:

```
<script>element.style.backgroundColor = 'blue'; 
</script>
```
* En lecture, un problème se pose : Si on a modifié les propriétés CSS en éditant la feuille de style et non l'attribut style, on ne peut pas accéder directement en lecture. 
* Il faut utiliser dans ce cas la fonction getComputedStyle() qui récupère n'importe quel style CSS. Déclaré via l'attribut Style, via une feuille de style ou même généré automatiquement, la fonction se chargera de récupérer l'information (en lecture seule).
* Pour Plus de détails concernant la manipulation du CSS avec Javascript, je vous renvoie à [ce cours](https://openclassrooms.com/courses/dynamisez-vos-sites-web-avec-javascript/manipuler-le-css)

# *Partie V. Exemple (TP openclassroom)*

Pour mettre en oeuvre ces acquis, on vous invite à faire le [TP de Openclasrooms](https://openclassrooms.com/courses/dynamisez-vos-sites-web-avec-javascript/tp-un-formulaire-interactif-1)

***Ressouces:***
* [Cours "Formulaires avec JavaScript" de OpenClassrooms](https://openclassrooms.com/courses/dynamisez-vos-sites-web-avec-javascript/les-formulaires-1)
* [Cours "les formulaires en JavaScript" de Tout JavaScript](http://www.toutjavascript.com/savoir/savoir06_3.php3)
