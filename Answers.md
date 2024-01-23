# Answers
## Partie 2 - Grid
### 🔧 Exercice 1
Pour comprendre l'utilité de `LazyVGrid`, on peut essayer de séparer les différentes termes du nom de cet élément :
- `Lazy` siginifie paresseux et fait référence au chargement des données à retardement (les données sont chargées pendant que l'application est utilisée)
- `V` est pour le caractère vertical
- `Grid` signifie "grille"
Donc `LazyVGrid` signigie une grille verticale permettant de charger des données pendant qu'elle est utilisée.
C'est le cas ici où l'on charge des photos depuis Unsplash. C'est pour cette raison que l'on l'utilise plutôt que `Grid`.

Les différents types de `column` sont :
- `Fixed` qui ne s'adaptent pas et peuvent sortir de l'écran
- `Flexible` qui respectent au maximum les instructions, mais si elles n'ont pas assez de place vont créer une nouvelle colonne.
- `Adaptive` qui ne respectent pas les instructions et vont d'adapter à place disponible pour placer les colonnes.

Les images prennent toute la place de l'écran, car on ne leur a renseigné aucune largeur. Par défaut, le ratio de l'image n'est pas respecté et donc la largeur de l'image reste la même dans la vue.

### Exercice 2

- `.resizable()` permet à l'image d'être redimensionnée.
- `.scaledToFill()` indique que l'image doit être mise à l'échelle pour remplir entièrement le cadre tout en conservant son ratio.
- `.frame(width: geo.size.width, height: geo.size.height)` définit la taille du cadre de l'image en fonction de la largeur et de la hauteur de l'espace disponible fourni par le GeometryReader
- `.clipped()` cela indique que l'image doit être rognée pour s'adapter au cadre défini précédemment.
