# Empilement de cylindres

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

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
