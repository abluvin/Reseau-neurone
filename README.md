﻿# Reseau-neurone

Partie 1 : neurone artificiel
Définition:
Un neurone artificiel est l'unité de base d'un réseau de neurones. Il reçoit des entrées pondérées, effectue
un calcul sur ces entrées, ajoute un biais, applique une fonction d'activation et produit une sortie. Les
éléments clés d'un neurone artificiel sont les suivants :
• Poids : Les poids (des réels) sont des coefficients associés à chaque entrée. Ils déterminent
l'importance relative des différentes entrées pour le neurone.
• Biais ou seuil: Le biais est un terme constant ajouté au résultat de la somme pondérée des entrées.
Il permet de déplacer la fonction d'activation. Dans le cadre de ce projet, on considère le biais
comme un seuil d’activation du neurone. On se place donc dans le domaine discret.
• Fonction d'activation : La fonction d'activation est une fonction mathématique qui prend en
entrée la somme pondérée des entrées et du biais, et produit la sortie du neurone. Elle introduit
la non-linéarité dans le modèle et permet au neurone de capturer des relations complexes.
Questions:
On considère un neurone artificiel comme étant composé d’une liste de poids (des entiers) et d’un biais
(un entier). Écrire l’algorithme et le sous—programme C correspondant aux opérations suivantes :
1. InitNeur : permet de créer un neurone à partir d’une liste de poids et d’un seuil. Cette opération
doit prendre comme paramètre le nombre d’entrées du neurone.
2. Outneurone : permet de calculer la sortie d'un neurone artificiel en fonction d’une liste d’entiers
(liste des valeurs des entrées notées ei). Dans ce projet, on utilisera la fonction d'activation
suivante : f(x) = 1 si x >= seuil sinon 0 avec x=∑wiei,
wi : le ième poids de la liste des poids du neurone, ei : la ième entrée de la liste des valeurs des
entrées.


Partie 2 : Couche de neurones
Définition :
Une couche de neurones, dans un réseau de neurones artificiels, est un groupe de neurones similaires qui
effectuent généralement la même opération sur leurs entrées. Une couche de neurones est responsable
de la transformation des entrées en sorties à l'intérieur du réseau. La sortie de la couche de neurones
devient ensuite l'entrée de la couche suivante dans le réseau.
Questions:
On considère une couche comme une liste de neurones artificiels. Écrire l’algorithme et le sous—
programme C correspondant aux opérations suivantes :
1. InitCouche : permet de créer une couche et d’initialiser ses neurones. Cette opération doit
prendre comme paramètre le nombre de neurones de la couche et le nombre d’entrées de chaque
neurone. On suppose que tous les neurones d’une couche ont le même nombre d’entrées. Cette
opération réutilise l’opération InitNeur.
2. Outcouche : permet de calculer la liste des sorties d’une couche donnée en fonction de la liste des
entrées de chacun de ses neurones. La liste des sorties est composée des sorties des différents
neurones de la couche. En plus de la couche, cette opération prend comme paramètre la liste des
valeurs des entrées des neurones de la couche. A noter que cette liste est la même pour chaque
neurone de la couche. Cette opération réutilise l’opération OutNeurone


Partie 3 : Construction d’un réseau de neurones artificiel
Définition :
Un réseau de neurones artificiels est un modèle d'apprentissage automatique inspiré du cerveau humain.
Il est composé de neurones artificiels interconnectés, organisés en couches, et utilisés pour résoudre
diverses tâches d'apprentissage, telles que la classification, la régression, ou d'autres types de
modélisation de données.
Questions :
Un réseau de neurones est une liste de couches. Le premier élément de cette liste est la couche d’entrée
du réseau alors que le dernier élément est la couche de sortie du réseau. Les autres sont les couches
cachées (intermédiaires) du réseau. Écrire l’algorithme et le sous—programme C correspondant à
l’opération suivante :
1. CreerResNeur : Cette opération crée un réseau de neurones. Il doit prendre en compte le nombre
de couches et une liste contenant le nombre de neurones par couche.


Partie 4 : Principe de fonctionnement simplifié d’un réseau de neurone
Le fonctionnement (ou exécution) d’un réseau de neurones consiste en une succession d’opérations de
propagation avant et arrière permettant de converger vers des résultats proches de la réalité ou de la cible.
On se limite ici à la propagation avant qui consiste à calculer les sorties des neurones de la couche en
utilisant les entrées et les paramètres de la couche, et en appliquant lesfonctions d'activation. Cela permet
de transmettre l'information à travers le réseau, couche par couche, depuis l'entrée jusqu'à la sortie. La
propagation avant dans le réseau consiste à calculer la sortie de sa couche finale.
Question
Etant donné un réseau de neurones, et des données (des entrées), écrire l’opération qui permet de
réaliser la propagation avant dans le réseau.


Partie 5 : Exemples de réseaux de neurones
Créer et tester les réseaux suivants :
Réseau ET : composé d’un neurone à n entrées. Chaque entrée a un poids égal à un. Le seuil du neurone
est égal à n.
Réseau OU : composé d’un neurone à n entrées. Chaque entrée a un poids égal à un. Le seuil du neurone
est égal à 1.
Réseau NOT : composé d’un neurone à une entrée de poids égal à -1. Le seuil du neurone est égal à 0.
Réseau multi-couches (A ET (non B) ET C) OU (A ET (non C)) : composé de plusieurs couches, et construit
à partir des réseaux précédents (sera expliqué en cours). 
