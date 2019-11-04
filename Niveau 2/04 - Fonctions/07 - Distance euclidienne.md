# Distance euclidienne

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On crée une fonction à quatre paramètres qui s'en sert pour appliquer la formule et retourner le résultat.

Notez que la racine carrée peut aussi être calculée comme une puissance, car x−−√n=x1n
donc x−−√=x12. 

```
Fonction distance(x1, y1, x2, y2)
   Retourner racineCarrée((x2 - x1) ^ 2 + (y2 - y1) ^ 2)

x1 <- lireFlottant()
y1 <- lireFlottant()
x2 <- lireFlottant()
y2 <- lireFlottant()
Afficher distance(x1, y1, x2, y2)
```

## Python

<details>
  <summary>Solution</summary>

```Python
from math import *
def distance(x1, y1, x2, y2):
   return sqrt((x2 - x1) ** 2 + (y2 - y1) ** 2)
x1 = float(input())
y1 = float(input())
x2 = float(input())
y2 = float(input())
print(distance(x1, y1, x2, y2))
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
class Main {
   static Scanner entrée = new Scanner(System.in);
   static double distance(double x1, double y1, double x2, double y2) {
      return sqrt(pow(x1 - x2, 2) + pow(y1 - y2, 2));
   }
   public static void main(String[] args) {
      double x1 = entrée.nextDouble();
      double y1 = entrée.nextDouble();
      double x2 = entrée.nextDouble();
      double y2 = entrée.nextDouble();
      System.out.println(distance(x1, y1, x2, y2));
   }
}
```

</details>
