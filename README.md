# Cours d'Algorithmique++

_Note : A l'heure actuelle, ce repository présente la structure des éléments qui vont/sont/seront (être) abordés - il s'agit principalement d'un support visant à faciliter la prise en main des notions vues durant les séances._

- Introduction
- Algorithmes & projet
- Des spécifications ...
- A l'abstraction
- Pseudo-Code
- Exalgo
- Algorigrammes
- Mises à jour

## Historique

- v1.0 : version initiale du document

# Préambule

Petit repo de documentation pour appréhender pleinement l'algorithmique.
Ce document n'a pas vocation à faire un cours complet et exhaustif de tous les concepts d'algorithmiques (simples ou avancés) mais d'être un support permettant de pouvoir se plonger un peu plus en détail dans des notions vues par exemple.

De plus, le support évoluant dans le temps, il est possible de vérifier l'existence de nouvelles version directement sur le lieu de stockage en ligne de celui-ci : [https://github.com/codlab/cours_algo-](https://github.com/codlab/cours_algo-). Se référer à la partie "license" pour plus de détail sur le contexte d'usage possible.

_Note : Ce document ne met pas en exergue, actuellement, la complexité des algorithmes. Ce point sera l'objet d'une mise à jour ultérieure_


# Introduction

L'algorithmique est une discipline importante dans chaque processus "techniques" d'un projet. Elle est la construction d'un raisonnement logique dont le but est d'arriver, à partir d'un ensemble de composants de bases de produire, à résoudre des problèmes purement mathématiques.

# Algorithmes & projet

## Des spécifications ...

Dans une certaine mesure, elle a aussi sa place dans les processus itératifs de décisions et de gestions d'un projet après les étapes préalables de création d'un cahier des charges fonctionnels, besoins et de découpage d'un projet.

Avant toute étape d'écriture d'algorithme, il ne faut jamais oublier qu'un algorithme n'est qu'une façon décrire de manière logique ce qui est déjà de façon plus ou moins explicite dans les besoins. En effet, de manière assez concrète au sein d'un projet, les processus mis en avant dans des systèmes de gestions de projets, modélisation UML, génie logiciel etc... tendent à "algorithmiser" un besoin émis par un "client" pour en extraire la logique.

## A l'abstraction

Ainsi, tout comme il est possible d'imaginer qu'un projet n'est qu'un ensemble de :
- étapes
- strates
- entonnoir

On peut de la même façon appliquer ce type de raisonnement à tout le processus de création mais aussi de l'architecture d'un algorithme !

Quelques bonnes pratiques pour garder à l'esprit cette logique :

- aucun algorithme avant d'avoir dessiné l'architecture et les "fonctions" élémentaires qui seraient nécessaires
- une fonction (un bloc dense) doit toujours être établi dans un contexte connu et un seul!
- une fonction doit rester lisible et relativement légère
- dans la mesure du possible, éviter une organisation complexes
- un problème n'est qu'un ensemble de sous problème ! Toujours essayer de factoriser la logique

# Pseudo-Code

## Exalgo

Les projets, les algorithmes et les programmes ayant un cycle de vie, il ne faut donc pas oublier que le développeur peut évoluer dans différents contextes :
- seul ou à plusieurs sur le projet
- quid de la gestion dans le temps ?
- qui lira le code dans le présent ? le futur ?

Toute la problématique dans l'écriture d'un algorithme est donc d'arriver à concevoir un code "lisible" qui soit abstrait et la jonction entre le monde des langages naturels par nature ambigüs et des langages logiques sans ambigütés.

