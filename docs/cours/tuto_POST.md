# Tutoriel de connexion à Moodle via Postman

## Prérequis :

* Ce tutoriel se déroulera avec Mozilla Firefox car on peut y afficher les requêtes HTTP.
* Vous devez avoir téléchargé au préalable le logiciel Postman et avoir créé un compte dessus.

---

## Etapes :

* Lorsque vous êtes sur Mozilla Firefox, appuyez sur la touche `f12` de votre clavier et vous verrez apparaître un bandeau en bas de votre écran.

![](https://i.imgur.com/PLRIufI.png)

* Sélectionnez ensuite l'onglet `Réseau` sur le bandeau pour voir apparaître les requêtes HTTP de votre page.

![](https://i.imgur.com/fc1O4lV.png)

* Connectez vous alors sur l'espace Moodle avec vos identifiants et vous verrez alors des requêtes s'afficher.

![](https://i.imgur.com/JI7A0X1.png)

* La requête qui a permis la connexion est celle utilisant la méthode `POST`, les deux autres ne sont que les requêtes d'affichage de la page. Cliquez alors sur la flèche située sur la droite du bandeau, comme indiqué ci-dessous, pour afficher les détails de la requête.

![](https://i.imgur.com/YI1Byf8.png)

* Vous pouvez alors récupérer l'URL de l'entête et la rentrer dans Postman, en indiquant une méthode `POST`.

![](https://i.imgur.com/Rcm1i4G.png)

* Ensuite, dans l'onglet `Paramètres` du bandeau des requêtes HTTP, vous pouvez constater la présence de deux entités : `username` et `password`, qui correspondent à vos identifiants de connexion.

![](https://i.imgur.com/lvY589W.png)

* Dand l'onglet `Body` de Postman, sélectionnez `x-www-form-urlencoded` et rentrez ensuite les paramètres `username` et `password` avec comme valeurs vos identifiants.

![](https://i.imgur.com/GXEGd3n.png)

* Appuyez ensuite sur le bouton `SEND` et votre page MOODLE s'affichera en HTML en bas de l'écran, vous pouvez vérifier que la connexion a bien fonctionné en voyant affiché `TELECOM Bretagne : Ma page`.

![](https://i.imgur.com/gzHqHtM.png)

* Bravo, vous avez envoyé votre première requête `POST` à l'aide de Postman :horse:
