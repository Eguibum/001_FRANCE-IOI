# Le juste prix

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Ici, tu dois décider quel marchand a le meilleur prix en parcourant une boucle. A chaque fois que le prix est au plus bas, tu enregistres la position dans une valeur. A tarif égaux, tu gardes en mémoire la dernière position vue.
Les prix sont compris entre 1 et 1000000, donc tu vas initier ton prix minimum à 1000000. Ainsi tout prix inférieur ou égal à 1000000 sera pris en compte et remplacera la valeur courante de prix minimum.

```
Je récupère le nombre de marchands
J'initialise prixMinimum à 1000000
J'initialise positionPrixMin à -1 (valeur invalide)
J'initialise position à 1
Je répète autant de fois qu'il y a de marchand
  Je récupère prixGalette
  Si prixGalette est inférieur ou égal à prixMinimum
    prixMinimum = prixGalette
    positionPrixMin = position
    position = position + 1
J'affiche positionprixMin
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbMarchands = int(input())
minPrix = 1000 * 1000
posMinPrix = -1
pos = 1
for loop in range(nbMarchands):
   prix = int(input())
   if prix <= minPrix:
      minPrix = prix
      posMinPrix = pos
   pos = pos + 1
print(posMinPrix)
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
  <summary>Solution 1</summary>


```Java
import algorea.Scanner;
class Main
{
   public static void main(String[] args)
   {
      Scanner entrée = new Scanner(System.in);
      int nbMarchands = entrée.nextInt();
      
      int infini = 1000 * 1000;
      int minPrix = infini, posMinPrix = -1;
      int position = 1;
      for (int loop = 1; loop <= nbMarchands; loop = loop + 1)
      {
         int prix = entrée.nextInt();
         if (prix <= minPrix)
         {
            minPrix = prix;
            posMinPrix = position;
         }
         position = position + 1;
      }
      System.out.println(posMinPrix);
   }
}
```

</details>

<details>
  <summary>Solution 2</summary>


```Java
import algorea.Scanner;
class Main
{
   public static void main(String[] args)
   {
      Scanner entrée = new Scanner(System.in);
      int nbMarchands = entrée.nextInt();
      
      int infini = 1000 * 1000;
      int minPrix = infini, posMinPrix = -1;
      for (int pos = 1; pos <= nbMarchands; pos = pos + 1)
      {
         int prix = entrée.nextInt();
         if (prix <= minPrix)
         {
            minPrix = prix;
            posMinPrix = pos;
         }
      }
      System.out.println(posMinPrix);
   }
}
```

</details>
