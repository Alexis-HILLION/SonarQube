﻿# Règles applicables à SonarQube

Listing des règles applicables à SonarQube et facilement scannable sur un code static.

Référence discussion Google Group : [Soutiens de l'entreprise Davidson Consulting (google.com)](https://groups.google.com/g/ecoconceptionweb/c/O5OwuLuIbXc/m/TP6Y8ns2AgAJ)

Les règles s'appuient sur l'édition 3 du livre "Ecoconception Web / Les 115 bonnes pratiques" :
[Eco-conception Web : Les 115 bonnes pratiques (greenit.fr)](https://collectif.greenit.fr/ecoconception-web/115-bonnes-pratiques-eco-conception_web.html)

## Conditions des règles applicables

Une règle applicable à SonarQube doit suivre les conditions suivantes :

 - Elle peut être analysée au sein d'un code static
 - Elle doit être facilement scriptable et renvoyer une seule réponse (booléen : TRUE/FALSE)

## Liste de règles de "Mauvaises pratiques Green"

| Intitulé  | Référence "115" | Catégorie | Priorité | Pondération | Niveau de complexité de réalisation | Exemple / Commentaire |
|--|--|--|--|--|--|--|
| Utiliser les boutons officiels de partage des réseaux sociaux | 19 | Technique / Conception | 2 | 2 | | |
| Inclure un fichier CSS contenant des directives non utilisées sur une page | 21 | Templating / CSS | 1 | 3 | | Afin de réduire le nombre de requêtes HTTP |
| Déclarations CSS similaires non groupées | 25 | Templating / CSS | 1 | 3 | | Ne pas écrire : `h1 { background-color: gray; color: navy; } h2 { background-color: gray; color: navy; } h3 { background-color: gray; color: navy; }` mais plutôt : `h1, h2, h3 { background-color: gray; color: navy; }`|
| Notations CSS abrégées non utilisées | 26 | Templating / CSS | 1 | 3 | | Ne pas écrire : `margin-top:1em; margin-right:0; margin-bottom:2em; margin-left:0.5em;` mais plutôt : `margin:1em 0 2em 0.5em;` |
| CSS print non inclus | 27 | Templating / CSS | 1 | 3 | | Réduction du nombre de pages imprimées |
| Polices utilisées non standards | 29 | templating / Front | 1 | 3 | | |
| CSS et Javascript non externalisés | 32 | Templating / HTML | 1 | 3 | | Les codes CSS et JavaScript ne doivent pas être embarqués dans le code HTML de la page |
| Balises images contenant un attribut SRC vide | 33 | Templating / Images | 1 | 3 | | |
| Utiliser des images vectorielles non optimisées | 36 | Templating / Images | 1 | 3 | | Supprimer les informations de couche (layer), les commentaires, etc. |
| Utiliser un trop grand nombre d'animations CSS / javascript | 39 | Code client / CSS/Javascript| 1 | 3 | | **/!\ Nécessité de définir un palier du nombre d'animations trop important**|
| Modifier le DOM lorsqu'on le traverse | 41 | Code client / DOM | 1 | 3 | | |
| Modifier les éléments du DOM dans le rendre invisible | 42 | Code client / DOM | 2 | 2 | | |
| Modifier une propriété CSS directement | 45 | Code client / Javascript | 1 | 3 | | Privilégier la modification de classes CSS |
| Utiliser les appels à try...catch...finally | 47 | Code client / Javascript | 3 | 1 | | privilégier les tests logiques |
| L'emploi de méthodes pour les opérations de base | 48 | Code client / Javascript | 3 | 1 | | Privilégier les opérations primitives |
| Appeler un élément du DOM plusieurs fois sans mise en cache | 49 | Code client / Javascript | 1 | 3 | | |
| Utiliser les variables globales | 50 | Code client / Javascript | 3 | 1 | | |
| Utiliser les strings en arguments à SetTimeout() et setInterval() | 52 | Code client / Javascript | 1 | 3 | | |
| Utiliser les boucles for...in | 53 | Code client / Javascript | 2 | 2 | | |
| Réécrire les getter/setter natifs | 62 | Code serveur / Serveur d'applications | 2 | 2 | | |
| Assigner inutilement des valeurs aux variables | 63 | Code serveur / Serveur d'applications | 3 | 1 | | |
| Utiliser la variable $i++ lors d'une itération | 67 | Code serveur / Serveur d'applications | 3 | 1 | | | privilégier ++$i |
| Appeler une fonction dans la déclaration d'une boucle de type for | 69 | Code serveur / Serveur d'applications | 1 | 3 | | |
| Effectuer une requête SQL à l'intérieur d'une boucle | 72 | Code serveur / Base de données | 1 | 3 | | |
| Ecrire SELECT * FROM | 74 | Code serveur / Base de données | 1 | 3 | | |