C'est ici qu'une forme est proposée par le monde la recherche. Exalgo est un langage proposé afin de tenter de résoudre ces problématiques d'abstraction de certains éléments d'implémentation (Python versus Javascript versus C versus Java, etc...). Ecrit en France, un alrogithme écrit en Exalgo ne se limite tout de même pas à la forme qu'est donné par sa documentation. En effet, l'algorithme écrit en Exalgo restant relativement "haut niveau", il est possible de se donner quelques libertés (notamment en cas d'oublis). Gardez à l'esprit de toujours rester cohérent sur la façon d'écrire des éléments de logiques.

### Lexique du langage

De nombreuses pages issues du Labri et des documentations complètes sont disponibles en ligne pour permettre d'appréhender la mise en place et en forme. Par exemple sur [https://www.labri.fr/perso/robson/cours/exalgo.html](https://www.labri.fr/perso/robson/cours/exalgo.html)

*Attention : ce support ne contient pas encore une liste exhaustive des instructions "utilisables" en algorithme tel que présentait pendant les interventions, néanmoins le lien précédent suffit actuellement.*

### Selon que

Si on reprend l'idée d'une structure conditionnelle comme vue durant l'intervention, on peut noter au moins 2 cas d'utilisation de conditions :
```
si ... alors
  ...
sinon
  ...
fin si
```

et

```
si ... alors
  ...
sinon si ... alors
  ...
sinon si ... alors
  ...
sinon
```

Ici, les "si sinon si sinon" peuvent prendre énormément de types de conditions en attente (réduction de valeurs booléennes). Le selon que est intéressant pour tester dans une variable un ensemble de valeur possible de celle-ci. On la note :

```
selon que ma_variable est
  cas VALEUR1:
    //faire une action
    sortir
  cas VALEUR2:
    //faire une autre action
    sortir
  cas VALEUR3:
  cas VALEUR4:
    //faire une dernière action
    sortir
  cas VALEUR5:
  par défaut :
    //rien - par exemple
fin selon que
```

Ne pas oublier d'utiliser le mot clé "sortir" afin de vous assurer que le programme n'executera pas les blocs des selon que suivant (se souvenir qu'un des reliquats de l'ère des "labels" se retrouve dans cette notation du selon que).


### Apports & philosophie

Tout l'intérêt d'Exalgo réside donc dans :

- sa capacité à pouvoir être lu par n'importe quelle personne (si l'algorithme est conforme aux spécifications ET simple*!)
- sa tendance à pouvoir être exécuté et testé mentalement par un développeur
- son support papier ! format A4 de préférence
- son lexique relativement léger

* la simplicité restera toujours assez abstrait mais en gardant à l'esprit de factoriser, aérer, nommer convenablement et documenter, la simplicité devrait se faire sentir.

## Algorigrammes

### Forme

L'algorithmique avancée n'est pas uniquement de savoir effectuer une recherche en temps logarithmique ou d'optimiser un système de stockage en base de donnée avec un système de hash permettant de retrouver rapidement 1 parmi N serveurs. Elle est aussi, et bien peu souvent mis en avant, la capacité à représenter un algorithme dans une forme qui soit la plus visuelle et optimisée pour qu'un être humain puisse :

- **détecter** des erreurs de compréhension
- **détecter** des erreurs de compréhension
- **détecter** des optimisations

### Factorisation

On parle de factorisation de code dès qu'il est possible d'utiliser un bloc de code d'une même manière (à la variable près) dans un autre environnement du programme. On parle alors du processus qui consiste à extraire ce code dans une fonction qu'il s'agit d'une refactorisation.

Dans l'idéal, de telles factorisation du code doivent intervenir dès que sa lecture devient soit trop dense soit contextuellement intéressante.

### Synchrone versus Asynchrone

On a tendance à imaginer que l'asynchronicité est un fardeau dans l'implémentation de projets. Hors, en gardant à l'esprit que toute logique asynchrone n'est qu'un algorithme possèdant de multiples branches dans un contexte de "boucle" permet d'imaginer aisément une implémentation.

Voici quelques étapes pour permettre cette résolution :

- identifier tous les points "asynchrones" nécessitant d'être mis en place
- chaque point = 1 fonction avec 1 entrée et 1 sortie
- les appels à ses fonctions sont possible via un "selon que"
- le selon que est appelé advitam aeternam par une boucle sans fin

Ces étapes ne sont pas à "indiquer" à proprement parler mais sont là pour faciliter le processus intellectuel avant la mise sur papier des algorigrammes et algorithmes.

Dans la même mesure, on peut utiliser ces méthodes dans les étapes de distribution / traitements parallèles (un traitement parallèle avec barrière n'étant qu'une étape de traitements séquentielle - attention tout de mme aux effets de bord ;) )

## Mise en place

### Boites noires & organes

Pour schématiser un peu plus ce qu'un algorigramme doit pouvoir mettre en exergue c'est tout simplement qu'un programme/projet est une boîte dont l'intérieur est "opaque", avec plusieurs points d'entrée et de sorties qui sont connus. Les algorithmes sont eux, des articles scientifiques ou rapports qui permettent de décrire les organes élémentaires de cette boîte noire.

