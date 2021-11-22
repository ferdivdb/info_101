# Exercices Théoriques Python

[![N|Solid](https://fundit.fr/sites/default/files/actors/1456-universite-libre-bruxelles-ulb.jpg)](https://nodesource.com/products/nsolid)

## Les classes

### La Méthode \__init\__
#### L'opération d'instanciation (en "appelant" un objet classe) crée un objet vide. De nombreuses classes aiment créer des instances personnalisées correspondant à un état initial spécifique. À cet effet, une classe peut définir une méthode spéciale nommée __init__(), comme ceci :
> def _\_init__(self):
>   self.data = []

### La Méthode \__str\__
####     Appelée par str(objet) ainsi que les fonctions natives format() et print() pour calculer une chaîne de caractères « informelle » ou joliment mise en forme de représentation de l'objet. La valeur renvoyée doit être un objet string.
Cette méthode diffère de object.\__repr\__() car il n'est pas attendu que \__str\__() renvoie une expression Python valide : une représentation plus agréable à lire ou plus concise peut être utilisée.
C'est l'implémentation par défaut des appels à object.\__repr\__() du type natif object.

### p == q
#### Ce sont les méthodes dites de « comparaisons riches ». La correspondance entre les symboles opérateurs et les noms de méthodes est la suivante : x<y appelle x.__lt__(y), x<=y appelle x.\__le\__(y), x==y appelle x.\__eq\__(y), x!=y appelle x.\__ne\__(y), x>y appelle x.\__gt\__(y) et x>=y appelle x.\__ge\__(y).

Une méthode de comparaison riche peut renvoyer le singleton NotImplemented si elle n'implémente pas l'opération pour une paire donnée d'arguments. Par convention, False et True sont renvoyées pour une comparaison qui a réussi. Cependant, ces méthodes peuvent renvoyer n'importe quelle valeur donc, si l'opérateur de comparaison est utilisé dans un contexte booléen (par exemple dans une condition d'une instruction if), Python appelle bool() sur la valeur pour déterminer si le résultat est faux ou vrai.

Par défaut, object implémente \__eq\__() en utilisant is et renvoie NotImplemented si la comparaison renvoie False : True if x is y else NotImplemented. Pour \__ne\__(), il délègue à \__eq\__() et renvoie le résultat inverse, sauf si c'est NotImplemented. Il n'y a pas d'autres relations implicites pour les opérateurs de comparaison ou d'implémentations par défaut ; par exemple, (x<<y or x==y) n'implique pas x<=y. Pour obtenir une relation d'ordre total automatique à partir d'une seule opération, reportez-vous à functools.total_ordering().

Lisez le paragraphe \__hash\__() pour connaître certaines notions importantes relatives à la création d'objets hashable qui acceptent les opérations de comparaison personnalisées et qui sont utilisables en tant que clés de dictionnaires.

Il n'y a pas de versions avec les arguments interchangés de ces méthodes (qui seraient utilisées quand l'argument de gauche ne connaît pas l'opération alors que l'argument de droite la connaît) ; en lieu et place, \__lt\__() et \__gt\__() sont la réflexion l'une de l'autre, \__le\__() et \__ge\__() sont la réflexion l'une de l'autre et \__eq\__() ainsi que \__ne\__() sont réflexives. Si les opérandes sont de types différents et que l'opérande de droite est d'un type qui une sous-classe directe ou indirecte du type de l'opérande de gauche, alors la méthode symétrique de l'opérande de droite est prioritaire, sinon c'est la méthode de l'opérande de gauche qui est prioritaire. Les sous-classes virtuelles ne sont pas prises en compte.

### Sursarge d'oérateur \__add\__ (\__radd\__)



### Polymorphisme

### Programation orienté-objet

 <!-- ajouter illustration diagramme d'objet  -->
