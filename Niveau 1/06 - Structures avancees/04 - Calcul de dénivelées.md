# Calcul de dénivelées

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Sur un chemin en dent de scie, ça monte et ça descend. Ce qu'on veut, c'est que tu calcules le total de montées et le total de descente, et que tu affiches ces totaux à la fin (sous forme d'entiers positifs). Il faut donc répartir chaque mesure dans le bon groupe, et afficher le groupe des descentes en positif. Finger in ze noze, si j'ose dire (Sauf pour Voldemort)

```
J'initialise totalMontée à 0
J'initialise totalDescente à 0
Je récupère le nombre de montée et descente
Je répète autant de fois que de montée et descente
  Je recupère la variation d'altitude
  Si la variation est supérieure à 0
    Je l'ajoute à totalMontée
  Sinon
    Je la soustrait à totalDescente (et oui, car 0 -- 1 = 0 + 1 = 1 <= résultat positif)
J'affiche totalMontée
J'affiche totalDescente
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbVariations = int(input())
sommePos = 0
sommeNeg = 0
for loop in range(nbVariations):
   variation = int(input())
   if variation > 0:
      sommePos = sommePos + variation
   else:
      sommeNeg = sommeNeg - variation
print(sommePos)
print(sommeNeg)
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
      int nbVariations = entrée.nextInt();
      int sommePos = 0;
      int sommeNeg = 0;
      for (int loop = 1; loop <= nbVariations; loop = loop + 1)
      {
         int variation = entrée.nextInt();
         if (variation > 0)
         {
            sommePos = sommePos + variation;
         }
         else
         {
            sommeNeg = sommeNeg - variation;
         }
      }
      System.out.println(sommePos);
      System.out.println(sommeNeg);
   }
}
```

</details>
