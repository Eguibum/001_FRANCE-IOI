# Empilement de cylindres

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

Le but est de déplacer toute la tour de gauche à droite pour monter, sans qu'un plateau ne soit sur un plateau plus petit que lui-même

Je n'affiche pas de pseudo-code pour cet exercice car il est très long, mais je te conseille grandement de t'aider d'une feuille de papier pour illustrer chaque ligne d'instruction.

Sinon, renseignee-toi sur les tours d'Hanoï ;)

## Python

<details>
  <summary>Solution</summary>

```Python
from robot import *
deplacer(1, 2)
deplacer(1, 3)
deplacer(2, 3)
deplacer(1, 2)
deplacer(3, 1)
deplacer(3, 2)
deplacer(1, 2)
deplacer(1, 3)
deplacer(2, 3)
deplacer(2, 1)
deplacer(3, 1)
deplacer(2, 3)
deplacer(1, 2)
deplacer(1, 3)
deplacer(2, 3)
```

</details>

## Java

Code minimal Java

<details>
  <summary>Solution</summary>

```Java
  class Main {
    public static void main(String[] args) {
      // ton code ici
    }
  }
```

</details>

</br>
Et avec le robot et les instructions :)
</br>
</br>

<details>
  <summary>Solution</summary>


```Java
import static algorea.Robot.*;
class Main {
   public static void main(String[] args) {
      deplacer(1,2);
      deplacer(1,3);
      deplacer(2,3);
      
      deplacer(1,2);
      
      deplacer(3,1);
      deplacer(3,2);
      deplacer(1,2);
      
      
      deplacer(1,3);
      
      
      deplacer(2,3);
      deplacer(2,1);
      deplacer(3,1);
      
      deplacer(2,3);
      
      deplacer(1,2);
      deplacer(1,3);
      deplacer(2,3);
   }
}
```

</details>
