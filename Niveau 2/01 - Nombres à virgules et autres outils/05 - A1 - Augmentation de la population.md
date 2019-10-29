# Augmentation de la population

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 À partir du pourcentage d'augmentation croissancePourcent, on calcule la nouvelle population en multipliant par (1 + croissancePourcent / 100) l'ancienne population. En effet, sur un exemple avec une augmentation de 15 % (c'est-à-dire que croissancePourcent est égal à 15), on a :

nouvellePopulation=populationActuelle+populationActuelle×(15100)

nouvellePopulation=populationActuelle×(1+15100)

nouvellePopulation=populationActuelle×(1+croissancePourcent100)

Une fois qu'on a calculé cette valeur décimale, il suffit d'arrondir à l'entier inférieur pour respecter la convention qui était donnée dans l'énoncé. 

```
populationActuelle <- LireEntier()
croissancePourcent <- LireDecimal()
populationFuture <- ArrondiInferieur( populationActuelle * (1 + croissancePourcent / 100) )
Afficher populationFuture
```

## Python

<details>
  <summary>Solution</summary>

```Python
from math import *
populationActuelle = int(input())
croissancePourcent = float(input())
populationFuture = floor( populationActuelle * (1 + croissancePourcent / 100) )
print(populationFuture)
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
      Scanner entrée = new Scanner(System.in);
      int populationActuelle = entrée.nextInt();
      double croissancePourcent = entrée.nextDouble();
      int populationFuture =
         (int)floor( populationActuelle * (1 + croissancePourcent / 100) );
      System.out.println(populationFuture);
   }
}
```

</details>
