# Caserne de pompiers

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

L'exercie peut sembler ardu, mais un simple dessin peut faciliter la compréhension. Ici, il faut déterminer si les zones se chevauchent et afficher OUI, sinon il faut afficher NON (on n'oublie pas que si elles ne font que se toucher, il faut afficher NON). Du coup, plutôt que de vérifier toutes les intersections possibles, le mieux est de vérifier si les zones ne se touchent pas. En effet, on sait que si les coordonnées des rectangles, rapportés sur les axes, ne se touchent pas, alors les zones ne se superposent pas. Donc, comme dans le cas des amitiés entre garde, on va faire nos tests en cherchant la non-intersection :)

```
Je récupère le nombre de paires
Je répètea autant de fois qu'il y a de père
  Je récupère xMin1
  Je récupère xMin2
  Je récupère xMax1
  Je récupère xMax1
  Je récupère yMin1
  Je récupère yMin2
  Je récupère yMax1
  Je récupère yMax1
    Si ( (xMax2 <= xMin1) ou (xMax1 <= xMin2) ) ou ( (yMax2 <= yMin1) ou (yMax1 <= yMin2) ) alors
      Afficher "NON"
   Sinon
      Afficher "OUI"
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbPaires = int(input())
for loop in range(nbPaires):
   xMin1 = int(input())
   xMax1 = int(input())
   yMin1 = int(input())
   yMax1 = int(input())
   xMin2 = int(input())
   xMax2 = int(input())
   yMin2 = int(input())
   yMax2 = int(input())
   if ( (xMax2 <= xMin1) or (xMax1 <= xMin2) ) or ( (yMax2 <= yMin1) or (yMax1 <= yMin2) ):
      print("NON")
   else:
      print("OUI")
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
      int nbPaires = entrée.nextInt();
      for (int loop = 1; loop <= nbPaires; loop = loop + 1)
      {
         int xMin1 = entrée.nextInt();
         int xMax1 = entrée.nextInt();
         int yMin1 = entrée.nextInt();
         int yMax1 = entrée.nextInt();
         int xMin2 = entrée.nextInt();
         int xMax2 = entrée.nextInt();
         int yMin2 = entrée.nextInt();
         int yMax2 = entrée.nextInt();
       
         if((xMax2 <= xMin1) || (xMax1 <= xMin2) || (yMax2 <= yMin1) || (yMax1 <= yMin2))
         {
            System.out.println("NON");
         }
         else
         {
            System.out.println("OUI");
         }
      }
   }
}
```

</details>
