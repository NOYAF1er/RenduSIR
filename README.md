# SIR
------------------

## Binôme

>Christian ADANE, \n
>Louse MABIALA, \n
>Yannick N'GUESSAN \n

# Contenu
------------------
Ce repertoire contient 3 projets que sont:

## TP 7: Angular + JAX-RS

>Application repartie en deux modules soit une interface utilisateur avec AngularJS et un serveur avec Jax-RS (Jersey)

## TP 6: PokeDex

>Interface utilisateur (AngularJS) en interraction avec la plateforme "pokeapi"

## TP 3: NoSQL (Réponses aux questions)

### Question 1: 
>Quelles sont les limites d’une base de données orientée document ?

### Réponses: 
>Aucun schéma de modélisation n’est fixe 
>Une BD orientée document est inadaptée pour les données interconnectées (telles que les données du graphique)
>Le modèle de requête est limité à des clés et index
>Une BD orientée document peut alors être lent pour les grandes requêtes (avec MapReduce)
>Abscence de jointures: la structure d’un document est fait de telle sorte que les jointures sont le moins nécessaires
>possibles.

### Question 2: 
>Quelles sont les types de données stockés dans Redis ?

### Réponses: 
>Redis est une base de données open source de type clefs-valeurs mono-threadée.
>Les types de données stockés dans Redis sont entre autre:
>>-les listes: elles sont simplement des listes de string avec l’ordre d’insertion conservé. Une liste peut contenir jusqu’à plus de 4 milliards d’éléments.
>>-les sets: collections non ordonnées de String, ils permettent d’effectuer des opérations directement sur Redis ce qui permet de lancer des croisements de données particulièrement efficace.
>>-les hashs: ce sont de purs Map de String. Naturellement, c’est la structure qui semble la plus adapté pour représenter un objet comme un utilisateur d’un site web par exemple.
>>-les ZSet: Il s’agit de SET, avec la possibilité d’attacher un score à chaque valeur. Ils sont utilisés comme des index.

### Question 3: 
>Que peut on faire comme types de requêtes ?

### Réponses: 
>Les différents types de requêtes pouvant être effectués sur Redis sont citées ci dessous:

#### Strings
>SET pages:about “about us”
>GET pages:about 

#### Hashes
>HSET caen code_postal 14000
>HSET caen region “Normandie”
>HGET caen code_postal

#### Lists
get the 10 newest users
>keys = redis.Irange(‘users:newest’ , 0, 10)
multi get the actual 10 user objects
>redis.mget(*keys)

#### Sets
>SADD friends:leto ghanima
>SADD friends:leto duncan
>SADD friends:elvis duchan
>SINTER friends:leto friends:paul

#### ZSet
>ZADD friends:leto 1000 ghanima
>ZADD friends:leto 994 duncan
>ZADD friends:leto 2 farad’n
>ZRANGEBYSCORE friends:leto 500 1000


