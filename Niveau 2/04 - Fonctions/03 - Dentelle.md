# Dentelle

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On écrit une fonction ligneDentelle qui prend deux paramètres : la longueur de la ligne et le motif de la dentelle, dans laquelle on affiche le motif avec une boucle. On appelle la fonction trois fois avec les trois motifs dans le programme. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
def ligneDentelle(longueur, motif):
   for iCol in range(longueur):
      print(motif, end = "");
   print()
longueur = int(input())
ligneDentelle(longueur, "X");
ligneDentelle(longueur, "#");
ligneDentelle(longueur, "i");
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
   static void ligneDentelle(int longueur, char motif) {
      for (int iCol = 1; iCol <= longueur; iCol++) {
         System.out.print(motif);
      }
      System.out.println();
   }
   public static void main(String[] args) {
      int longueur = entrée.nextInt();
      ligneDentelle(longueur, 'X');
      ligneDentelle(longueur, '#');
      ligneDentelle(longueur, 'i');
   }
}
```

</details>
