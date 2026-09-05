# 🎲 Le compte est bon !

Un petit jeu de calcul mental inspiré du **compte est bon**, pensé pour un niveau **CE2** (additions, soustractions et multiplications faciles). Développé sous forme d'une **application web autoportante** (un seul fichier HTML), sans dépendance ni installation.

## 🎯 Principe du jeu

1. On lance **5 dés verts** (valeurs de 1 à 6).
2. Un algorithme calcule un **nombre à trouver** (toujours entre 10 et 90), obtenu en combinant certains des nombres tirés avec des additions, soustractions ou multiplications adaptées au niveau CE2.
3. Le joueur sélectionne deux nombres, puis une opération (**+ − ×**) pour les combiner. La soustraction est toujours calculée du plus grand vers le plus petit (jamais de résultat négatif).
4. Il recommence jusqu'à obtenir une valeur qui correspond au nombre à trouver, puis clique sur **Valider mon nombre**.
5. Un bouton **Voir une solution** permet d'afficher un exemple de calcul en cas de blocage.
6. Chaque compte exact rapporte une ⭐.

## 🖥️ Utilisation

Aucune installation : ouvrir le fichier `compte-est-bon.html` dans n'importe quel navigateur.

## 🛠️ Stack technique

- HTML / CSS / JavaScript vanilla, **fichier unique autoportant**
- Aucune dépendance externe (hormis les polices Google Fonts, chargées via CDN)
- Compatible ordinateur, tablette et mobile

## 📝 Changelog

### v1.2.0
- Correction définitive : si aucun nombre ≥ 10 n'est atteignable avec les dés tirés, les dés sont relancés automatiquement jusqu'à obtenir un tirage valide (suppression de l'ancien secours qui pouvait produire un nombre trop faible, ex. 3 × 3 = 9).

### v1.1.0
- Le nombre à trouver ne peut plus être inférieur à 10, pour éviter des comptes trop simples.

### v1.0.0
- Version initiale : lancer de 5 dés, génération automatique du nombre à trouver, combinaison des nombres par +, − et ×, validation, indice/solution, score en étoiles.