Les algorigrammes vont eux décrire schématiquement les éléments, les groupes de fonctions, les organes, etc...

Voici une liste des éléments de base suffisamment pour écrire la quasi totalité des algorithmes sous cette forme :

![Image](https://github.com/codlab/cours_algo-/blob/master/algorigramme.png?raw=true)

### Implémentation & amélioration continue

Bref,

_Un algorigramme qui se lit aisément implique un algorithme qui s'implémente aisément_

Dans le cadre d'un projet, toutes les techniques d'améliorations continues doivent aussi s'appliquer sur les algorithmes ! Ne pas oublier que les algorigrammes et algorithmes que vous allez écrire sont un parfait moyen de tenir une documentation saine et cohérente pour un projet.

**Note : On peut notamment imaginer qu'un algorigramme remplace toute velléité d'insérer des blocs de codes dans un rapport technique**

# Cas d'usage

_Pour changer et aller plus vite, plus loin, il est proposé de travailler sur la technologie blockchain avec le prisme de l'ERC20 pour Ethereum_

## Manipulation de types de données autour des tableaux

exemples de tableaux dans un style "haut niveau" (c'est-à-dire que les langages, implémentations, traitements abstraient un maximum la logique de la gestion mémoire d'un tableau jusqu'à sa destruction - on retrouve cette vision dans des langages comme le JavaScript):

```
var tableau_de_resultats: tableau d'entier = []
```
ou si il contient des valeurs
```
var tableau_de_resultats: tableau d'entier = [10, 5, 4]
```

obtenir la taille d'un tableau : `taille(<tableau>)`

si besoin d'allocation d'un tableau
```
var tableau_de_prenoms: tableau de chaine de caracteres = allouer(50)
tableau_de_prenoms[0] = "claire"
tableau_de_prenoms[1] = "leopold"
```

### Manipulation d'un tableau

Etant donné la nature de ce support dalgorithmie, on se propose de donner dans la suite, une définition "algorithmique" des traitements sur un tableau

5 méthodes de bases :
- allouer
- récupérer
- ajouter
- modifier
- supprimer

_Noter que ces 5 traitements sont habituellement retrouvable pour tout type de structure ou de classes. En effet, l'allocation, ajout, modification, supression etc... sont des traitements bien souvent nécessaires pour gérer toute interaction avec un objet_


- allouer :
tableau = allouer(50) ou tableau = [] ou tableau = [5, 10, ....]

- récupérer
tableau[2] ou tableau[indice]

- ajouter
dans le format "souple" (haut niveau) :
pousser(<tableau>, <valeur>)

exemple :
var tableau: tableau d'entier = []
pousser(tableau, 50)
//tableau = [50]
pousser(tableau, 9)
//tableau = [50, 9]

var tableau: tableau de tableau d'entier = []
var colonne_1: tableau d'entier = [10, 5]
var colonne_2: tableau d'entier = [1]

pousser(tableau, colonne_1)
//tableau = [ [10, 5] ]
pousser(tableau, colonne_2)
//tableau = [ [10, 5], [1] ]

Ici, nous allons déclarer l'algorithme qui permet à bas niveau d'avoir une gestion haut niveau :
- ici manipuler le tableau avec une autre variable "indice"

```
type Tableau
debut
  tableau: tableau
  taille: entier
  taille_maximale: entier
fin type

fonction allouer(taille_tableau: entier): Tableau
debut
  var nouveau_tableau: Tableau = allouer()
  nouveau_tableau.tableau = allouer(nouvelle_taille)
  nouveau_tableau.taille = 0
  nouveau_tableau.taille_maximale = nouvelle_taille

  retourner nouveau_tableau
fin

fonction copie(tableau_out: Tableau, tableau_in: Tableau)
debut
  pour variable indice de 0 à tableau_in.taille
  debut
    pousser(tableau_out, tableau_in.tableau[indice])
  fin
fin

fonction pousser(tableau: Tableau, contenu)
debut
  var indice: entier = tableau.taille
  si indice >= taille_maximale
    var nouvelle_taille: entier = (tableau.taille + 1) * 2
    variable tableau_final: Tableau = allouer(nouvelle_taille)

    copie(tableau_final, tableau)

    detruire(tableau.tableau)
    tableau.tableau = tableau_final.tableau
    tableau.taille_maximale = tableau_final.taille_maximale
  fin si

  tableau.tableau[indice] = contenu
  tableau.taille = indice + 1
fin
```

De fait, nous pouvons maintenant, avec notre notation "bas niveau", nous permettre de simplifier l'écriture de nos algorithmes
```
var tableau: Tableau = allouer()
pousser(tableau, 2)
```


- supprimer

```
fonction supprimer(tableau: Tableau, indice: entier)
debut
  si tableau.taille > indice
    pour index de indice à tableau.taille - 2
    debut
      tableau.tableau[index] = tableau.tableau[index + 1]
    fin pour
    tableau.taille = tableau.taille - 1
  fin si
fin
```

- modification

```
tableau[0] = 1
```

*Pour aller plus loin : Il peut être envisagé de faire évoluer les fonctions de modifications pour prendre en compte des cas d'erreur : tentative d'accès en dehors du tableau, modification à un indice qui n'existe pas encore etc...*

## Création d'une liste chaînée

Une liste chaînée est un type particulier que nous nous proposons d'implémenter ici.

Dans l'idée il s'agit de blocs qui se suivent les uns à la suite des autres. On parle de liste chaînée "avant" ou liste chaînée "arrière" en fonction du lien des blocs les uns avec les autres.

Par exemple :

```
type Noeud:
enreg
  valeur: entier
  suivant: Noeud
finenreg

type Liste:
enreg
  tete: Noeud

  Liste()
  ajouter(valeur: entier): Liste
  supprimer(index: entier): Liste
  modifier(index: entier, valeur: entier): Liste
finenreg
```



### fonction allouer
```
fonction Liste::Liste()
debut
  liste.tete = vide
fin
```

### fonction ajout
```
fonction Liste::ajouter(element: entier): Liste
debut
  var noeud: Noeud = nouveau Noeud();
  noeud.valeur = element;
  noeud.suivant = vide;

  var tete: Noeud = soit_meme.tete;

  si tete est non vide
  debut
    tant que tete.suivant est non vide
    debut
      tete = tete.suivant
    fin

    tete.suivant = noeud;
  sinon
    liste.tete = noeud;
  fin si

  retourner soit_meme
fin

var liste: Liste = nouvelle Liste();
liste.ajouter(10)
     .ajouter(20)
```

### fonction suppression
```
fonction supprimer(index_cible: enter): Liste
debut
  si soit_meme.tete est non vide
  debut
    var index: entier = 0;
    var noeud: Noeud;

    tant que noeud.suivant est non vide et index < index_cible
    debut
      si index == index_cible - 1
      debut
        var noeud_supprime: Noeud = noeud.suivant
        noeud.suivant = noeud.suivant.suivant

        libérer noeud_supprime
      find

      noeud = noeud.suivant
      index ++
    fin


  fin si
fin
```

### fonction modification
```
fonction modification(index: entier)
debut
  si soit_meme.tete est non vide
  debut
    var index: entier = 0;
    var noeud: Noeud = soit_meme.tete;

    tant que noeud est non vide et index < index_cible
    debut
      noeud = noeud.suivant
      index ++
    fin

    si noeud est non vide
    debut
      noeud.valeur = valeur
    find

  fin si
fin
```

### Modification pour une liste chaînée arrière

Le block de tête connait son "précédent", les manipulations de la liste vont donc "contextuellement" servir pour des listes qui évoluent dans le temps par exemple où le dernier élément à une importance plus grande que le tout premier ajouté. Il ne s'agit ici surtout que du résultat d'un choix de nommage dans le cadre d'un contexte donné à un problème !

Quelques exemples d'implémentations de fonctions pour manipuler cette liste

```
fonction ajouterEnTete(liste: Liste, block: Block)
debut
  block.precedent = liste.tete
  liste.tete = block
fin
```

```
fonction ajouterEnQueue(liste: Liste, block: Block)
debut
  si liste.tete == vide alors
    liste.tete = block
  sinon
    var block_actuel: Block = liste.tete
    tant que block_actuel.precedent != vide
      block_actuel = block_actuel.precedent
    fin tant que

    block_actuel.precedent = bloc
  fin si
fin
```

## Arbre & Cartographie

### Arbres

### Cartographie

```
type Coordonnées:
debut enreg
  latitude: flottant
  longitude: flottant
finenreg

type Utilisateur:
debut enreg
  identifiant: chaine de caractères
  coordonnées: Coordonnées
finenreg

type Noeud:
debut enreg
  utilisateurs: Liste d'Utilisateur
  centre: Coordonnées
  taille: entier
  zones: Tableau de Noeud
  niveau: entier

  autour(utilisateur: utilisateur, rayon: flottant) : Liste d'Utilisateur
finenreg

type Arbre hérite de Noeud
debut enreg
  //autour est surchargé par Arbre
finenreg
```
```

fonction autourDeZone(utilisateur: Utilisateur, utilisateurs: Liste d'Utilisateur,
                rayon: flottant): Liste d'Utilisateur
debut
  constante resultat = nouveau Tableau()

  pour chaque element de la liste utilisateurs
  debut
    si distance(utilisateur, element) < rayon
      resultat.ajouter(utilisateur)
  fin

  retourner resultat
fin

fonction Noeud::autour(utilisateur: Utilisateur, rayon: flottant, utilisateurs: Liste d'Utilisateur)
debut
  si n'est pas ADistance(utilisateur, rayon)
  debut
    retourner
  fin si

  si soit_meme.zones est vide
    constante trouvés = autourDeZone(utilisateur, soit_meme.utilisateurs, rayon)
    utilisateurs.ajouterTout(trouvés)
  sinon
    soit_meme.zones[0].autour(utilisateur, rayon, utilisateurs)
    soit_meme.zones[1].autour(utilisateur, rayon, utilisateurs)
    soit_meme.zones[2].autour(utilisateur, rayon, utilisateurs)
    soit_meme.zones[3].autour(utilisateur, rayon, utilisateurs)
  fin sinon
fin


fonction Arbre::autour(utilisateur: Utilisateur, rayon: flottant): Liste d'Utilisateur
debut
  constant utilisateurs = nouveau Liste d'Utilisateur
  soit_meme.autour(utilisateur, rayon, utilisateurs)
  retourner utilisateurs
fin

fonction Noeud::pousser(utilisateur: Utilisateur)
debut
  soit_meme.utilisateurs.pousser(utilisateur)
fin

fonction Noeud::dispatcher(utilisateurs_max_par_zone: entier): Liste de Noeud
debut
  si soit_meme.utilisateurs.taille > utilisateurs_max_par_zone
  debut
    soit_meme.zones = nouveau Tableau de Noeud()
    pour i de 0 à 3 par pas de 1
    debut
      soit_meme.zones.ajouter(nouveau Noeud(/* mettre les paramètres de description*/))
    fin

    pour chaque utilisateur de utilisateurs
    debut
      pour chaque zone de soit_meme.zones
      debut
        si zone.appartient(utilisateur)
        debut
          zone.pousser(utilisateur)
          sortir_boucle
        fin
      fin
    fin

    soit_meme.utilisateurs.vider()

    pour chaque zone de soit_meme.zones
    debut
      zone.dispatcher(utilisateurs_max_par_zone)
    fin
  fin si

  retourner soit_meme.zones
fin


fonction Arbre::initialiser(utilisateurs: Liste d'Utilisateur, utilisateurs_max_par_zone: entier)
debut
  soit_meme.dispatcher(utilisateurs_max_par_zone)
fin

fonction Noeud::dispatcher(utilisateurs: Liste d'Utilisateur, utilisateurs_max_par_zone: entier)
debut
  soit_meme.utilisateurs = nouveau Liste d'Utilisateur()

  pour chaque utilisateur de utilisateurs
  debut
    si soit_meme.appartient(utilisateur)
    debut
      soit_meme.utilisateurs.ajouter(utilisateur)
      utilisateurs.supprimer(utilisateur)
    fin
  fin

  si soit_meme.utilisateurs.taille > 1000
  debut
    soit_meme.zones = nouveau Tableau de Noeud()
    pour i de 0 à 3 par pas de 1
    debut
      soit_meme.zones.ajouter(nouveau Noeud())
      soit_meme.zones[i].dispatcher(soit_meme.utilisateurs, utilisateurs_max_par_zone)
    fin
  fin si
fin
```

## Algorithmes de tri


**Gros TODO sur cette partie**
**N'hésitez pas à effectuer une ouverture de ticket si la priorité doit être donné à cette partie ou si'il y a un oubli de ma part !**

### Tri par bulle

### Tri par sélection

### Tri par arbre binaire de recherche


## Transformation de blocs vers un "ledger" de transactions

Ce cas présente l'utilisation d'une bibliothèque qui permettrait à un programme d'intéragir avec le réseau de la blockchain Ethereum pour transformer les blocs synchronisés vers une base de donnée à partir de laquelle un service web pourrait lire les transactions d'une adresse, recherche de data etc...

```
fonction obtenirNumeroBlock(): entier
fonction obtenirBlock(numero: entier, avec_transaction: booleen): Block

fonction formaterTransaction(): tableau de chaine de caractere
fonction enregistrerEnBaseDeDonnee(tableau: tableau de chaine de caractere)


fonction synchroniser()
  var indice: entier = 0
  tant que vrai
    const nombre_block: entier = obtenirNumeroBlock()

    tant que indice <= nombre_block
      const block: Block = obtenirBlock(indice, vrai)

      pour tout transaction de block.transactions
        const transaction_formattee: tableau de chaine de caracteres = formaterTransaction(transaction)
        enregistrerEnBaseDeDonnee(transaction_formattee)
      fin pour

      indice = indice + 1
    fin tant que

    attendre(8) //secondes
  fin tant que
fin
```

## Création d'un token

La création de token dans une blockchain :
[https://theethereum.wiki/w/index.php/ERC20_Token_Standard](https://theethereum.wiki/w/index.php/ERC20_Token_Standard)

# Pour aller plus loin !

Je vous propose d'aller plus loin et de travailler sur :

- la création d'une calculatrice simple
  - cette calculatrice demandera successivement à un utilisateur de rentrer 1 nombre, un opérateur et un 2eme nombre pour faire un résultat intermédiaire avant de continuer par un nouvel opérateur etc... Notez l'usage d'une boucle
  - mettre un maximum d'opérateurs RESULTAT = VALEUR OPERATEUR VALEUR (division, multiplication, soustraction, addition, etc...)
  - vous pouvez partir du principe que des fonctions existent déjà et vous permettent de lire un nombre, une chaine de caractère - à vous de choisir un nom "explicite" et "cohérent" avec leur tâche
  - prenez vos téléphones et faites beaucoup de croquis du fonctionnement, la clé d'un bon algorithme reste encore une bonne modélisation d'un problème

- la création d'une calculatrice plus évoluée
  - en reprenant la calculatrice précédente, implémentez la gestion des parenthèses ( et ) pour la gestion de priorités
  - analysez bien les appels de fonctions que vous allez déclarer pour gérer la demande d'opérateur, de nombre, de parenthèses et les appels récursifs des uns dans les autres (oups, spoiler alert!)

- aller plus loin encore ! Vous vous souvenez de la fonction de lecture d'un nombre ou d'un opérateur ? Elles n'existent pas forcément dans la vie réelle, donc à partir d'une simple fonction qui elle donne une chaine de caractère et qui existerait réellement, proposez une implémentation de 2 fonctions qui donneraient un `nombre relatif` et un `operateur`

- parce que travailler sur des ABR (Arbre Binaire de Recherche) et des tableaux reste sympathique, imaginez une solution de recherche dans un tableau trié par la technique de la dichotomie. De la même manière, implémentez un tri par dichotomie d'un tableau via l'ajout d'un ABR "en dehors" de ce tableau.

# Mises à jour

Les pull-requests sont acceptés. La logique de validation reste dans le spectre de :

- corrections proposées
- amélioration des visuels
- ajout d'éléments de notions abordées

Processus :

- création d'un pull request *(optionnel)*
- ouverture d'une pull request
- titre & description explicite de l'amélioration souhaitée/proposée
- validation et ajout dans la branche principale du projet

## Contactez-moi

Vous pouvez me contacter directement sur mon adresse mail : kevin.leperf@nonopn.com

# Licenses

Repository sous license GPL v3
L'ensemble des documents écrits qui seraient directement extrait de ce dépôt le sont sous license Creative Commons CC BY-NC-SA
