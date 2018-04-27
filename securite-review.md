# La sécurité sur le web

## Introduction
De la même manière qu'il propose un nombre presque infini de fonctionnalités, le web peut porter atteinte à notre sécurité, et les failles de sécurité qui lui sont liées sont très nombreuses. Pour s'en prémunir et naviguer en toute sécurité, il faut être au courant des risques et les comprendre. Ce cours a pour but d'avertir sur ces risques, d'expliquer les mécanismes du web qui présentent des failles et sont par conséquent un danger potentiel pour les internautes. Ce cours présente également une solution de sécurité : le VPN, qui permet entre autres de cacher ses informations.

## Serveur DNS, ou comment accéder à son site préféré

## I. Qu'est ce qu'un serveur DNS ? À quoi ça sert ?

Tout d'abord, nous devons comprendre comment votre navigateur se connecte à un site. Un site web est en fait un fichier de code (le plus souvent du HTML) que votre navigateur exécute et affiche la page web qui en résulte. Chaque site est hébergé par un serveur auquel vous devez vous connecter pour pouvoir accéder au site. Pour cela, vous devez vous munir de l'adresse IP du serveur. Vous conviendrez que retenir l'adresse IP de chaque site auquel vous voulez vous connecter n'est pas vraiment amusant. C'est pourquoi il existe ce que l'on appelle un DNS (Domain Name System). Un DNS est tout simplement un annuaire associant une adresse IP avec un nom de domaine (par exemple : google.fr). De ce fait, pour vous connecter au site de Google, il vous suffit de connaître le nom de domaine (google.fr) beaucoup plus facile à retenir, et le DNS trouve l'adresse IP correspondante pour vous.

    Et le serveur DNS dans tout ça ?

Avant 1984, le DNS était stocké localement sur la machine de l'internaute, mais avec le grand nombre de sites qui se créaient à l'époque, on s'est vite rendus compte que le DNS allait prendre beaucoup trop de place sur le disque dur de l'internaute. C'est pourquoi en 1984 sont mis en place les serveurs DNS qui ont pour unique but de stocker les DNS. Le problème restait cependant le même, s'il fallait stocker tout l'annuaire sur une seule machine, il aurait fallu beaucoup de disques durs (sachant qu'à l'époque il ne faisaient pas 2To). Il a donc fallu structurer tout ça !

## II. Notion de domaine

Vous vous êtes toujours demandé pourquoi certains sites finissaient par .fr, d'autres par .com, etc ? Le web est en fait hiérarchisé. fr, com, org, etc. correspondent à ce que l'on appelle des domaines. Ce sont les domaines de premier niveau. google.fr est un sous-domaine de fr, c'est à dire qu'il appartient au domaine fr, comme wikipedia.org est un sous-domaine de org. Un sous-domaine est lui aussi un domaine. De telle sorte que fr.wikipedia.org (la version française de wikipedia) est un sous-domaine de wikipedia.org. Il en existe d'autres, www.wikipedia.org par exemple. Le web a donc une structure arborescente. À noter que lorsque vous achetez un nom de domaine (exemple : exemple.fr), vous pouvez créer autant de sous-domaines que vous le souhaitez et vous en serez le propriétaire.

