# Type d'arbres

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Dans cet exercice, il faut différencier 4 types d'arbres qui ont chacun leur propre type de feuilles, ça fait beaucoup de critères. Plutôt que de se palanquer une liste longue comme un jour sans pain de comparaisons, essayons de regrouper les critères pour faciliter le tri.

Tu remarques que les arbres ont pour critères leur taille (-5, -8, +10 ou +12) et leur folioles sur leurs feuilles (-5, -7, +8 ou +10). Tu peux donc partager en 2 grands groupes : les arbres qui font moins de 9m et ceux qui ont plus de 6 folioles (la valeur étant de 8 pour les plus grand arbres)

```
Je récupère la valeur de la hauteur
Je récupère la valeur du nombre de folioles
Si l'arbre fait moins de 9m
  Si le nombre de folioles est supérieur à 6
    J'affiche Tinuviel
  Sinon
    J'affiche Falarion
Sinon
  Si le nombre de folioles est inférieur à 8
    J'affiche Dorthonion
  Sinon
   J'affiche Calaelen
```

## Python

<details>
  <summary>Solution</summary>

```Python
hauteur = int(input())
nbFolioles = int(input())
if hauteur < 9:
   if nbFolioles > 6:
      print("Tinuviel")
   else:
      print("Falarion")
else:
   if nbFolioles < 8:
      print("Dorthonion")
   else:
      print("Calaelen")
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
      int hauteur = entrée.nextInt();
      int nbFolioles = entrée.nextInt();
      if(hauteur < 9)
      {
         if(nbFolioles > 6)
         {
            System.out.println("Tinuviel");
         }
         else
         {
            System.out.println("Falarion");
         }
      }
      else
      {
         if(nbFolioles < 8)
         {
            System.out.println("Dorthonion");
         }
         else
         {
            System.out.println("Calaelen");
         }
      }
   }
}
```

</details>
