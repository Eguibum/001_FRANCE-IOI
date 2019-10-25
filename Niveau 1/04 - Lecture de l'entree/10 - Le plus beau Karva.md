# Le plus beau Karva

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Le but ici est de faire une boucle te permettant de récupérer pour chaque Karva ses caractéristiques, de calculer son total de points et de l'afficher. Une des caractérisques, l'age, n'est pas pris en compte dans le calcul de points. Son stockage dans une variable n'est donc pas obligatoire (ça préserve de la mémoire).

```
Je récupère le nombre de karvas participants
Je répète autant de fois qu'il y a de karvas
  je récupère son poids
  je récupère son age (sans la stocker obligatoirement)
  je récupère sa longueur de cornes
  je récupère sa hauteur au garot
  j'affiche le résultat de sa longueur de cornes * sa hauteur au garot + son poids
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbKarvas = int(input())
for loop in range(nbKarvas):
   poids = int(input())
   âge = int(input())
   longueurCornes = int(input())
   hauteurAuGarrot = int(input())
   print(longueurCornes * hauteurAuGarrot + poids)
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
      int nbKarvas = entrée.nextInt();
      for (int loop = 1; loop <= nbKarvas; loop = loop + 1) {
         int poids = entrée.nextInt();
         entrée.nextInt(); // âge
         int longueurCornes = entrée.nextInt();
         int hauteurAuGarrot = entrée.nextInt();
         System.out.println(longueurCornes * hauteurAuGarrot + poids);
      }
   }
}
```

</details>
