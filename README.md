# Exercices Théoriques Python

## Les classes

### La Méthode __init__
#### L'opération d'instanciation (en "appelant" un objet classe) crée un objet vide. De nombreuses classes aiment créer des instances personnalisées correspondant à un état initial spécifique. À cet effet, une classe peut définir une méthode spéciale nommée __init__(), comme ceci :
> def __init__(self):
>   self.data = []

### La Méthode __str__
####     Appelée par str(objet) ainsi que les fonctions natives format() et print() pour calculer une chaîne de caractères « informelle » ou joliment mise en forme de représentation de l'objet. La valeur renvoyée doit être un objet string.
Cette méthode diffère de object.__repr__() car il n'est pas attendu que __str__() renvoie une expression Python valide : une représentation plus agréable à lire ou plus concise peut être utilisée.

C'est l'implémentation par défaut des appels à object.__repr__() du type natif object.
 
