# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 Si chaque malade contamine deux nouvelles personnes le jour suivant, alors s'il y a 100 malades, il y a 200 nouveaux contaminés le jour suivant, donc 300 malades au total. Ainsi, chaque jour on multiplie par 3 le nombre de malades !

On va donc calculer le nombre de malades aux jours 1, 2… et s'arrêter quand ce nombre dépasse le nombre d'habitants de la ville. Dit autrement, tant que le nombre de malades est strictement inférieur au nombre d'habitants, on ajoute 1 au nombre de jours et on multiplie par 3 le nombre de malades. 

```
populationVille <- lireEntier()
numJour <- 1
nbMalades <- 1
Tant que nbMalades < populationVille
   numJour <- numJour + 1
   nbMalades <- nbMalades * 3
Afficher numJour
```

## Python

<details>
  <summary>Solution</summary>

```Python
populationVille = int(input())
numJour = 1
nbMalades = 1
while nbMalades < populationVille:
   numJour = numJour + 1
   nbMalades = nbMalades * 3
print(numJour)
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
class Main {
   static Scanner entrée = new Scanner(System.in);
   public static void main(String[] args) {
      int populationVille = entrée.nextInt();
      int numJour = 1;
      int nbMalades = 1;
      while (nbMalades < populationVille) {
         numJour = numJour + 1;
         nbMalades = nbMalades * 3;
      }
      System.out.println(numJour);
   }
}
```

</details>
