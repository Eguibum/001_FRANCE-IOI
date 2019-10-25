# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Ici, il s'agit d'additionner à chaque boucle le nombre de karva avec le total, défini à 0. Et il faut répéter la boucle autant de fois qu'il y a de fermiers.

```
J'initialise mon total de karvas à 0
Je répète autant de fois qu'il y a de fermiers
  je récupère le nombre de karvas
  Je l'ajoute au total
j'affiche le total de karvas
```

## Python

<details>
  <summary>Solution</summary>

```Python
totalKarvas = 0
for loop in range(20):
   nbBêtes = int(input())
   totalKarvas = totalKarvas + nbBêtes
print(totalKarvas)
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
      int totalKarvas = 0;
      for (int loop = 1; loop <= 20; loop = loop + 1) {
         int nbBêtes = entrée.nextInt();
         totalKarvas = totalKarvas + nbBêtes;
      }
      System.out.println(totalKarvas);
   }
}
```

</details>
