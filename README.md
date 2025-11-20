# Projet Python : Morpion & 2048

Ce dépôt contient une implémentation en Python de deux jeux classiques :

- **Un morpion (Tic-Tac-Toe)** complet avec interface texte et version graphique basée sur des images.
- **Une version simplifiée du jeu 2048**, jouable entièrement dans le terminal.

Les deux jeux sont implémentés de manière pédagogique avec tests (`assert`) et fonctions modularisées.

---

## 1. Morpion (Tic-Tac-Toe)

Le code inclut les fonctionnalités suivantes :

- Génération d’un plateau vide  
- Vérification si une case est libre  
- Placement des symboles **X** et **O**  
- Affichage texte du plateau  
- Détection de victoire (ligne, colonne, diagonale)  
- Détection d’égalité  
- Partie contre un ordinateur qui joue aléatoirement  
- Version graphique avec génération d’images (croix, ronds, grille)

### Fonctions principales

- `plateau_vide()`  
- `videt()`  
- `jouex()` / `joueo()`  
- `dessine_plateaut()`  
- `gagnet()`  
- `pleint()`  
- `tourt()`  
- Version image : `dessine_plateaut_im()`, `tourt_im()`

### Exemple d’utilisation (console)

```python
from Code2048 import *
```

plateau = plateau_vide()
tourt(plateau, 1, 2)  # Le joueur joue puis l'ordinateur répond

Exemple d’utilisation (version image)

tourt_im(plateau, 0, 0)

2. Jeu 2048

Le fichier contient une version fonctionnelle du jeu 2048 avec :

    Génération d’un plateau initial aléatoire

    Déplacement des cases (haut, bas, gauche, droite)

    Fusion des cases identiques

    Apparition automatique d’un nouveau nombre après chaque mouvement

    Détection de victoire (2048 atteint)

    Détection de défaite (aucun mouvement possible)

    Affichage ASCII du plateau

Fonctions principales

    plat2048_ini()

    generation()

    plamvt()

    dessine_plateau2048()

    rempli2048()

    gagne2048()

    tour2048()

Exemple d’utilisation

- p = plat2048_ini()
- tour2048(p, "")   # Affiche le plateau initial

- tour2048(p, "h")  # Déplacement vers le haut
- tour2048(p, "g")  # Déplacement vers la gauche

Tests intégrés

Le fichier contient de nombreux assert permettant :

    de vérifier la validité des fonctions,

    de s’assurer que les règles du morpion et du 2048 sont respectées,

    de détecter automatiquement les comportements incorrects.
