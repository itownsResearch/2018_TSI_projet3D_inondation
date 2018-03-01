# Modélisation de l'inondation de Lyon

## Analyse du sujet

Nous devons réaliser un site web pour visualiser en fonction du niveau de l'inondation de Lyon les bâtiments touchés (directement ou indirectement).

## Implémentation

- Modélisation d'une inondation pour la ville de lyon (niveau de l'eau)

- Création du menu de gestion du niveau de l'eau et des bâtiments
 - niveau de l'eau
 - affichage relatif au bâtiment
  - corespondance de la couleur
  - lien entre les bâtiments
  - logo selon type

- récupération des données d'un bâtiment (coordonnées, altitude minimun, type)

- liste des bâtiments (type, couleur, lien avec les autres bâtiments)

- gestion de l'affichage des bâtiments
 - inondé ou non (couleur)
 - type (couleur / logo)
 
- visualisation des liens entre les bâtiments

- bâtiments affectés par l'inondation (directe ou indirecte) 

    ex : inondation d'une centrale qui entraine une coupure d'électricité

## Problèmes

Isolation des données sur les bâtiments : ! Problèmes résolus !

Fichier Feature2Mesh fonction [coordinateToPolygonExtruded](https://github.com/iTowns/itowns/blob/master/src/Renderer/ThreeExtended/Feature2Mesh.js#L241-L284)

- pb 1 : les bâtiment sont tous regroupés en un seul mesh alors que nous avons besoin d'un mesh par bâtiments pour le projet (travail sur la couleur et la mise en place de lien entre les bâtiments ou logo) et de leur lier leurs propriétés
- pb 2 : la modification du Feature2Mesh.js n'entraine aucun changement dans l'affichage. Comment faire en sorte que les changements soient pris en compte ?

## Installation

Pour installer et exécuter notre projet il faut :

- cloner le repository

```sh
git clone https://gitlab.com/LSchlegel/itowns_inondation.git
```

- installer les modules

```sh
cd itowns_inondation && npm install
```

- construire le projet

```sh
npm run build
```

- et enfin lancer le serveur

```sh
npm start
```

Rendez-vous ensuite dans votre navigateur à [http://localhost:8080/examples/globe_wfs_extruded.html](http://localhost:8080/examples/globe_wfs_extruded.html)