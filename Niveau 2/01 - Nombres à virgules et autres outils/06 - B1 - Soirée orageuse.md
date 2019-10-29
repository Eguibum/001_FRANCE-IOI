# Soirée orageuse

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Comme on connait la vitesse du son et le temps que celui-ci a mis pour parcourir la distance il est facile de calculer la distance (en mètres) en faisant
`distanceMetres <- tempsParcours * vitesseSon`

on a donc
`distanceKilometres <-  (tempsParcours * vitesseSon) / 1000`

et donc avec l'arrondi
`distanceKilometres <- ArrondiPlusProche((tempsParcours * vitesseSon) / 1000)`

```
vitesseSon <- 340.29
tempsParcours <- LireDecimal()
distanceKilometres <- ArrondiPlusProche((tempsParcours * vitesseSon) / 1000)
Afficher distanceKilometres
```

## Python

<details>
  <summary>Solution</summary>

```Python
from math import *
vitesseSon = 340.29
tempsParcours = float(input())
distanceKilometres = round((tempsParcours * vitesseSon) / 1000)
print(distanceKilometres)
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
import algorea.Scanner;
import static java.lang.Math.*;
class Main
{
   public static void main(String[] args)
   {
      double vitesseSon = 340.29;
      Scanner entrée = new Scanner(System.in);     
      double tempsParcours = entrée.nextDouble();
      int distanceKilometres = (int)(round((tempsParcours * vitesseSon) / 1000));
      System.out.println(distanceKilometres);
   }
}
```

</details>
