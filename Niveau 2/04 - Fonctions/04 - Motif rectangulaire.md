# Motif rectangulaire

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Nous faisons une fonction pour dessiner le rectangle : cette fonction prend trois paramètres, le nombre de lignes et de colonnes ainsi que le caractère à afficher, et elle dessine le rectangle dans deux boucles imbriquées comme nous avons déjà pu le faire précédemment. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
def dessinerRectangle(nbLignes, nbColonnes, motif):
   for iLigne in range(nbLignes):
      for iCol in range(nbColonnes):
         print(motif, end = "")
      print()
nbLignes = int(input())
nbColonnes = int(input())
motif = input()
dessinerRectangle(nbLignes, nbColonnes, motif)
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
   static void dessinerRectangle(int nbLignes, int nbColonnes, char motif) {
      for (int iLigne = 0; iLigne < nbLignes; iLigne = iLigne + 1) {
         for (int iCol = 0; iCol < nbColonnes; iCol = iCol + 1) {
            System.out.print(motif);
         }
         System.out.println();
      }
   }
   public static void main(String[] args) {
      int nbLignes = entrée.nextInt();
      int nbColonnes = entrée.nextInt();
      char motif = entrée.next().charAt(0);
      dessinerRectangle(nbLignes, nbColonnes, motif);
   }
}
```

</details>
