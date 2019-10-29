# Préparation de l'onguent

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On utilise un tableau dans lequel on va stocker les quantités nécessaires pour chaque ingrédient. Il suffit alors de lire le numéro de l'ingrédient demandé et d'afficher la valeur du tableau correspondante. 

```
quantite <- [500, 180, 650, 25, 666, 42, 421, 1, 370, 211]
ingredient <- LireEntier()
Afficher quantite[ingredient]
```

## Python

<details>
  <summary>Solution</summary>

```Python
quantite = [500, 180, 650, 25, 666, 42, 421, 1, 370, 211]
ingredient = int(input())
print(quantite[ingredient])
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
      int[] quantite = {500, 180, 650, 25, 666, 42, 421, 1, 370, 211};
      int ingredient = entrée.nextInt();
      System.out.println(quantite[ingredient]);
   }
}
```

</details>
