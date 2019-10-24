# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

Encore des boucles ! Bah oui, c'est le chapitre des répétitions.
Encore une fois, il faut détailler ce que le robot doit faire, et le répéter le nombre de fois nécessaire.

Il doit donc ramasser, se déplacer 15 fois vers la droite, déposer, se déplacer 15 fois vers la gauche. Et il doit répéter cette suite d'instruction 20 fois. On y va ?

```
Je répète 20 fois
  Je ramasse
  Je répète 15 fois
    Aller à droite
  Je dépose
  Je répète 15 fois
    Aller à gauche
```

## Python

<details>
  <summary>Solution</summary>

```Python
from robot import *
for loop in range(20):
   ramasser()
   for loop in range(15):
      droite()
   deposer()
   for loop in range(15):
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
      for (int loop = 1; loop <= 20; loop = loop + 1) {
         ramasser();
         for (int loop2 = 1; loop2 <= 15; loop2 = loop2 + 1) {
            droite();
         }
         deposer();
         for (int loop2 = 1; loop2 <= 15; loop2 = loop2 + 1) {
            gauche();
         }
      }
   }
}
```

</details>
