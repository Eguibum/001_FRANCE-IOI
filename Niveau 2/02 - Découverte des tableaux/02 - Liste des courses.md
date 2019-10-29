# Liste des courses

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On utilise un tableau dans lequel on va stocker les prix au kilo de chaque ingrédient. Ensuite, à l'aide d'une boucle, on va lire les quantité demandées pour chaque ingrédient, calcul le prix à payer pour cette quantité et ajouter cette valeur à une variable prixTotal. Il suffira alors d'afficher le contenu de cette variable. 

```
prix <- [9, 5, 12, 15, 7, 42, 13, 10, 1, 20]
prixTotal <- 0
Pour idIngredient allant de 0 à 9
   quantite <- LireEntier()
   prixTotal <- prixTotal + prix[idIngredient] * quantite
Afficher prixTotal
```

## Python

<details>
  <summary>Solution</summary>

```Python
prix = [9, 5, 12, 15, 7, 42, 13, 10, 1, 20]
prixTotal = 0
for idIngredient in range(10):
   quantite = int(input())
   prixTotal = prixTotal + prix[idIngredient] * quantite
print(prixTotal)
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
      int[] prix = {9, 5, 12, 15, 7, 42, 13, 10, 1, 20};
      int prixTotal = 0;
      for (int idIngredient = 0; idIngredient < 10; idIngredient = idIngredient + 1)
      {
         int quantite = entrée.nextInt();
         prixTotal = prixTotal + prix[idIngredient] * quantite;
      }
      System.out.println(prixTotal);
   }
}
```

</details>
