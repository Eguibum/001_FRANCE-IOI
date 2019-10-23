# Dans les fourrés

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

Comme dans un vieux jeu Pokemon sur Gameboy 2D, il faut se déplacer de case en case sans tomber dans les pièges ou les fourrés :)

Attention, pour cet exercice, pense bien à importer le module Robot !!!

```
haut
haut
haut
droite
droite
bas
bas
droite
```

## Python

<details>
  <summary>Solution</summary>

```Python
from robot import *
haut()
haut()
haut()
droite()
droite()
bas()
bas()
droite()
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
Et avec le module et les instructions :)
</br>
</br>

<details>
  <summary>Solution</summary>


```Java
import static algorea.Robot.*;
class Main {
   public static void main(String[] args) {
      haut();
      haut();
      haut();
      droite();
      droite();
      bas();
      bas();
      droite();
   }
}
```

</details>
