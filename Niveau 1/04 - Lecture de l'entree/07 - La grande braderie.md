# La grande braderie

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

C'est exactement le même principe que l'exercice des thermomètres, sauf que tu n'as pas de valeur de fin, juste une valeur de début.

```
Je récupère la position de départ
Je récupère la largeur d'un emplacement
Je récupère le nombre de vendeurs
Je répète autant de fois qu'il y a de vendeur
  J'affiche la position
  J'assigne à position = position + largeur de l'emplacement
```

## Python

<details>
  <summary>Solution</summary>

```Python
positionDépart = int(input())
largeurEmplacement = int(input())
nbVendeurs = int(input())
position = positionDépart
for iVendeur in range(nbVendeurs + 1):
   print(position)
   position = position + largeurEmplacement
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
      int positionDépart = entrée.nextInt();
      int largeurEmplacement = entrée.nextInt();
      int nbVendeurs = entrée.nextInt();
      int position = positionDépart;
      for (int iVendeur = 0; iVendeur <= nbVendeurs; iVendeur = iVendeur + 1) {
         System.out.println(position);
         position = position + largeurEmplacement;
      }
   }
}
```

</details>
