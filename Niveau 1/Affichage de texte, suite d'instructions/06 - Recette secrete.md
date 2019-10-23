# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

A partir d'un seau de 5L et d'un seau de 3L, il te faut obtenir 4L. Pour cela, des petits dessins s'imposent, en prenant en compte le fait de remplir, transférer et vider.

Ce dessus, je vais lister les étapes et à la fin, indiquer la contenance des seaux (x,y). x correspond au seau de 5L et y au seau de 3L.

```
Je remplis le seau de 5L (5,0)
Je transfere le seau de 5L dans le seau de 3L (2,3)
Je vide le seau de 3L (2,0)
Je transfere le seau de 5l dans le seau de 3L (0,2)
Je remplis le seau de 5L (5,2)
Je transfere le seau de 5L dans le seau de 3L (4,3)
```

## Python

<details>
  <summary>Solution</summary>

```Python
from robot import *
remplir(5)
transferer(5, 3)
vider(3)
transferer(5, 3)
remplir(5)
transferer(5, 3)
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
      remplir(5);
      transferer(5, 3);
      vider(3);
      transferer(5, 3);
      remplir(5);
      transferer(5, 3);
   }
}
```

</details>
