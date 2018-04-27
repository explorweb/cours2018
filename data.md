# Les Données

## C'est quoi une donnée ? 
---
![](https://i.imgur.com/JXd0huq.jpg)
###### source image : [Les données sur le web](https://i.imgur.com/JXd0huq.jpg)
---

La définition d'une donnée diffère du contexte dans lequel on se situe. 
D'un point de vu informatique, une donnée est la représentation d'une information dans un programme (le code source)  ou dans la mémoire durant l'exécution. 
Au sens de la loi, une donnée est une information qui permet d'identifier une personne physique directement ou indirectement.
Cependant une similitude ressort de toutes ces définitions. Les données, étant souvent des réponses à des questions, sont des informations relatives à toute chose physique ou virtuelle. Elles sont omniprésentes autour de nous et donc se retrouvent partout sur le Web.


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

:warning: **Attention** : vérifiez que le format des données que vous récupérez soit lisible par un ordinateur.

> Déjà avec cette méthode, il est possible s'amuser à chercher à réponde à des questions comme : 
> -- Est ce que le pourcentage d'utilisateur d'internet est corrélé au chiffre d'affaire des GAFAM ?
> -- Est ce que l'espérance de vie augmente avec les dépenses de santé ?

###### source : [Ecole des données](https://ecoledesdonnees.org/handbook/cours/trouver-des-donnees/)


### 2. Collecter des données soi même

Pour collecter des données qui ne sont pas publiques soit même, il existe deux moyens :
* **Les outils de collecte de données**. Ce sont des outils informatiques spécialement développés pour le receuil de données sur les sites web ( https://blog.clydes.fr/10-outils-pour-scraper-des-donnees-sans-coder-ou-presque/), on appelle ça du **Scraping**. Ces outils ont pour rôle de récupérer des données présentes sur les sites web et de les stocker pour vous. Ils seront vus plus en détail plus loin dans le cours.
* **Python**. C'est un langage de programmation comme tout autre (Java, C++...). Mais muni de certaines bibliothèques comme **[BeautifulSoup](https://fr.wikipedia.org/wiki/Beautiful_Soup)**, on peut l'utiliser pour faire de la collecte et du traitement de données sur le web. Il est maintenant le premier langage utilisé par les scientifiques pour le traitement de données.
---
![](https://i.imgur.com/I8dPytm.jpg)

---
L'expression la plus juste est le Big Data. En effet aujourd'hui on ne peut pas parler de données sur le web sans aborder le Big Data. L’expression  “Big  Data”  est  apparue  avec  l’accumulation  massive  d’informations  collectées  grâce  à  Internet et notamment via les sites marchands. Mais :warning::warning::warning:**la collecte de données est réglémentée dans tous les pays d'Europe**. Il faut donc s'assurer d'avoir les droits adéquats avant de s'y aventurer.

### 3. Acheter des données
En plus de la collecte de donnée, il y a un autre moyen d'en obtenir.. il suffit de les **acheter**. En effet il existe plusieurs [entreprises](https://www.lebigdata.fr/top-5-data-brokers-vendeurs-donnees) spécialisées dans le commerce de données personnelles ou pas. Ces entreprises vendent les données qu'elles ont recueillies des utilisateurs aux particuliers, annonceurs, sociétés de e-commerce et les instituts de sondages qui sont prêts à débourser de grosses sommes pour avoir accès à ces précieuses informations sur leurs potentiels clients. Parmi ces entreprises on peut citer [SFR, ORANGE](http://data.blog.lemonde.fr/2013/08/14/big-data-vos-donnees-en-vente/), [GOOGLE, FACEBOOK](https://www.usine-digitale.fr/article/ces-entreprises-qui-achetent-vos-data.N243379) etc..
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

## Les outils d'analyse de données


* tools to analise data
http://asq.org/learn-about-quality/data-collection-analysis-tools/overview/overview.html
https://www.coursera.org/learn/data-analysis-tools

we asume that now you have selected a data set and research question, managed your variables 

- １． what is the choice of your statistical soft packages?
 SAS，MATLAB or Python ?
- 2 start to analys the relationship between your data
1.relationship graphically 
2.relationships statistically

 
- Analys Independence between your data
1.give hypotheses
Are those vatiables independent?
2.write a program to test your hypotheses
manages any additional variables you may need and runs and interprets
３.modify your hypotheses according to your programming results
retry step 2
 
- test hypotheses in the context of a Pearson Correlation
that is to say,when you have two quantitative variables
1.write a program that manages any additional variables you may need and interprets a correlation coefficient
2.modify your hypotheses according to your programming results
retry step 1
  
- try something in the basic concept of statistical interaction (also known as moderation)
In statistics, moderation occurs when the relationship between two variables depends on a third variable.
that is to say,a third (Z) variable will affec the relation between your (X) and (Y) variable


## Les données comme réponse

C'est bien beau de savoir récuperer des données, mais maintenant le but est que cette compétence nous serve pour prendre des décision pour une entreprise par exemple.

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
