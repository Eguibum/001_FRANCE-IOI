# Maisin de l'espion

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

C'est un peu le même principe que le périmètre de protection, vu en Structures avancées - exercice 7.

Sauf qu'ici, tu as déjà les abcisses et ordonnées max et min du rectangle à controler. Tu dois donc vérifier que l'abscisse ou l'ordonnée de la maison est dans de cette zone. Pour cela, l'abscisse de la maison doit être entre l'abscisse min et max du rectangle et que l'ordonnée est entre l'ordonnée min et max du rectangle. C'est parti !

```
Je récupère abscisseMin
Je récupère abscisseMax
Je récupère ordonnéeMin
Je récupère ordonnéeMAx
Je récupère nbMaisons
J'initialise nbAFouiller à 0
Je répète nbMaisons fois
  Je récupère abscisse
  Je récupère ordonnée
  Si abscisseMin <= abscisse ET abscisse <= abscisseMax ET ordonnéeMin <= ordonnée ET ordonnée <= ordonnéeMax
    J'ajoute 1 à nbAFouiller
J'affiche nbAFouiller
```

## Python

<details>
  <summary>Solution</summary>

```Python
xMin = int(input())
xMax = int(input())
yMin = int(input())
yMax = int(input())
nbMaisons = int(input())
nbAFouiller = 0
for loop in range(nbMaisons):
   x = int(input())
   y = int(input())
   if (xMin <= x) and (x <= xMax) and (yMin <= y) and (y <= yMax):
      nbAFouiller = nbAFouiller + 1
print(nbAFouiller)
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
      int xMin = entrée.nextInt();
      int xMax = entrée.nextInt();
      int yMin = entrée.nextInt();
      int yMax = entrée.nextInt();
      int nbMaisons = entrée.nextInt();
      int nbAFouiller = 0;
      
      for (int loop = 1; loop <= nbMaisons; loop = loop + 1)
      {
         int x = entrée.nextInt();
         int y = entrée.nextInt();
         if( (xMin <= x) && (x <= xMax) && (yMin <= y) && (y <= yMax))
         {
            nbAFouiller = nbAFouiller + 1;
         }
      }
      System.out.println(nbAFouiller);
   }
}
```

</details>
