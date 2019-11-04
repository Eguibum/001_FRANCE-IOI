# Phénomène numérique

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Tant qu'on atteint pas le nombre 1, on calcule le terme suivant avec une fonction ; ce qui donne le programme ci-dessous. 

```
Fonction termeSuivant(terme)
   Si terme mod 2 = 0
      Retourner terme / 2
   Sinon
      Retourner 3 * terme + 1
terme <- lireEntier()
Tant que terme != 1
   terme <- termeSuivant(terme)
   Afficher terme, " " (sans retour à la ligne ni séparateur)
Aller à la ligne
```

## Python

<details>
  <summary>Solution</summary>

```Python
def termeSuivant(terme):
   if terme % 2 == 0:
      return terme // 2
   else:
      return terme * 3 + 1
terme = int(input())
while terme != 1:
   terme = termeSuivant(terme)
   print(terme, end = " ")
print()
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
   static int termeSuivant(int terme) {
      if (terme % 2 == 0) {
         return terme / 2;
      } else {
         return terme * 3 + 1;
      }
   }
   public static void main(String[] args) {
      int terme = entrée.nextInt();
      while (terme != 1) {
         terme = termeSuivant(terme);
         System.out.print(terme + " ");
      }
      System.out.println();
   }
}
```

</details>
