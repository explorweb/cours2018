# Les Données

L'objectif est qu'à la fin de ce cours vous ayez une connaissance générale du moyen de récupérer des données sur le web pour résoudre un problématique dans le respect de la loi.

> Soyez avertis que les auteurs de ce cours n'ont aucunement la prétention d'être d'exaustif (d'autant plus sur un tel sujet).

Mais avant tout...
## C'est quoi une donnée ? 
---
![](https://i.imgur.com/JXd0huq.jpg)
###### source image : [Les données sur le web](https://i.imgur.com/JXd0huq.jpg)
---

La définition d'une donnée diffère du contexte dans lequel on se situe. 
D'un point de vu informatique, une donnée est la représentation d'une information dans un programme (le code source)  ou dans la mémoire durant l'exécution. 
Au sens de la loi, une donnée est une information qui permet d'identifier une personne physique directement ou indirectement.
Cependant une similitude ressort de toutes ces définitions. Les données, étant souvent des réponses à des questions, sont des informations relatives à toute chose physique ou virtuelle. Elles sont omniprésentes autour de nous et donc se retrouvent partout sur le Web.

Maintenant que l'on à une petite idée de ce dont on parle, faisons un petit point sur la loi européenne et française afin d'éviter de l'enfeindre.

## Réglementation des données
### :small_red_triangle: Au niveau français
##### *Loi Informatique et Liberté*
Les dispositions de cette loi portent sur  le traitement de données automatisé ou pas (cette seconde partie étant bien souvent oubliée).
Elle oblige différentes choses :
* Déclarer les traitement qui sont effectués.
* Assurer la sécurité des données en évaluant les risques liés aux traitements et en metant en place des solutions adaptés ainsi qu'en obligeant le respect de la confidentialité des données.
* Conserver les données personnelles dans l'Union Européenne. 
* Informer les personnes sur les différents traitement effectués.
* Ne pas traiter les données sensibles telles que celle relevant de la santé, religion ...
* Le traitement doit avoir un but spécifique et la collecte de données doit se faire de manière pertinante et avec le consentement des personnes.
* Le respect des droits des personnes à l'accés et à la communication des données, à l'opposition au traitement et à la modification/rectification.

###### source : [CNIL](https://www.cnil.fr/fr/loi-78-17-du-6-janvier-1978-modifiee)

### :small_red_triangle: Au niveau Européen
##### *La Réglementation Générale de la Protection des Données*
Cette réglementation est applicable à partir du 26 mai 2018. Il élargie certains droits des citoyens de l'Union Européenne.
* **Le droit de consentement** : les données ne peuvent être collectées sans un accord explicite et positif de la personne.
* **Le droit de portablilité** : la personne doit pouvoir récupérer ces données pour les transférer ailleur.
* **Le droit d'accès et de rectification** : la personne doit pouvoir avoir accès à ces données et les modifier.
* **Le droit de transparence** : droit de savoir à quoi servent les données.
* **La minimisation** : les données utilisées doivent être pertinantes avec le but du traitement.
* **Le droit d'oppoition** : droit se s'opposer au traitement de ces données à tout moment.
* **Le droit à l'oubli** : la personne doit pouvoir supprimer ces données et la conservations de celles-ci est limitée.
* **Le droit de profilage** : le droit de ne pas faire l'objet d'une décision fondée sur un traitement de données automatisé.
* **Le droit de sécurité** : la personne doit avoir le droit d'avoir ces données constamment protégés.
* **Le droit de notification** : la personne doit être informée en cas de fuite de données.

###### source : [CNIL](https://www.cnil.fr/fr/reglement-europeen-protection-donnees)

Ok très bien. A présent on sais ce qu'est une donnée et on sait ce qu'on à le droit de faire avec. Il serait donc intéressant d'aller à la pêche aux données maintenant !

## Obtenir des données
Maintenant qu'on sait ce que c'est qu'une donnée, on va s'intéresser à **"Comment l'obtenir"**. 
Les données fluctuent abondamment sur le web mais sont bien rangées quelque part et vous vous en doutez bien où :smirk: ... dans les **bases de données**. Elles permettent de stocker et de retrouver l'intégralité de données en rapport avec un thème ou une activité. Sur le Web les bases de données sont relationnelles, c'est à dire qui mettent en relation plusieurs données entre elles à travers des tables...
Il existe principalement trois moyens de se de se procurer des données :
* Trouver des données déjà en ligne
* Collecter des données soi même
* Acheter des données 
 

### 1. Trouver des données déjà en ligne
Plusieurs sources publient au regard de tous des données qu'on peut réutiliser. Ces sources sont les états et collectivités (sur [data.gouv.fr](http://data.gouv.fr/) entre autres), les organisations internationnales (la [Banque mondiale](https://data.worldbank.org/) par exemple) ou encore les sources scientifiques (comme la [NASA](http://data.nasa.gov/)).

De plus la magnifique communauté que regroupe le web a lancé plusieurs projets pour faciliter l'accès aux données déjà en ligne. Pour n'en citer qu'un, citons un français : [Nosdonnées.fr](http://nosdonnees.fr/).


> Déjà avec cette méthode, il est possible s'amuser à chercher à réponde à des questions comme : 
> -- Est ce que le pourcentage d'utilisateur d'internet est corrélé au chiffre d'affaire des GAFAM ?
> -- Est ce que l'espérance de vie augmente avec les dépenses de santé ?

###### source : [Ecole des données](https://ecoledesdonnees.org/handbook/cours/trouver-des-donnees/)


### 2. Collecter des données soi même

Pour collecter des données qui ne sont pas publiques soit même, il existe deux moyens :
* **Les outils de collecte de données**. Ce sont des outils informatiques spécialement développés pour le receuil de données sur les sites web ( https://blog.clydes.fr/10-outils-pour-scraper-des-donnees-sans-coder-ou-presque/), on appelle ça du **Scraping**. Ces outils ont pour rôle de récupérer des données présentes sur les sites web et de les stocker pour vous. Ils seront vus plus en détail plus loin dans le cours.
* **Python**. C'est un langage de programmation comme tout autre (Java, C++...). Mais muni de certaines bibliothèques comme **[Pandas, Numpy ou Matplotlib](https://openclassrooms.com/courses/decouvrez-les-librairies-python-pour-la-data-science/passez-de-numpy-a-pandas)** on peut l'utiliser pour faire de la collecte et du traitement de données sur le web. Il est maintenant le premier langage utilisé par les scientifiques pour le traitement de données.
---
![](https://i.imgur.com/I8dPytm.jpg)

---
L'expression la plus juste est le Big Data. En effet aujourd'hui on ne peut pas parler de données sur le web sans aborder le Big Data. L’expression  “Big  Data”  est  apparue  avec  l’accumulation  massive  d’informations  collectées  grâce  à  Internet et notamment via les sites marchands. :warning: **Mais attention la collecte de données est réglémentée** (cf. la partie liée à la réglementation européenne et française disponible [ici](https://hackmd.io/mQK_YpZfRGO14wlkoIy-wA?both#R%C3%A9glementation-des-donn%C3%A9es)). Il faut donc s'assurer d'avoir les droits adéquats avant de s'y aventurer.

### 3. Acheter des données
En plus de la collecte de données, il y a un autre moyen d'en obtenir.. il suffit de les **acheter**. En effet il existe plusieurs [entreprises](https://www.lebigdata.fr/top-5-data-brokers-vendeurs-donnees) spécialisées dans le commerce de données personnelles ou pas. Ces entreprises vendent les données qu'elles ont recueillies des utilisateurs aux particuliers, annonceurs, sociétés de e-commerce et les instituts de sondages qui sont prêts à débourser de grosses sommes pour avoir accès à ces précieuses informations sur leurs potentiels clients. Parmi ces entreprises on peut citer [SFR, ORANGE](http://data.blog.lemonde.fr/2013/08/14/big-data-vos-donnees-en-vente/), [GOOGLE, FACEBOOK](https://www.usine-digitale.fr/article/ces-entreprises-qui-achetent-vos-data.N243379) etc..

Ça y est ! On a saturé notre disque dur de données d'importance vitale. Il est temps de les faire parler.


## Les outils d'analyse de données


* outils pour analyser les données
[ASQ](http://asq.org/learn-about-quality/data-collection-analysis-tools/overview/overview.html)
[Coursera](https://www.coursera.org/learn/data-analysis-tools)

Nous supposons que maintenant vous avez sélectionné un ensemble de données et une question de recherche, gérez vos variables

- １．Quel est le choix de vos paquets logiciels statistiques?
 SAS，MATLAB or Python ?
- 2 Commencer à analyser la relation entre vos données
1.relation graphique
2.relations statistiques
 
- Analyser l'indépendance entre vos données
1. Poser des hypothèses
Ces variables (données) sont-elles indépendantes?
2. écrivez un programme pour verifier vos hypothèses
Ce programme gère toutes les variables supplémentaires dont vous pourriez avoir besoin, les exécute et les interprète.
3. Modifiez vos hypothèses en fonction de vos résultats obtenus
Puis réessayer étape 2
 
- tester des hypothèses dans le contexte d'une corrélation de Pearson
c'est-à-dire, quand vous avez deux variables quantitatives
1. écrivez un programme qui gère toutes les variables supplémentaires dont vous pourriez avoir besoin et interprète un coefficient de corrélation
2. modifier vos hypothèses en fonction de vos résultats
Puis réessayer étape 1

- Essayer quelque chose dans le concept de base de l'interaction statistique (également connu sous le nom de modération)
En statistique, la modération se produit lorsque la relation entre deux variables dépend d'une troisième variable. En d'autres termes, une troisième variable (Z) va affecter la relation entre vos variables (X) et (Y)





## Méthode : Les données comme réponse

On a vu beaucoup de choses jusqu'ici. Cependant il faut lier un peu tout ça pour pouvoir résoudre un problème (par exemple prendre la décision de se positionner sur un certain marché lorsque l'on est une entreprise). Voici un petite méthodologie pour vous aider à faire vos premiers pas.


#### 1. Définir la question, le problème.
La première étape est applicabla à tous les domaines : définir clairement son problème et se poser la bonne question. Pour que votre question soit "bonne" vérifier qu'elle soit claire et mesurable.

#### 2. La mesure
Un fois votre question posée (ce qui est souvent la plus grosse partie du problème) il va falloir y répondre. C'est ici qu'interviennent les données.
##### Que mesurer ?
Dans un premier temps, il est judicieux de ce demander de quel type de donnée vous avez besoin pour répondre à votre question (qui se divise très certainement en plusieurs sous questions).
##### Comment le mesurer ?
Une fois que vous avez identifié ce dont vous avez besoin, vous pouvez choisir un moyen de récupérer les données dont vous avez besoin à l'aide des techniques vues précédemment.

#### 3. Récupérer les données
Vous savez déjà comment faire. :smile: 

#### 4. Analyser les données
Une fois que vous pensez avoir récupérer tous ce dont vous avez besoin (rassurez vous vous risquez avoir à revenir plusieurs fois aux étapes précédentes) il vous reste à les analyser.
Pour cela, le tableur sera votre meilleur ami. Néanmoins pour des statistiques plus avancées certains logiciels peuvent vous faciliter grandement la vie. Des logiciels comme *Minitab*, *Stata* ou encore *Visio* sont plutôt apréciés des internautes. Cepandant pour la majeure partie du traitement des données, le tableur est largement suffisant. Pour vous reseigner sur cette usage Harvard à publié une [revue](http://hbr.org/product/baynote/an/2001HF-HTM-ENG?referral=00506) à ce sujet.

#### 5. Il ne vous reste plus qu'à interpréter vos résultats.




###### source : [Big sky](https://www.bigskyassociates.com/blog/bid/372186/The-Data-Analysis-Process-5-Steps-To-Better-Decision-Making)
