# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Ici la difficulté est de répartir le bon joueur dans la bonne équipe. A l'aide de boucles et de conditions, on peut résoudre cet exercice.

```
Je récupère le nombre de joueurs par équipe
J'initialise mon total poids équipe 1 à 0
J'initialise mon total poids équipe 2 à 0
Je répète autant de fois qu'il y a de joueurs par équipe
  Je récupère le poids du joueur équipe 1
  Je récupère le poids du joueur équipe 2
  Je mets à jours le poids total de l'équipe 1 en rajoute le poids du joueur
  Je mets à jours le poids total de l'équipe 2 en rajoute le poids du joueur
Si le poids total de l'équipe 1 est supérieur au poids total de l'équipe 2
  J'affiche L'équipe 1 a un avantage
Sinon
  J'affiche l'équipe 2 a un avantage
J'affiche le poids total de l'équipe 1
J'affiche le poids total de l'équipe 2
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbPersonnes = int(input())
totalÉquipe1 = 0
totalÉquipe2 = 0
for loop in range(nbPersonnes):
   poids1 = int(input())
   poids2 = int(input())
   totalÉquipe1 = totalÉquipe1 + poids1
   totalÉquipe2 = totalÉquipe2 + poids2
if totalÉquipe1 > totalÉquipe2:
   print("L'équipe 1 a un avantage")
else:
   print("L'équipe 2 a un avantage")
print("Poids total pour l'équipe 1 :", totalÉquipe1)
print("Poids total pour l'équipe 2 :", totalÉquipe2)
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
      int nbPersonnes = entrée.nextInt();
      int totalÉquipe1 = 0, totalÉquipe2 = 0;
      for (int loop = 1; loop <= nbPersonnes; loop = loop + 1) {
         int poids1 = entrée.nextInt();
         int poids2 = entrée.nextInt();
         totalÉquipe1 = totalÉquipe1 + poids1;
         totalÉquipe2 = totalÉquipe2 + poids2;
      }
      if (totalÉquipe1 > totalÉquipe2) {
         System.out.println("L'équipe 1 a un avantage");
      }
      else {
         System.out.println("L'équipe 2 a un avantage");
      }
      System.out.println("Poids total pour l'équipe 1 : " + totalÉquipe1);
      System.out.println("Poids total pour l'équipe 2 : " + totalÉquipe2);
   }
}
```

</details>
