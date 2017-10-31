# Cours d'Algorithmique++

Petit repo de documentation pour appréhender pleinement l'algorithmique

_Note : A l'heure actuelle, ce repository présente la structure des éléments qui vont/sont/seront (être) abordés_

- Introduction
- Algorithmes & projet
  - Des spécifications ...
  - A l'abstraction
- Pseudo-Code
  - Exalgo
  - Algorigrammes
- Mises à jour


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

### Implémentation & amélioration continue

Bref,

_Un algorigramme qui se lit aisément implique un algorithme qui s'implémente aisément_

Dans le cadre d'un projet, toutes les techniques d'améliorations continues doivent aussi s'appliquer sur les algorithmes ! Ne pas oublier que les algorigrammes et algorithmes que vous allez écrire sont un parfait moyen de tenir une documentation saine et cohérente pour un projet.

**Note : On peut notamment imaginer qu'un algorigramme remplace toute velléité d'insérer des blocs de codes dans un rapport technique**

# Cas d'usage

_Pour changer et aller plus vite, plus loin, il est proposé de travailler sur la technologie blockchain avec le prisme de l'ERC20 pour Ethereum_

## Domaine de définition

- voir ce qui a été fait sur la session de 2 jours - un complément va être mis en place assez rapidement -

## Création d'un token

- voir ce qui a été fait sur la session de 2 jours - un complément va être mis en place assez rapidement -

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

Vous pouvez me contacter directement sur mon adresse mail : kevin.leperf_Q_nonopn.com

# Licenses

Repository sous license GPL v3
L'ensemble des documents écrits qui seraient directement extrait de ce dépôt le sont sous license Creative Commons CC BY-NC-SA
