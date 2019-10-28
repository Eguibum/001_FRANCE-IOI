# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 La principale difficulté de cet exercice est de trouver la bonne condition pour la boucle « tant que ». On veut en effet la plus grande pyramide constructible avec moins de pierres que la limite qu'on nous donne. On ne peut donc pas calculer le nombre de pierres de chaque taille de pyramide et tester si cette valeur est plus grande que la limite : il faut s'arrêter avant que l'on atteigne cette limite.

La manière la plus simple de faire est de se poser la question suivante : est-ce que le nombre de pierres de cette pyramide, si je lui ajoutais un étage, est plus petit que le nombre maximum de pierres autorisées ? Si oui, alors on peut en toute sécurité ajouter un étage ; sinon, on sait qu'il faut s'arrêter, et le nombre de pierres de la pyramide actuelle est la réponse qui est attendue. 

```
nbMaxPierres <- lireEntier()
nbPierres <- 0
hauteur <- 1
Tant que nbPierres + hauteur * hauteur <= nbMaxPierres
   nbPierres <- nbPierres + hauteur * hauteur
   hauteur <- hauteur + 1
Afficher hauteur - 1
Afficher nbPierres
```

## Python

<details>
  <summary>Solution</summary>

```Python
nombreMaximumPierres = int(input())
nombrePierres = 0
hauteur = 1
while nombrePierres + hauteur * hauteur <= nombreMaximumPierres:
   nombrePierres = nombrePierres + hauteur * hauteur
   hauteur = hauteur + 1  
print(hauteur - 1)
print(nombrePierres)
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
      int nombreMaximumPierres = entrée.nextInt();
      int nombrePierres = 0;
      int hauteur = 1;
      while (nombrePierres + hauteur * hauteur <= nombreMaximumPierres)
      {
         nombrePierres = nombrePierres + hauteur * hauteur;
         hauteur = hauteur + 1;
      }
      System.out.println(hauteur - 1);
      System.out.println(nombrePierres);
   }
}
```

</details>
