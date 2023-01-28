# 1 er Partie : Data préparation 

![](images/Image1.png)

Le bouton appelle un sub dans VBA qui va écrire les différents tableaux contenant les rendements, SMA…

![](images/Image2.png)

Méthodes de rendements, SMA, standard déviation et Bollinger bands.

# 2e Partie Classe MLP :

Après étude, on remarque que la classe simple perceptron est égale à la classe MLP (1,1) donc à la fin de notre sujet, il ne reste que la classe MLP avec les différentes modifications comme à chaque fois redimensionner les poids, la sensitivité et les méthodes de calcul Than, sigmoid… En effet, dès la partie 2, on modifie notre simple perceptron qu’on va modifier dans la partie 3 et ensuite plus tard dans le MLP, donc nous avons décider de faire une grande classe MLP. Bien sûr, nous avons testé le simple perceptron et le MLP avec les 2 feuilles les correspondants et le tableau de perte et la courbe d’entropie associées à chacun des modèles et de leur matrice de confusion.

D’abord, on initialise nos poids aléatoirement puis viens la méthode Fordward qui va calculer tous nos outputs en fonctions de nos inputs en suivant la formule mathématique vu dans le document et donc faire une prédiction de chaque return.
Ensuite la méthode Backward qui vient mettre à jour les poids et la sensitivité du nœud en fonction de la véracité de notre prédiction par rapport au vrai return (0 et 1).

Donc on vient donc entrainer pour avoir le meilleur poids et sensitivité optimal pour la prédiction de nos rendements sur 80% de notre data. Puis on vient l’applique sur nos 20% restant qui sont les tests. On vient ensuite récupérer les pertes pour observer une perte constante à chaque itération.

# 3e Partie AR-GARCH Interface :

Ensuite il y a toutes les méthodes intermédiaires pour calculer exponentielle, fonction activation…

![](images/Image3.png)  

Ici on peut voir toutes les méthodes et notre classe MLP et toutes nos feuilles.

Donc dans les feuilles, nous avons celle présenté au-dessus avec les données de Google. Ensuite nous avons l’interface qui résume tout le code avec des boutons associés au code lié. Une feuille pour AR-GARCH solver, une AR-GARCH train test, un MLP et une feuille pour le Simple perceptron.

## Interface :

![Interface](images/Image4.png)  

## AR-GARCH Solver :

![](images/Image5.png)  

## AR-GARCH train test : 

![](images/Image6.png)  

Par rapport aux modules, nous avons le modules fonction lié à la page google avec les méthodes de rendements, sma…
Ensuite, nous avons un module « Search » qui permet de récupérer la date et le prix de google.

Ensuite un module « Affichage » pour print nos tableau et matrice de confusion.

![](images/Image7.png)  

Exemple d’affichage, je demande quelle matrice print sur quelle feuille, à quelle ligne et colonne.

Avec la conversion de « Asc » d’une lettre en nombre puis inversement d’un Integer a un string avec « Chr » je peux incrémenter mes lettres. 

![](images/Image8.png)  

Ensuite, un module pour résoudre mon AR-GARCH en utilisant une macro que j’ai nettoyer pour ne garder que l’essentiel.

![](images/Image9.png)  

Et enfin le module, interface qui permet d’une première part compute l’AR-GARCH train test et calculer la matrice de confusion et de le print dans la feuille interface avec le début du train et fin tout comme le test. Ce code est ensuite implémenté en bouton (voir la page interface).

Et la dernière implémentation est le MLP et simple perceptron, avec de même print du début et fin training test puis initialisation de la classe MLP et MLP (1,1) simple perceptron puis appelle des différentes méthodes de classes pour compute et enfin récupération des outputs pour comparaison avec les returns observés en implémentant la matrice de confusion, toutes ces méthodes sont appelées dans le module « function » et non réécrite. 

Pour être enfin print sur notre interface avec aussi le bouton interactif pour lancer le code. De plus, on regarde les pertes pour faire une entropie du modèle.

