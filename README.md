# Documentation perceptron

# Titre du projet : Trust_Transact

# Problématique

La problématique spécifique résolue dans cet algorithme est d'identifier les transactions frauduleuses en fonction de différents attributs de la transaction.

# Présentation de l'algorithme
L'algorithme utilisé pour résoudre cette problématique est le PERCEPTRON.

Le perceptron est un algorithme de machine learning qui résout principalement des problématiques de classification binaire. Il est utilisé pour prendre une décision entre deux classes distinctes. Plus précisément, le perceptron est conçu pour résoudre des problèmes où on doit trouver une frontière de décision linéaire entre les classes.

# Description de l'algorithme

Dans cette version simplifiée, nous calculons un score pour chaque nouvelle activité en utilisant la moyenne des attributs de cette activité. Ensuite, nous comparons ce score avec la moyenne des attributs des activités que l'utilisateur a aimées dans son historique. Si le score est supérieur à la moyenne des attributs aimés, nous recommandons l'élément, sinon nous ne le recommandons pas.

# Illustration
/Users/mohamedmazuicloud.com/Documents/Hitema_projects/1*uzm-62Wq3J1JF1HwTMY4mg.png

# Installation et Utilisation
Pour tester les différentes versions de chacun des algorithmes, vous devez cloner ou télécharger le repository.

Installer premièrement numpy si cela n'a pas déjà été fait sur votre ordinateur, avec la commande suivante : 

pip install numpy

Ensuite installer scikit-learn avec la commande suivante:

pip install scikit-learn

Vous pouvez lancer ensuite le programme contenu dans Perceptron_normal dans votre emulateur Jupyter.

ou 

Ouvrez un terminal Python dans vscode et activez l'environnement notebook de votre choix.

Exécutez pip install -U ipykernel

Fermez et rouvrez VS Code et votre notebook. 
# Vues de l'éxécution de Perceptron_normal
