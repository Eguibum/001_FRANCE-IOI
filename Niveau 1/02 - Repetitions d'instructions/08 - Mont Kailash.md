# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

En lisant bien les instructions, on réalise que c'est encore juste une histoire de boucles imbriquées. D'abord, il faut définir les boucles pour faire 1 seul tour, puis imbriqué cette ensemble de conditions dans une boucle pour faire le nombre de tour demander.

Pour faire un tour, il faut donc se déplacer 13 fois vers le haut, 13 fois vers la droite, 13 fois vers le bas et 13 fois vers la gauche. Et ce "cercle", il faut le répéter 108 fois. On définit donc la première boucle à 108, puis on enchaîne à l'intérieur les 4 boucles de 13.

Et n'oublie pas ton robot !

```
Je répète 108 fois
  Je répète 13 Fois
    Aller en haut
  Je répète 13 Fois
    Aller à droite
  Je répète 13 Fois
    Aller en bas
  Je répète 13 Fois
    Aller à gauche
```

## Python

<details>
  <summary>Solution</summary>

```Python
from robot import *
for loop in range(108):
   for loop in range(13):
      haut()
   for loop in range(13):
      droite()
   for loop in range(13):
      bas()
   for loop in range(13):
      gauche()
```

</details>

## Java

Code minimal Java

<details>
  <summary>Minimum fonctionnel</summary>

```Java
  class Main {
    public static void main(String[] args) {
      // ton code ici
    }
  }
```

</details>

</br>
Et avec les instructions :)
</br>
</br>

<details>
  <summary>Solution</summary>


```Java
import static algorea.Robot.*;
class Main {
   public static void main(String[] args) {
      for (int loop = 1; loop <= 108; loop = loop + 1) {
         for (int loop2 = 1; loop2 <= 13; loop2 = loop2 + 1) {
            haut();
         }
         for (int loop2 = 1; loop2 <= 13; loop2 = loop2 + 1) {
            droite();
         }
         for (int loop2 = 1; loop2 <= 13; loop2 = loop2 + 1) {
            bas();
         }
         for (int loop2 = 1; loop2 <= 13; loop2 = loop2 + 1) {
            gauche();
         }
      }
   }
}
```

</details>
