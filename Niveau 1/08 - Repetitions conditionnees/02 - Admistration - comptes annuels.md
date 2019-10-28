# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Comme on ne sait pas à l'avance combien de dépenses ont été effectuées, il faut utiliser une boucle « tant que ». On sait qu'il y aura au moins un entier à lire (le marqueur de fin est toujours là), donc on commence par lire un premier entier ; puis s'il est différent de -1, alors on l'ajoute à la somme et on peut lire un nouvel entier. Si celui-ci est différent de -1, on peut l'ajouter à la somme… et ainsi de suite. 

```
sommeDépenses <- 0
dépense <- lireEntier()
Tant que dépense != -1
   sommeDépenses <- sommeDépenses + dépense
   dépense <- lireEntier()
Afficher sommeDépenses
```

## Python

<details>
  <summary>Solution</summary>

```Python
sommeDépenses = 0
dépense = int(input())
while dépense != -1:
   sommeDépenses = sommeDépenses + dépense
   dépense = int(input())
print(sommeDépenses)
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
      int dépense = entrée.nextInt();
      int sommeDépenses = 0;
      while (dépense != -1)
      {
         sommeDépenses = sommeDépenses + dépense;
         dépense = entrée.nextInt();
      }
      System.out.println(sommeDépenses);
   }
}
```

</details>
