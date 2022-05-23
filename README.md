# Pro-fit
Conception d'une application proposant des substituts alimentaires sains dans le cadre d'un régime de sèche sportive
Lien des consignes académiques OpenClassRooms: https://openclassrooms.com/fr/paths/148/projects/628/assignment

## Présentation

Dans plusieurs disciplines sportives, la période de sèche correspond à un régime visant à perdre de la masse graisseuse en minimisant la perte de masse musclulaire.

Cette application cible toutes les personnes souhaitant à la fois augmenter (ou maintenir) leur masse musculaire et diminuer (ou maintenir) leur masse graisseuse.
L'application prendra en entrée un code barre et s'appuiera sur la base de donnée d'OpenFoodFacts pour proposer des substituts.

Exemple :

![image](https://user-images.githubusercontent.com/76253068/169880705-3af9bc5b-4d0d-4266-a1e6-19a73c94afdd.png)

## Bases de données :
La base de données d'OpenFoodFacts est disponible via ce lien:
https://s3-eu-west-1.amazonaws.com/static.oc-static.com/prod/courses/files/parcours-data-scientist/P2/fr.openfoodfacts.org.products.csv.zip

## Traitement et nettoyage de la base de données :

- Gestion des doublons
- Suppression des produits indisponibles en France
- Suppression des colonnes non pertinentes
- Gestion des nans
- Gestions des valeurs aberrantes


## DataViz :

### Analyse nutriscore :

![image](https://user-images.githubusercontent.com/76253068/169882198-29de01cf-ff9f-45e9-bf6d-6df3abb1e2eb.png)

- Catégories C, D et E largement majoritaires
- L’application sera plutôt sélective

### Analyse des taux de sucres :

![image](https://user-images.githubusercontent.com/76253068/169882243-c4c1ed61-b1c0-4245-abc0-d629e967fe78.png)
- Forte corrélation entre taux de sucre et nutriscore
- Distribution plus faible dans les catégories A et B
- L’application proposera des produits peu sucrés

### Analyse des taux de graisses saturées :

![image](https://user-images.githubusercontent.com/76253068/169882267-bed23f77-5d3c-4025-b50a-a1fbae8e9534.png)
- Forte corrélation entre taux de graisse saturée et nutriscore
- L’application proposera des produits avec peu de graisses saturées

### Analyse des taux caloriques :

![image](https://user-images.githubusercontent.com/76253068/169882296-339669ea-46a9-4049-a2f5-c7468f5b42d1.png)




### Analyse bivariée taux kcal/nutriscore :

![image](https://user-images.githubusercontent.com/76253068/169882319-9a2f357f-7214-4fd6-8f08-39d1114201bc.png)

- Forte corrélation entre taux calorique et nutriscore

### Analyse bivariée taux de protéine/nutriscore :

![image](https://user-images.githubusercontent.com/76253068/169882374-a7d775e2-d72f-45b4-a0f0-4bbe8a8c6442.png)

- Forte corrélation entre taux de protéine et nutriscore 
- Forte présence de produits protéinés dans la catégorie D
- L’application éliminera beaucoup de produits protéinés (probablement des viandes transformées)

### Analyse bivariée calorie/protéine :

![image](https://user-images.githubusercontent.com/76253068/169882409-53a7cb77-3a0c-4e8b-8210-77330eaf863f.png)

- Corrélation positive mais faible entre taux de protéine et taux calorique
- Les produits situés près de la ligne du bas du graphique sont les plus intéressants 
- Concentration plus élevée de produits autour du taux de 20g de protéines

![image](https://user-images.githubusercontent.com/76253068/169882432-86adaa16-e951-4cbf-ac0a-8ef55a3ffe3b.png)


Pour le rapport kcal/protéine les catégories A et B qui sont les plus intéressantes

## Test de l'application sur un produit trop calorique et peu protéiné :

![image](https://user-images.githubusercontent.com/76253068/169883394-35c1bc50-a3d6-48b6-b149-f208c56a81ff.png)

## Test de l'application sur un produit peu calorique mais peu protéiné :

![image](https://user-images.githubusercontent.com/76253068/169883646-29abe747-a285-4123-be94-ab0ee18e9c96.png)

## Test de l'application sur un produit adapté :

![image](https://user-images.githubusercontent.com/76253068/169883737-fa9c8fac-ef69-4d35-9fd3-023b4ed1aca7.png)

## Synthèse

![image](https://user-images.githubusercontent.com/76253068/169888104-88beeddc-a764-46e8-8729-2ae35889c286.png)
