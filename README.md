# Projet de Reconnaissance de la Parole BE2


## Technologies Utilisées
- Python 3.9.12
- Librairies : NumPy, Librosa, Matplotlib, SciPy

## Partie 1

Ce projet implémente un système simple de reconnaissance de mots isolés en anglais. Le système utilise une paramétrisation du signal de parole à l'aide des coefficients LPC (Linear Predictive Coding) et une reconnaissance basée sur l'algorithme des k plus proches voisins (k-NN), en utilisant la distance élastique (Dynamic Time Warping - DTW).

### Étape 1 : Lecture des Fichiers Audio
Les fichiers audio sont lus et stockés à partir d'un dossier spécifié. Chaque fichier audio correspond à un chiffre prononcé en anglais par différentes personnes.

### Étape 2 : Calcul des Coefficients LPC
Les coefficients LPC sont calculés pour chaque fichier audio pour paramétrer les signaux de parole. Ces coefficients servent de caractéristiques pour la reconnaissance de la parole.

### Étape 3 : Calcul de la Matrice des Distances DTW
Une matrice de distances DTW est calculée pour toutes les paires de séquences LPC. Cette matrice mesure la distance élastique entre chaque paire de signaux, en tenant compte des variations de vitesse et de prononciation.

### Étape 4 : Séparation des Données en Ensembles d'Entraînement et de Test
Les données sont divisées en ensembles d'entraînement et de test. Les étiquettes correspondantes sont également préparées pour chaque ensemble.

### Étape 5 : Classification k-NN
L'algorithme des k plus proches voisins est utilisé pour classer les données de test en fonction de leur distance aux données d'entraînement. La classification est réalisée pour différentes valeurs de k, et les performances sont évaluées en termes d'exactitude, de rappel et de score F1.

### Étape 6 : Visualisation des Performances
Les performances du modèle pour différentes valeurs de k sont visualisées à l'aide de graphiques, montrant l'exactitude, le score F1 et le rappel.


## Conclusion de la partie 1
Cette première partie du projet démontre la mise en place d'un système de base pour la reconnaissance de mots isolés en utilisant des méthodes
