# Le plus petit de deux entiers

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On lit le premier des nombres de l'utilisateur, pour le stocker dans une variable qui va contenir la plus petite valeur rencontrée jusqu'à présent. À chaque nouvelle valeur, on conserve la plus petite parmi la valeur stockée et la valeur lue, en appelant la fonction min2. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
def min2(val1, val2):
   if val1 < val2:
      return val1
   else:
      return val2
valMin = int(input())
for iVal in range(9):
   valMin = min2(valMin, int(input()))
print(valMin)
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
   static int min2(int a, int b)
   {
      if (a < b)
         return a;
      else
         return b;
   }
   public static void main(String[] args) {
      int valMin = entrée.nextInt();
      for (int iVal = 1; iVal < 10; iVal = iVal + 1) {
         valMin = min2(valMin, entrée.nextInt());
      }
      System.out.println(valMin);
   }
}
```

</details>
