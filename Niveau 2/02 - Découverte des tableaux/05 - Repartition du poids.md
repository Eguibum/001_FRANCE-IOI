# Répartition du poids

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 On souhaite que toutes les charrettes aient le même poids qui correspond à une répartition équitable. On commence donc par calculer le poids total puis on divise par le nombre de charrettes pour obtenir le poids moyen que chaque charrette devrait avoir. Pendant qu'on calcul ce poids total, on fait bien sûr attention à stocker dans un tableau de poids de chaque charrette car on en a besoin pour la suite.

Une fois qu'on connait le poids moyen, c'est-à-dire le poids que devrait avoir chaque charrette, il faut calculer le poids à ajouter ou enlever. On sait que si la charrettes n'est pas assez chargée il va falloir lui ajouter du poids et donc on devra afficher un nombre positif qui sera donc égal au poids moyen moins le poids de la charrette. 

```
nbCharrettes <- LireEntier()
poids <- Tableau de taille nbCharrettes contenant des 0.0
poidsTotal <- 0.0
Pour numero allant de 0 à nbCharrettes-1
   poids[numero] <- LireDecimal()
   poidsTotal <- poidsTotal + poids[numero]
poidsMoyen <- poidsTotal / nbCharrettes
Pour numero allant de 0 à nbCharrettes-1
   Afficher (poidsMoyen - poids[numero])
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbCharrettes = int(input())
poids = [0.0] * nbCharrettes
poidsTotal = 0.0
for numero in range(nbCharrettes):
   poids[numero] = float(input())
   poidsTotal = poidsTotal + poids[numero]
poidsMoyen = poidsTotal / nbCharrettes
for numero in range(nbCharrettes):
   print(poidsMoyen - poids[numero])
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
      int nbCharrettes = entrée.nextInt();
      double[] poids = new double[nbCharrettes];
       
      double poidsTotal = 0.0;
      for (int numero = 0; numero < nbCharrettes; numero = numero + 1)
      {
         poids[numero] = entrée.nextDouble();
         poidsTotal = poidsTotal + poids[numero];
      }
       
      double poidsMoyen = poidsTotal / nbCharrettes;
       
      for (int numero = 0; numero < nbCharrettes; numero = numero + 1)
      {
         System.out.println(poidsMoyen - poids[numero]);
      }
   }
}
```

</details>
