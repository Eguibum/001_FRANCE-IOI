# Nombre de personnes à la fête

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Il faut un peu se creuser la tête pour celui-là aussi. Tu récupères le nombre de personnes qu'il y a eu à la fête, et à partir de ça à chaque boucle, tu dois récupérer deux valeurs à comparer. Pour simplfier le calcul, il suffit de multiplier le nombre de personnes par 2 dans la boucle et de traiter chaque entrée 1 par 1. A partir de là, c'est simple. Si le chiffre est positif, une personne entre, s'il est négatif, une personne sort. Toi, tu veux garder en mémoire le nombre maximum de personnes qu'il y a eu en même temps ! A toi de faire les calculs et d'assigner cette valeur à chaque fois qu'elle est atteinte.

```
Je récupère nbPersonnes
J'initialise nbMax à 0
J'initialise nbActuel à 0
Je répète nbPersonnes * 2 fois
  Je récupère numéro
  Si numéro > 0
    J'ajoute 1 à nbActuel
    Si nbActuel > nbMax
      nbMax prend la valeur de nbActuel
  sinon
    J'enlève 1 à nbActuel
J'affiche nbMax
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbPersonnes = int(input())
nbMax = 0
nbActuel = 0
for loop in range(nbPersonnes * 2):
   numero = int(input())
   if numero > 0:
      nbActuel = nbActuel + 1
      if nbActuel > nbMax:
         nbMax = nbActuel
   else:
      nbActuel = nbActuel - 1
print(nbMax)
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
      int nbPersonnes = entrée.nextInt();
      int nbMax = 0, nbActuel = 0;
      for (int loop = 1; loop <= nbPersonnes * 2; loop = loop + 1)
      {
         int numéro = entrée.nextInt();
         if(numéro > 0)
         {
            nbActuel = nbActuel + 1;
            if(nbActuel > nbMax)
            {
               nbMax = nbActuel;
            }
         }
         else
         {
            nbActuel = nbActuel - 1;
         }
      }
      System.out.println(nbMax);
   }
}
```

</details>
