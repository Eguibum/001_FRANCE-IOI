# Encore des punitions

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Encore une punition ! Décidémment, ils ne sont pas très sages ces élèves ! Pour les aider, tu dois donc programmer ton robot à répéter une phrase un nombre de fois inconnu, qui te sera fourni par une entrée.

```
Je récupère le nombre de répétition dans une variable
Je répète "variable" fois
  j'affiche Je dois suivre en cours
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbLignes = int(input())
for iLigne in range(nbLignes):
   print("Je dois suivre en cours")
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
      int nbLignes = entrée.nextInt();
      for (int iLigne = 1; iLigne <= nbLignes; iLigne = iLigne + 1) {
         System.out.println("Je dois suivre en cours");
      }
   }
}
```

</details>
