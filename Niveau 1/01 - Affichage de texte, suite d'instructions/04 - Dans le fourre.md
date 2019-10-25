# Dans les fourrés

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

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