Revenons au DNS. Chaque domaine possède en réalité son propre serveur DNS, qui contient l'annuaire de tout le domaine. Il stocke les adresses IP correspondantes de tous les sous-domaines. Voyons ce qu'il se passe lors de la requête d'un utilisateur. L'internaute souhaite se connecter au site dns.coursweb.fr. Il demande au serveur DNS "local" (c'est généralement le serveur fourni par le FAI) quelle est l'adresse IP correspondante au nom de domaine dns.coursweb.fr. Ce-dernier ne stockant pas tout l'annuaire ne connait pas la réponse. Il doit interroger le serveur DNS du domaine coursweb.fr dont il ne connait pas l'adresse IP non plus. Dans un premier temps, il demande au serveur DNS du domaine fr (connu puisque c'est un domaine de premier niveau) l'adresse IP du sous-domaine coursweb.fr. Après avoir reçu la réponse, il demande au serveur DNS de coursweb.fr l'adresse IP du sous-domaine dns.coursweb.fr puis transmet l'information à l'internaute qui peut alors se connecter.

## III. Le serveur DNS : une faille de sécurité majeure

Imaginez qu'un pirate réussisse à se faire passer pour un serveur DNS et lorsque vous demandez l'adresse IP du domaine amazon.fr, il ne vous donne pas la vraie adresse mais une adresse d'un serveur qu'il contrôle. Il peut vous faire croire que vous naviguez sur le site officiel d'amazon alors que vous êtes sur un faux site, vous tapez vos coordonnées bancaires, et le pirate vous les vole.

Une des attaques les plus connues s'appelle l'attaque DNS Cache Poisonning. Le cache d'un serveur DNS est une zone mémoire où le serveur stocke temporairement l'annuaire d'un domaine. Lorsqu'un internaute demande l'adresse de exemple.fr, le serveur DNS va chercher l'information puis la stocke dans son cache, de telle sorte que si un autre internaute lui demande l'adresse de exemple.fr, il n'ait pas à chercher de nouveau. Le pirate cherche à corrompre l'intégrité de la mémoire cache en bombardant le serveur DNS de requêtes (amazon.fr par exemple) et en même temps, depuis une autre machine, envoie des résolutions de requêtes en se faisant passer pour le serveur DNS du domaine amazon.fr. Bien entendu, les requêtes sont identifiées, et il faut que la réponse ait la même identification que la requête. Le pirate exploite le fait qu'il est facile de "deviner" l'identifiant. En réalité, il teste tous les identifiants possibles jusqu'à trouver le bon. Quand le serveur DNS reçoit la fausse réponse venant du pirate, il la stocke dans sa mémoire cache, et lorsqu'un internaute demande l'adresse de amazon.fr, il est redirigé sur le site du pirate.


## IV. Les Menaces et failles visant la sécurité du Web
La conception et l'ulisation du Web exige la securité  avec une vigilance car les la plupart des activités de ces jours se font sur l'internet et le Web. Dans cette partie de presentation on se base sur les failles et les vulnerabilités sur le Web qui nous exigent la securité de nos sites Web et applications web.

#### La faille Cross-Site Scripting(XSS)
C'est une faille permettant l'injection du contenu du web via le code HTML ou Javascript dans des variables mal protégées. Il y a deux types de XSS:
##### Le XSS réfléchi(non permanent)
Cette faille est basée sur les données fournis par l'utilisateur.
Les champs de formulaires des applications web que leurs utilisateurs remplissent sont à la même fois les failles de securité. 
l'attaquant crée une page Web avec un lien vers l'application de l'utilisateur qui contient des parametres du code javascripts frauduleux. En utilisant ce lien,par son navigateur, l'utilisateur va interpréter le code malicieux et va tenter d'exécuter une fonctionnalité de l'application cible. Pendant la connection de lutilisateur,l'application va exécuter la commande sans que l'utilisateur le connaisse.
![](https://web.developpez.com/tutoriels/web/failles-securite-application-web/images/failles_de_securite_v1-3_Page_18_Image_0001.jpg)
[Source Image:Failles de sécurité des applications Web](https://web.developpez.com/tutoriels/web/failles-securite-application-web/)
##### Le XSS stocké(permanent)
Cette faille très dangeureuse comme ça se fait quand code malicieux  pouvait être stocké  dans les bases de donnée de l'application web.  
il sera executé a chaque fois que l'utilisateur lance le site web  ou l'application web.
L'application va alors accepter d'exécuter cet ordre comme si la demande provenait de l'utilisateur lors de son utilisation de l'application. [Details1](https://openclassrooms.com/courses/protegez-vous-efficacement-contre-les-failles-web/la-faille-xss-1)
et [Details2](https://developer.mozilla.org/fr/docs/Learn/Server-side/First_steps/Website_security)
![](https://web.developpez.com/tutoriels/web/failles-securite-application-web/images/failles_de_securite_v1-3_Page_19_Image_0001.jpg)
[source Image:Failles de sécurité des applications Web](https://web.developpez.com/tutoriels/web/failles-securite-application-web/)
#### L'injection SQL
C'est un vecteur d'attaque qui permet les utilisateur marveillant d'injecter les morceaux de code non filtrés et les executer.
Une attaque par injection réussie peut usurper des identités(Identity spoofing), créer de nouvelles identités avec des droits d'administration, accéder à toutes les données sur le serveur ou détruire / modifier les données pour les rendre inutilisables.
[source Image:Openclassroom:](https://openclassrooms.com/courses/protegez-vous-efficacement-contre-les-failles-web/l-injection-sql-1)
![](https://www.vpnfaqs.com/wp-content/uploads/2015/06/SQL-injection-vulnerability-found-in-Vbulletin-hosted-websites.png)
[Source image:Deep into SQL injection](https://www.vpnfaqs.com/deep-sql-injection/)
[SQL Injection](https://www.vpnfaqs.com/deep-sql-injection/)
#### Cross-Site Request Forgery(CSRF) ou One click attack
La faille CSRF peut etre aussi expliqué comme la falsification inter-sites car il permet l'attaquant d'executer les actions en utilisant les informations de l'autre utilisateur sans son consentement c'est-à- dire que l'attaquant vise un site ou une page en utilisant l'utilisateur comme declancheur sans le savoir.![](https://images.leblogduhacker.fr/2014/02/faille-csrf1.jpg)
[Source image:La faille CSRF, explication et contre-mesures](https://www.leblogduhacker.fr/faille-csrf-explications-contre-mesures/)
Suivant l'exemple ci-dessus l'attaquant peut supprimer l'article d'un administrateur. Si on suppose que le lien de suppression d'un article soit:http://www.monblog.fr/del.php?id=1, Normalement un visiteur non connecté à la page d'administration n'a pas le droit d'editer ou de supprimer les articles d'un blog qui ne lui appartient pas. Par contre si le visiteur connait ce lien ça suffit pour lui d'envoyer le lien à l'administrateur en faisnat en sorte que ce dernier clique et quand l'administrateur clique le lien de suppression s'éxecute avec succès. La faille CSFR peut etre protegé par l'Authentification par jeton et par la demande de confirmation.
[Plus de details sur Cross-Site Request Forgery(CSRF)](https://www.leblogduhacker.fr/faille-csrf-explications-contre-mesures/)
#### CRLF 
Carriage Return Line Feed est une faille plus souvant utilisé pour recupérer le mot de passe de quelqu'un en utilisant la fonction mail de la page "mot de passe oublié" qu'on trouve sur beaucoup des site web et application web. En utilisant cette faille, il suffit de connaitre le mail de l'utilisateur et se mettre en copy pour lancer une attaque.
#### L'Attaque par force brute
L'attaque par force brute est utilisé pour 
trouver un mot de passe ou un clé en testant une par une et tous les combinaison possibles. Il effectivement nécessite beaucoup de temps d'execution mais il est efficace. Cette attaque aussi est souvent combiné avec l'attaque par dictionaire dont l'attaquant utilise enormes des  dictionaires contenant des mots de passes regulièrment utilisé.
#### La faille Include
La function include() est une function utilisé dans beaucoup de langage de programmation. Il est aussi utilisé pour executer du code PHP situé dans une autre page,Sa mauvaise utilisation peut étre exploiter par les Hackers  pour faire ceux qu'ils veulent.Comme cette fonction pemet l'accès autres pages,C'est evident qu'il est exposés aux hackers en cas de mauvais utilisation.
Il ya deux types de faille Include:
###### la faille include à distance et la faille include en Local
#### La faille Upload
L'utilisation de la balise HTML "<input type="file" />" qui permet d'heberger le fichier,il peut aussi étre utiliser par un utilisateur malintentionné pour uploader le fichier marveillant qui peut lui permettre de prendre le control de votre site web et méme il peut arriver à prendre main sur le serveur. 
###### La double Extension
Peut etre que le type des fichier à héberger peut etre limiter mais la double extension permet d'heberger le fichier avec une nouvelle extension en ignorant l'extension prévu.
Par example on veut uploader seulement les fichiers d'extension .png, Je peux également nommer mon fichier backdoor.php.\0.png qui permet d'afficher mon fichier  comme backdoor.php et il ignore  l'autre partie du fichier.   
#### Variation de session
La session qui n'est pas bien protégée est aussi une considerable risque puisque il peut etre volée  ou empoisonnée(session hijacking et poisoning). 
###### Le vol de sesssion 
Lors de la connection sur un site, on reçoit un ID unique qui doit etre attribueé à cette session qui permet d'etre reconnu par le serveur. 
Si la session  n'est pas securisé un pirate/hacker peut attaque et profiter cette session  et fait ce qui le plait durant toute la session.

![](https://sdz-upload.s3.amazonaws.com/prod/upload/sch%C3%A9ma%2021.jpg)
[Source Image:Opensource](https://openclassrooms.com/courses/protegez-vous-efficacement-contre-les-failles-web/les-variable-de-session)
###### Empoisenement de session
Au moment où le pirate peut utliser la session, il peut aussi injecter tout ce qu'il veut pour detruire ou endommager votre système. Le principe est le même que celui de l'injection SQL  
#### Buffer overflow
Avant le traitement de toute donnée, l'ordinateur doit le stocker dans une  memoire temporaire appelé"Tampon". La surexploitation du tampon en stockant les données de grande taille que celle du tampon ça la deborde. Ce debordement
 du tempon est la cause principale ce faille car il permet l'attaquant d'injecter les donnée et les instructions pour l'exploitation.Cette faille nécessite une bonne connaissance technique de fonctionnement d'ordinateur ainsi que de la programation.
 #### Vers(Worms)
Les vers sont les programme marveillant qui se dupliquent et se propagent eux sur les réseaux meme  si leur but principal est se reproduire et de se duopliquer, Il surchargent l'ordinateur et le réseau sur le quel il se trouve et ils peuvent aussi entrainer de sérieux dysfonctionnement de l'ordinateur. [plus d'infos](http://www.creantivirus.com/dossiers/difference-vers-virus-trojans/).

#### Les Virus
les petit programme qui s'attache un programme complet, et le modifie. L'execution du programme complet provoque l'exécution du virus en même temps pour juste contaminer le systeme. [plus d'infos](http://www.creantivirus.com/dossiers/difference-vers-virus-trojans/) . Même s'il est à la base  un automate autoréplicatif marvaillant maintenant est additionné le code marveillant inventé pour se propager à autres ordinateurs en s'inserent sur les logiciels légitimes qui peuvent perturber le fonctionnement du système d'ordinateur.Tous les moyens d'échange de données numériques comme les réseaux informatiques, les cédérom,les clefs USB,les disques durs, etc les favorisent de se repandre. [plus d'infos](https://fr.wikipedia.org/wiki/Virus_informatique)
#### Autres Menaces et vulnérabilités 
Il ya beaucoup ménaces et vulnerabilités du Web comme:Clickjacking,Denial of Service,Diretory Traversal,File Inclusion,Command Injection,etc



  ## V. Une solution de sécurité: le VPN (Virtual Private Injection)
  
En naviguant sur le net, vous n'êtes à l'abri d'aucun piratage informatique ou de vols de données. en effet, l'on peut recuperer vos données après avoir accedé à vos identifiants. Afin de se prémunir de ces incidents, il est necessaire d'utiliser les VPN(Virtual Private Network)
Les VPN sont des reseaux virtuels s'appuyant sur un autre reseau comme Internet. Il permet de faire transiter des infos entre les différents membres de ce VPN , le tout de manière sécurisée. une connexion VPN revient à se connecter en reseau en utilisant comme adresse de destination, les adresses IP locales de votre machine.
utiliser les VPN comporte des avantages mais aussi des inconvenients.

les avantages principaux:
-Protection optimale sur Internet
-Téléchargez des torrents sans risque	
-Naviguez librement en sécurité	–
-Contournez la censure géographique	–
-Streamez tout de partout (Netflix, Bein,…)	

les inconvenients
-Peut ralentir votre connexion internet
-Il faut en prendre un payant

Pour configurer un VPN, il existe trois methodes à savoir le PPTP, l'Ipsec et le l'openVPN. ce sont ces trois VPN que vous pouvez installer sur des servers dédiés ou  des serveurs personnels.
Voici ici quelques lignes de commandes pour les plus curieux qui veulents savoir comment configurer un VPN avec Ipsec. 

## situation: 
    nous avons un reseau composé de trois routeurs R1,R2 et R3. nous voulons installer un vpn entre les routeurs R1 et R3. ce TP a pour objectif de
    montrer quelle configuration faut-il faire sur chaque routeur pour confi-
    gure le vpn. le logiciel utilisé s'appelle Cisco Packet tracer.
    
Nous commencerons par configurer notre PC et notre serveur en leur attribuant la bonne configuration réseau. Nous attaquerons ensuite la configuration du routeur R1  
On commence par le Hostname :
```
Router#configure terminal
Router(config)#hostname R1
Nous configurons ensuite les adresses IP des deux interfaces :
R1(config)#interface FastEthernet 0/1
R1(config-if)#ip address 192.168.1.254 255.255.255.0
R1(config-if)#no shutdown
R1(config-if)#exit
R1(config)#interface FastEthernet 0/0
R1(config-if)#ip address 10.1.1.1 255.255.255.252
R1(config-if)#no shutdown
R1(config-if)#exit

```
Nos interfaces sont maintenant configurées, il nous reste à configurer le routage. J'ai choisi de faire du routage RIP( vous pouvez faire du statique si vous voulez)

1.Router R1
```
R1(config)#router rip
R1(config-router)#version 2
R1(config-router)#no auto-summary
R1(config-router)#network 192.168.1.0
R1(config-router)#network 10.1.1.0
R1(config-router)#exit


```
La configuration de base de notre routeur R1 est terminée. Passons maintenant au routeur R2

2) Routeur R2
Même procédure pour notre routeur R2 :
On commence par le Hostname
```
Router#configure terminal
Router(config)#hostname R2
```
Nous configurons ensuite les adresses IP des deux interfaces
```
R2(config)#interface FastEthernet 0/1
R2(config-if)#ip address 10.2.2.2 255.255.255.252
R2(config-if)#no shutdown
R2(config-if)#exit
R2(config)#interface FastEthernet 0/0
R2(config-if)#ip address 10.1.1.2 255.255.255.252
R2(config-if)#no shutdown
R2(config-if)#exit
```

Nos interfaces sont maintenant configurées, il nous reste à configurer le routage.

```
R2(config)#router rip
R2(config-router)#version 2
R2(config-router)#no auto-summary
R2(config-router)#network 10.2.2.0
R2(config-router)#network 10.1.1.0
R2(config-router)#exit
```
La configuration de base de notre routeur R2 est terminée. Passons maintenant au routeur R3

3) Routeur R3
Même procédure pour notre routeur R3 :
On commence par le Hostname
```
Router#configure terminal
Router(config)#hostname R3
```
Nous configurons ensuite les adresses IP des deux interfaces 
```
R3(config)#interface FastEthernet 0/1
R3(config-if)#ip address 192.168.3.254 255.255.255.0
R3(config-if)#no shutdown
R3(config-if)#exit
R3(config)#interface FastEthernet 0/0
R3(config-if)#ip address 10.2.2.1 255.255.255.252
R3(config-if)#no shutdown
R3(config-if)#exit
```

Nos interfaces sont maintenant configurées, il nous reste à configurer le routage.
```
R3(config)#router rip
R3(config-router)#version 2
R3(config-router)#no auto-summary
R3(config-router)#network 10.2.2.0
R3(config-router)#network 192.168.3.0
R3(config-router)#exit
```

La configuration de base de notre routeur R3 est terminée

4. Configuration du VPN

Il faut savoir que le VPN se configure juste sur les Routeurs d'extrémités dans notre cas R1 et R3 

    4.1) Configuration VPN sur R1

 Etape 1 
Commençons par notre routeur R1, vous devez vérifier que l'IOS de vos routeurs supporte le VPN. On active ensuite les fonctions crypto du routeur :
```
R1(config)#crypto isakmp enable
``` 
Cette fonction est activée par défaut sur les IOS avec les options cryptographiques.
 
 Etape 2 :
Nous allons configurer la police qui détermine quelle encryptions on utilise, quelle Hash quelle type d'authentification, etc.
```
R1(config)#crypto isakmp policy 10
R1(config-isakmp)#authentication pre-share
R1(config-isakmp)#encryption 3des
R1(config-isakmp)#hash md5
R1(config-isakmp)#group 5
R1(config-isakmp)#lifetime 3600
R1(config-isakmp)#exit
```
*group 5 : Spécifie l'identifiant Diffie-Hellman
*lifetime : Spécifie le temps de validité de la connexion avant une nouvelle négociation des clefs.

Etape 3:
Ensuite nous devons configurer la clef :
```
R1(config)#crypto isakmp key mot_de_passe address 10.2.2.1
```
Sur certains routeurs avec certains IOS la commande ne fonctionne pas car le routeur demande si le mot de passe doit être chiffré ou pas, dans ce cas, tapez cette commande :

```
R1(config)#crypto isakmp key 6 mot_de_passe address 10.2.2.1
```

Etape 4 :
Configurons les options de transformations des données :
```
R1(config)#crypto ipsec transform-set 50 esp-3des esp-md5-hmac
```
*esp : Signifie Encapsulation Security Protocol

(N'oublions pas d'utiliser les mêmes protocoles d'encryptions et de Hash utilisés dans la première étape.
Dans notre cas :
Encryption : 3des
hash : md5)
On fixe ensuite une valeur de Lifetime :
```
R1(config)#crypto ipsec security-association lifetime seconds 1800
```
Etape 5 :
La 5éme étape consiste à créer une ACL qui va déterminer le trafic autorisé.
```
R1(config)#access-list 101 permit ip 
192.168.1.0  0.0.0.255  192.168.3.0   0.0.0.255
```

Etape 6 :
Dans cette dernière étape nous configurons la crypto map qui va associer l'access-list, le traffic, et la destination 
```
R1(config)#crypto map nom_de_map 10 ipsec-isakmp
R1(config-crypto-map)#set peer 10.2.2.1
R1(config-crypto-map)#set transform-set 50
R1(config-crypto-map)#set security-association lifetime seconds 900
R1(config-crypto-map)#match address 101
R1(config-crypto-map)#exit
```
Nous devons appliquer la crypto map sur l'interface de sortie :
Dans notre cas FastEthernet 0/0.
```
R1(config)#interface FastEthernet 0/0
R1(config-if)#crypto map nom_de_map
```

*Jan 3 07:16:26.785: %CRYPTO-6-ISAKMP_ON_OFF: ISAKMP is ON
Un message vous indique que la crypto map fonctionne.

    4.2 Configuration VPN sur R3

On refait la même configuration que sur R1 :
Etape 1:
```
R3(config)#crypto isakmp enable
```

Etape 2:
```
R3(config)#crypto isakmp policy 10
R3(config-isakmp)#authentication pre-share
R3(config-isakmp)#encryption 3des
R3(config-isakmp)#hash md5
R3(config-isakmp)#group 5
R3(config-isakmp)#lifetime 3600
R3(config-isakmp)#exit
```
Etape 3:
```
R3(config)#crypto isakmp key mot_de_passe address 10.1.1.1
ou
R3(config)#crypto isakmp key 6 mot_de_passe address 10.1.1.1
` ``

R3(config)#crypto ipsec transform-set 50 esp-3des esp-md5-hmac
R3(config)#crypto ipsec security-association lifetime seconds 1800
```
Etape 5 :
```
R3(config)#access-list 101 permit ip
192.168.3.0  0.0.0.255  192.168.1.0   0.0.0.255
```
Etape 6:
```
R3(config)#crypto map nom_de_map 10 ipsec-isakmp
R3(config-crypto-map)#set peer 10.1.1.1
R3(config-crypto-map)#set transform-set 50
R3(config-crypto-map)#set security-association lifetime seconds 900
R3(config-crypto-map)#match address 101
R3(config-crypto-map)#exit
R3(config)#interface FastEthernet 0/0
R3(config-if)#crypto map nom_de_map
```
*Jan 3 07:16:26.785: %CRYPTO-6-ISAKMP_ON_OFF: ISAKMP is ON

```

```
# Sources
-Fonctionnement d'un serveur DNS, cours laboratoire d'informatique de Grenoble : http://lig-membres.imag.fr/sicard/crRES/cours%20DNS.pdf
-La securité du web:https://developer.mozilla.org/fr/docs/Learn/Server-side/First_steps/Website_security
-Les failles et les protection https://openclassrooms.com/courses/protegez-vous-efficacement-contre-les-failles-web/la-faille-xss-1
 -Failles de securité d'application web s https://web.developpez.com/tutoriels/web/failles-securite-application-web/
-Deep in injection Sql:https://www.vpnfaqs.com/deep-sql-injection/
-La faille CSRF, explications et contre-mesures https://www.leblogduhacker.fr/faille-csrf-explications-contre-mesures/
