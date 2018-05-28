
# Faire une requête HTTP avec Postman

Lorsque vous faîtes une recherche sur internet en tapant une adresse du type http://..., c'est HTTP qui est utilisé pour traduire les requêtes nécessaires à l'affichage des pages que vous voyez dans votre navigateur, à l'envoi des données que vous avez remplies dans un formulaire sur internet, ...

Mais comment cela marche-t-il ? Et tout d'abord, qu'est réellement HTTP ?

### Qu'est-ce que HTTP ?

Le Hypertext Transfer Protocol, plus connu sous l'abréviation HTTP, littéralement le « protocole de transfert hypertexte », est un protocole de communication client-serveur développé pour le World Wide Web. Il est utilisé pour échanger toute sorte de données entre client HTTP et serveur HTTP.

###### Source : [Wikipédia](https://fr.wikipedia.org/wiki/Hypertext_Transfer_Protocol)

![](https://user.oc-static.com/files/5001_6000/5675.jpg)

Sur le schéma ci-dessus , les requêtes http sont représentées par les flèches bleue et verte

---

### Les requêtes HTTP



#### Syntaxe générale

Voici le schéma global d'une requête client : 
```
Méthode ; URL ; Version de protocole
Entête de requête
<nouvelle ligne>
Corps de la commande
```

##### Les types de méthode
Voici toutes les méthodes que l'on peut utiliser en HTTP.  


* **GET**
C'est la méthode la plus courante pour demander une ressource. Une requête GET est sans effet sur la ressource, il doit être possible de répéter la requête sans effet.
Par exemple : `GET www.site.com/cours.html` permet de récupérer le contenu de la page cours.html située sur le site site.

* **HEAD**
Cette méthode ne demande que des informations sur la ressource, sans demander la ressource elle-même.  Elle est intéressante si on veut, par exemple, récupérer des informations sur un fichier ou sur le serveur.
Exemple de réponse de la requête en ligne de commande:
![](https://i.imgur.com/NBCKGPU.png)


* **POST**
Cette méthode doit être utilisée lorsqu'une requête modifie la ressource. Par exemple, lorsque vous remplissez un formulaire sur internet ou faites une recherche sur Google, les requêtes utilisent la méthode POST pour récupérer ce que vous tapez au clavier.

* **OPTIONS**
Cette méthode permet d'obtenir les options de communication d'une ressource ou du serveur en général.

* **CONNECT**
Cette méthode permet d'utiliser un proxy comme un tunnel de communication.

* **TRACE**
Cette méthode demande au serveur de retourner ce qu'il a reçu, dans le but de tester et d'effectuer un diagnostic sur la connexion.

* **PUT**
Cette méthode permet d'ajouter une ressource sur le serveur.

* **DELETE**
Cette méthode permet de supprimer une ressource du serveur

###### source: [Wikipédia](https://fr.wikipedia.org/wiki/Hypertext_Transfer_Protocol)


##### l'URL

C'est l'adresse du serveur sur lequel vous désirez appliquer la méthode inscrite précédemment.

##### Version de protocole

La version de HTTP que vous désirez utiliser. Pour utiliser la version 1.1 de HTTP, on écrira `HTTP/1.1`.

##### Les entêtes

Ils regroupent tout un panel de paramètres pour l'exécution de la commande HTTP. Certains sont optionnels. On spécifie un entête ainsi : `nom_du_paramètre: valeur`. Le ':' est indispensable, mais l'espace avant la valeur est ignoré. Vous pourrez trouver [ici](https://www.iana.org/assignments/message-headers/message-headers.xhtml) la liste de ces entêtes, maintenue par IANA. Leur définition est donnée dans la [RFC 4229](https://tools.ietf.org/html/rfc4229).

Voici quelques exemples d'entêtes.

* Gestion de connexion : **Keep-Alive**
    * *syntaxe* : `Keep-Alive: <paramètres>`
    * *paramètres* : une liste de paramètres, séparés par des virgules. Chaque paramètre est composé d'un identificateur suivi de '=' et de la valeur du paramètre. Voici deux exemples d'identificateurs :
        * `timeout=valeur` : indique le temps minimal, en secondes, qu'une connexion passive doit rester ouverte.
        *  `max=valeur` : indique le nombre maximal de requêtes pouvant être envoyées sur la connexion avant d'être fermée. 
    * *exemple* : 
```
HTTP/1.1 200 OK
Connection: Keep-Alive
Content-Encoding: gzip
Content-Type: text/html; charset=utf-8
Date: Thu, 11 Aug 2016 15:23:13 GMT
Keep-Alive: timeout=5, max=1000
Last-Modified: Mon, 25 Jul 2016 04:32:39 GMT
Server: Apache

(body)
```
* Définition de la méthode d'authentification : **WWW-Authenticate**

    * *syntaxe* : `Authorization: <type> <credentials>`
    * *directives* : 
        * **<type>** : Le type d'identification. Le type typiquement utilisé est `Basic`. Vous pouvez trouver des détails sur ce type [ici](https://developer.mozilla.org/en-US/docs/Web/HTTP/Authentication#Basic_authentication_scheme). D'autres types sont définis [ici](http://www.iana.org/assignments/http-authschemes/http-authschemes.xhtml).
        *  **<credentials>** : Si le type d'identification est `Basic`, les *credentials* sont construits ainsi : 
            * le nom d'utilisateur et son mot de passe (par exmple `monnom:tunesauraspas`).
            * la chaîne de caractère résultante, codée en [base 64](https://developer.mozilla.org/en-US/docs/Web/API/WindowBase64/Base64_encoding_and_decoding).
     

    * *exemples* :
```
Authorization: Basic YWxhZGRpbjpvcGVuc2VzYW1l
```
###### source : [OpenClassrooms](https://openclassrooms.com/courses/les-requetes-http), [developer.mozilla](https://developer.mozilla.org/fr/docs/Web/HTTP/Headers)

##### Le Corps de la commande
Pour terminer la requête, on envoie le corps de requête. Il peut contenir, par exemple, le contenu d'un formulaire HTML envoyé en POST.
Dans le cas du formulaire, les variables ont un nom et une valeur, comme l'en-tête Cookie, et les différentes variables sont séparées par des esperluettes : "&" (notez que les variables passées par GET sont également séparées par "&").
* exemple : 
```
variable1=valeur1&variable2=valeur1
```
---

### Piste de TP : commande GET et POST

* Premièrement, téléchargez le logiciel [Postman](https://www.getpostman.com/)

* [Qu'est ce que Postman ?](cours/postman.html)

* La commande GET :
    * [Tutoriel d'accès à une page Web via Postman](cours/tuto_GET.html)

* La commande POST : se connecter à moodle
    * [Tutoriel de connexion à Moodle via Postman](cours/tuto_POST.html)

---

### Exercice

Exerce toi maintenant ! Voilà le lien d'un Google Form, utilise Postman pour te rendre sur cette page et le remplir. Prends des captures d'écran des requêtes que tu utilises pour valider le brevet.

* Astuce : les paramètres de la commande `POST` correspondant aux questions du formulaire sont (donnés dans l'ordre des questions) :
    * entry.1491143551
    * entry.323103977
    * entry.499847795

[Lien du Google Form](https://docs.google.com/forms/d/e/1FAIpQLSevVMgLC7Q9cFPuBrZ5_IZJ5oov2E-nsHR744e0Pxseq3skBA/viewform)

Vous pouvez vérifier que votre réponse au formulaire a bien été envoyée sur le lien suivant.

[Lien des réponses au Google Form](https://docs.google.com/forms/d/e/1FAIpQLSevVMgLC7Q9cFPuBrZ5_IZJ5oov2E-nsHR744e0Pxseq3skBA/viewanalytics)

---

### Pour aller plus loin: HTTPS vs HTTP

![](https://seopressor.com/wp-content/uploads/2017/07/HTTP-vs-HTTPS.png)

L'HyperText Transfer Protocol Secure, plus connu sous l'abréviation HTTPS   est la combinaison du HTTP avec une couche de chiffrement comme SSL ou TLS.

HTTPS permet au visiteur de vérifier l'identité du site web auquel il accède, grâce à un certificat d'authentification émis par une autorité tierce, réputée fiable. Il garantit théoriquement la confidentialité et l'intégrité des données envoyées par l'utilisateur et reçues du serveur. Il peut permettre de valider l'identité du visiteur, si celui-ci utilise également un certificat d'authentification client.

HTTPS est généralement utilisé pour les transactions financières en ligne : commerce électronique, banque en ligne, courtage en ligne, etc. Il est aussi utilisé pour la consultation de données privées, comme les courriers électroniques, par exemple.


###### source: [Wikipedia](https://fr.wikipedia.org/wiki/HyperText_Transfer_Protocol_Secure), [seopressor.com](https://seopressor.com/blog/http-vs-https/)
