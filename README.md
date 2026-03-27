# 🧩 Sudoku & Benchmark Solver

Une application de Sudoku complète et performante développée en Python. Ce projet ne se contente pas d'offrir une expérience de jeu élégante ; il sert également de plateforme de **benchmark** pour comparer différents algorithmes de résolution de problèmes de satisfaction de contraintes (CSP).

---

## 🚀 Fonctionnalités

### 🎮 Mode Joueur
- **Génération Dynamique :** Création de grilles valides et uniques à chaque partie.
- **Aide à la Saisie :** Détection des erreurs en temps réel (doublons en ligne, colonne ou bloc).
- **Interface Fluide :** Navigation au clavier (flèches directionnelles) et focus automatique.
- **Système de Victoire :** Validation automatique de la grille une fois remplie.

### ⚙️ Mode Benchmark (Solveur)
Comparez l'efficacité de trois approches algorithmiques :
1. **Force Brute (Lent) :** Exploration systématique, idéale pour comprendre les limites de la récursion simple.
2. **Backtracking Classique :** Algorithme récursif avec élagage de l'arbre de recherche.
3. **MRV Optimisé (Rapide) :** Utilise l'heuristique *Minimum Remaining Values* pour résoudre la grille en un temps record.

### 📊 Monitoring Système
- **Chronométrage de précision :** Temps de résolution calculé au dix-millième de seconde.
- **Stats Ressources :** Affichage de l'utilisation du CPU (%) et de la RAM (GB) durant le calcul grâce à `psutil`.

---

## 📂 Structure du Projet

| Fichier | Rôle |
| :--- | :--- |
| **`main.py`** | Interface graphique (GUI) construite avec `CustomTkinter`. |
| **`sudoku_engine.py`** | Logique métier : génération, initialisation et vérification des règles. |
| **`force_brute_dichotomique.py`** | Implémentation de l'algorithme optimisé (SudokuOptimise / MRV). |
| **`backtracking.py`** | Algorithme de résolution par retour sur trace standard. |
| **`force_brute.py`** | Algorithme de recherche exhaustive. |
| **`infos.py`** | Gestion du temps et récupération des métriques système. |

---

## 🛠️ Installation & Lancement

### Prérequis
- Python 3.8+
- Les bibliothèques suivantes :
  ```bash
  pip install customtkinter psutil
