<h1>Modélisation de l'inondation de Lyon</h1>

<h2>Analyse du sujet</h2>

Nous devons réaliser un site web pour visualiser en fonction du niveau de l'inondation de Lyon les bâtiments touché (directement ou indirectement).

<h2>Implementation</h2>

- Modélisation d'une inondation pour la ville de lyon (niveau de l'eau)

- Création du menu de gestion du niveau de l'eau et des bâtiments
 - niveau de l'eau
 - affichage relatif au batiment
  - corespondance de la couleur
  - lien entre les batiments
  - logo selon type

- récupération des données d'un bâtiment (coordonnées, altitude minimun, type)

- liste des batiments (type, couleur, lien avec les autres batiments)

- gestion de l'affichage des batiments
 - inonder ou non (couleur)
 - type (couleur / logo)
 
- visualisation des liens entre les bâtiments

- bâtiments affecter par l'inondation (directe ou indirecte) 

    ex : inondation d'une centrale qui entraine une coupure d'électricité

<h2>problèmes</h2>

isolation des données sur les batiments :

fichier Feature2Mesh fonction [coordinateToPolygonExtruded](https://github.com/iTowns/itowns/blob/master/src/Renderer/ThreeExtended/Feature2Mesh.js#L241-L284)

- pb 1 : les bâtiment sont tous regrouper en un mesh on a besoin d'un mesh par batiments pour le projet (travail sur la couleur et la mise en place de lien entre les batiments ou logo) et de leur lier leur propriété
- pb 2 : la modification du Feature2Mesh.js n'entraine aucun changement dans l'affichage. Comment faire en sorte que les changements soient pris en compte ?