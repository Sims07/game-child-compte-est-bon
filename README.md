# 🎲 Le compte est bon !

Un petit jeu de calcul mental inspiré du **compte est bon**, pensé pour un niveau **CE2** (additions, soustractions et multiplications faciles). Développé sous forme d'une **application web autoportante** (un seul fichier HTML), sans dépendance ni installation.

## 🎯 Principe du jeu

1. On lance **5 dés verts** (valeurs de 1 à 6).
2. Un algorithme calcule un **nombre à trouver** (toujours entre 10 et 90), obtenu en combinant certains des nombres tirés avec des additions, soustractions ou multiplications adaptées au niveau CE2.
3. Le joueur choisit un nombre, puis une opération (**+ − ×**), puis un second nombre — comme sur une calculette — et le calcul se fait aussitôt. La soustraction est toujours calculée du plus grand vers le plus petit (jamais de résultat négatif).
4. Il recommence jusqu'à obtenir une valeur qui correspond au nombre à trouver, puis clique sur **Valider mon nombre**.
5. Un bouton **Voir une solution** permet d'afficher un exemple de calcul en cas de blocage.
6. Chaque compte exact rapporte une ⭐.

## 🖥️ Utilisation

Aucune installation : ouvrir le fichier `compte-est-bon.html` dans n'importe quel navigateur.

## 🛠️ Stack technique

- HTML / CSS / JavaScript vanilla, **fichier unique autoportant**
- Aucune dépendance externe (hormis les polices Google Fonts, chargées via CDN)
- Compatible ordinateur, tablette et mobile

## 🖼️ Crédits image

- Texture de parchemin : *Old Parchment Paper* par cron, [OpenGameArt.org](https://opengameart.org/content/old-parchment-paper), licence CC0 (domaine public, réutilisation libre).

## 📝 Changelog

### v2.1.0
- Suppression de la bannière château (qui ne s'affichait pas de façon fiable et gaspillait de l'espace) et de la rangée baguette/balai, pour libérer beaucoup de place verticale en thème Poudlard.
- Une seule icône (le chapeau) reste en en-tête au lieu de deux.
- Tailles de police encore réduites (titre, sous-titre, nombre magique) pour mieux tenir sur petit écran.
- Correction de l'alignement des boutons (opérateurs, actions, bascule de thème) : tous centrent maintenant leur contenu de façon identique, ce qui supprime les décalages verticaux visibles entre les boutons.

### v2.0.1
- Correction du thème Poudlard : le titre et le nombre magique avaient une taille fixe qui ignorait l'optimisation mobile de la v2.0.0, provoquant un titre sur 3 lignes qui débordait sur iPhone. Les deux sont maintenant fluides comme le reste. Les bougies décoratives sont masquées sur petit écran pour épurer l'affichage.

### v2.0.0
- Optimisation des dimensions pour un affichage compatible iPhone (notamment dans un portail utilisant des iframes) : tailles de police et espacements désormais fluides (`clamp()`), réduction générale des marges/paddings (titre, plateau, bac à dés, boutons, bannière château), pour que l'ensemble du jeu tienne mieux sur un petit écran sans être coupé.

### v1.9.4
- Ajout d'une bannière "château magique" au-dessus du titre, en thème Poudlard uniquement (photo libre de droits, teintée pour s'harmoniser avec le parchemin, fondue en dégradé). Il s'agit d'un château fantastique générique, pas d'une reproduction du design officiel du château de la licence Harry Potter.

### v1.9.3
- Correction du bug d'affichage : la photo de parchemin était répétée en petites tuiles, créant de vilaines craquelures noires sur toute la page. Elle s'affiche maintenant en un seul grand fond (sans répétition).
- Le fond en vrai parchemin est désormais réservé au thème Poudlard (le thème classique retrouve son fond simple d'origine).
- Ajout d'un bord "parchemin déchiré" irrégulier sur le plateau et le bac à dés, et d'une police manuscrite (EB Garamond italique) pour le sous-titre, le libellé et le pied de page, pour un rendu plus proche d'un vieux grimoire.

### v1.9.2
- Remplacement de la texture de grain générée en SVG par une vraie photo de parchemin ancien (licence CC0, libre de droits), utilisée pour le fond du site ainsi que pour le bac à dés et les tuiles-nombres du thème Poudlard.

### v1.9.1
- Effet "vieux parchemin" du fond de page nettement renforcé : véritable grain de papier (généré en SVG), taches plus marquées et bords assombris, pour un rendu plus texturé qu'un simple dégradé.

### v1.9.0
- Fond de page transformé en vieux parchemin : taches, légère vignette sur les bords, texture de fibres de papier (sur les deux thèmes).
- Ajout d'un petit son de succès (carillon généré en direct via Web Audio API, aucun fichier audio à héberger) qui se joue à chaque bonne réponse.

### v1.8.0
- Thème Poudlard enrichi avec 3 améliorations : texture parchemin sur le bac et les tuiles (bords irréguliers, légère rotation), ambiance de fond façon Grande Salle (bougies flottantes scintillantes + ciel étoilé animé), et une célébration de victoire dédiée (sablier qui se remplit de rubis + étincelles dorées) remplaçant le simple message de bravo.

### v1.7.0
- Amélioration de la lisibilité des dés : dés et points agrandis, bordure contrastée autour de chaque dé, et en thème Poudlard un fond bordeaux foncé avec points dorés (au lieu de points clairs sur fond doré, peu lisibles).

### v1.6.0
- Ajout de décorations visuelles dans le thème Poudlard : chapeau de sorcier, vif d'or animé, baguette magique et balai (illustrations originales en SVG, sans logo officiel).

### v1.5.0
- Ajout d'un bouton **🪄 Thème Poudlard** permettant de basculer vers un habillage visuel inspiré de l'univers Gryffondor (couleurs rouge et or, typographie plus "magique", textes adaptés). Le thème classique reste disponible en un clic.

### v1.4.0
- Ajout d'un bouton ↩️ **Annuler** permettant de revenir sur la dernière opération effectuée.

### v1.3.0
- Nouveau mode de saisie façon calculette : on choisit d'abord un nombre, puis une opération (+ − ×), puis le second nombre, et le calcul se fait automatiquement (au lieu de sélectionner les deux nombres avant l'opération).

### v1.2.0
- Correction définitive : si aucun nombre ≥ 10 n'est atteignable avec les dés tirés, les dés sont relancés automatiquement jusqu'à obtenir un tirage valide (suppression de l'ancien secours qui pouvait produire un nombre trop faible, ex. 3 × 3 = 9).

### v1.1.0
- Le nombre à trouver ne peut plus être inférieur à 10, pour éviter des comptes trop simples.

### v1.0.0
- Version initiale : lancer de 5 dés, génération automatique du nombre à trouver, combinaison des nombres par +, − et ×, validation, indice/solution, score en étoiles.
