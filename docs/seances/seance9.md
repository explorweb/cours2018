# ELU 525 - Séance 9


## Thématique : seconde phase de développement

# Cahier des charges cours Web
Par cours, nous entendons ici un document web qui permet à un apprenant de développer une compétence sur un sujet du Web. On pourrait également parler de ressource, dans le sens où c’est un élément disponible.
Nous avons convenu que nos apprenants étaient des élèves ingénieurs ayant quelques connaissances en informatique. Par compétence, on signifie ici la capacité à mobiliser des connaissances et des savoir-faire pour répondre à une situation problématique.
L’objectif d’apprentissage doit être clairement identifié pour guider la construction du contenu, puis permettre à l’apprenant de savoir ce qu’il obtiendra en parcourant/suivant cette ressource/cours.

Un cours ou une ressource contient donc a priori :
* Des connaissances présentées de la forme la plus claire possible, en mixant plusieurs médias. Cela peut passer par du texte, des images, des illustrations, des schémas, des animations et des vidéos. Les éléments nouveaux doivent être expliqués clairement (définition, exemple, …) ;
* Des pistes d’approfondissement. Des références, des sites pour aller plus loin...
* Des exemples, des exercices qui permettent de développer des savoir-faire. Une bonne pratique est de s’appuyer sur une xemple qui serve de fil rouge et qui se complète tout au long de l’apprentissage. Actuellement, il est possible d’intégrer facilement des environnements permettant de programmer à n’importe quel niveau dans un document web.
  * Codepen permet de tester et proposer des petits codes regroupant HTML, CSS et javascript. JSFiddle propose le même type de fonctionnalités de manière collaborative. Plunker permet de plus de gérer des solutions plus complètes
  * Heroku permet de tester des solution de cloud en se basant des services existants
  * Bitnami ou Docker permettent de récupérer des installations complètes de solutions existantes et de les tester soit dans le cloud, soit sur sa propre machine.
* Des retours. Un point important est de donner des retours au lecteur pour qu’il puisse s’assurer de sa bonne compréhension des notions présentées
 * Cela peut être un QCM sur les notions présentées, en termes de connaissances ;
 * Cela peut être un exercice d’application à réaliser pour ancrer une notion ;
 * Finalement, sur des intégrations plus complexes, les échanges entre pairs permettent de s’approprier l’ensemble des notions.
 * Pour information, certains environnements pour apprendre un nouveau langage proposent ainsi une suite de notions suivies d’exercices d’application avec des correcteurs automatiques.

Dans le cadre de ce cours, vous devez viser que l’apprenant aura une heure de travail devant lui pour dérouler votre ressource et être arrivé au bout (hors lecture supplémentaire).

Vous avez le droit de vous inspirer de ressources existantes et de les adapter, mais n’oubliez pas de les citer dans votre bibliographie.

## Liste des sujets
Votre mission sera donc de proposer une ressource qui permette d’atteindre un des objectifs suivants:
1. être capable d’écrire un premier site en utilisant HTML et CSS pour obtenir une page agréable, par exemple pour un site de type Association sportive ou pour un site d’objets perdus. Ce tutoriel HTML/CSS introduira donc les notions nécessaires écrire un tel site, et présentera clairement les notions structurantes de HMTL plutôt qu’un catalogue des balises. Pour les exercices, il s’appuiera sur l’utilisation de Plunker ou équivalent. Vous pourrez introduire Bootstrap pour aller plus loin.
1. être capable d’écrire un exemple de code en javascript pour animer un site d’association sportive, par exemple un petit diaporama. Ici aussi, vous utiliserez un outil extérieur pour proposer des exercices ;
1. être capable d’écrire une page en javascript qui permette de remplir un formulaire pour interroger un site d’objets perdus. Ici aussi, vous utiliserez un outil extérieur pour proposer des exercices
1. être capable d’afficher un tableau en lisant(en anglais “parse”) un fichier JSON ou XML en utilisant javascript. Vous utiliserez comme exemple une liste d’objets perdus, ou une liste d’activités sportives. Ici aussi, vous utiliserez un outil extérieur pour proposer des exercices.
1. être capable de faire une requête http vers un serveur web. Comprendre les options GET/POST  …  au moyen d’un outil de test d’API (de préférence Postman). Les tests proposés permettront d’interroger des bases de données accessibles ( par exemple : https://data.rennesmetropole.fr/page/home/
1. être capable de déployer un CMS pour proposer un site de vente ou un site d’association. Ce tutoriel proposera d’installer un CMS type Magento ou Wordpress, via un service de type bitnami sur sa machine locale, et de faire une prise en main simple.
