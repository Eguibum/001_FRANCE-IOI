# Etape la plus longue

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Le but ici est de parcourir un nombre de distances et de garder en mémoire la plus élevée, car la distance la plus longue n'est pas forcément la dernière distance lue.

```
Je récupère le nombre de jours
J'initialise distanceMax à 0
Je répète autant de fois qu'il y a de jours
  J'initialise distanceParcourue avec l'input du programme
  Si distanceParcourue est supérieure à distanceMax
    DistanceMax prend la valeur de distanceParcourue
J'affiche distanceParcourue
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbJours = int(input())
distanceMax = 0
for loop in range(nbJours):
   distance = int(input())
   if distance > distanceMax:
      distanceMax = distance
print(distanceMax)
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
class Main
{
   public static void main(String[] args)
   {
      Scanner entrée = new Scanner(System.in);
      int nbJours = entrée.nextInt();
      int distanceMax = 0;
      for (int loop = 1; loop <= nbJours; loop = loop + 1)
      {
         int distance = entrée.nextInt();
         if(distance > distanceMax)
         {
            distanceMax = distance;
         }
      }
      System.out.println(distanceMax);
   }
}
```

</details>
