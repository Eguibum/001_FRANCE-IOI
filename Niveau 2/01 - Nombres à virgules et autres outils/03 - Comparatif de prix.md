# Comparatif de prix

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Une fois lu le nombre de légumes, on peut lire dans une boucle les informations concernant chaque légume, à savoir : un poids, un nombre de jours et un prix. Le nombre de jours est une information inutile pour calculer le prix au kilo. Mais, même si l'on n'utilise pas cette information, on est tout de même obligé de la lire. 

```
nombreLegumes <- LireEntier()
Répéter nombreLegumes fois
   poids <- LireDecimal()
   age <- LireDecimal()
   prix <- LireDecimal()
   Afficher (prix / poids)
```

## Python

<details>
  <summary>Solution</summary>

```Python
nombreLegumes = int(input())
for loop in range(nombreLegumes):
   poids = float(input())
   age = float(input())
   prix = float(input())
   print(prix / poids)
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
      int nombreLégumes = entrée.nextInt();
    
      for (int loop = 1; loop <= nombreLégumes; loop = loop + 1)
      {
         double poids = entrée.nextDouble();
         // âge
         entrée.nextDouble();
         double prix = entrée.nextDouble();
    
         System.out.println(prix / poids);
      }
   }
}
```

</details>
