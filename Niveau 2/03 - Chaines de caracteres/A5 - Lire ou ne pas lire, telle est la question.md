# Lire ou ne pas lire, telle est la question

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 On ne va donc afficher un titre de livre que s’il est plus long que tous les titres qu’on a affichés précédemment, ce qui revient à dire qu’il est plus long que le dernier titre affiché, étant donné que chaque titre est forcément plus long que le précédent.

Il faut donc mémoriser la longueur du plus grand titre affiché et si un nouveau titre est plus long que cette longueur mémorisée, alors on affiche le titre et on met à jour cette longueur.

Cela ressemble donc un peu à un calcul de maximum. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
nbLivres = int(input())
longueurPlusLongTitre = 0
for loop in range(nbLivres):
   titreLivre = input()
   longueurTitre = len(titreLivre)
   if longueurTitre > longueurPlusLongTitre:
      longueurPlusLongTitre = longueurTitre
      print(titreLivre)
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
      int nbLivres = entrée.nextInt();
      int longueurMinimum = 0;
      for (int livre = 0; livre < nbLivres; livre = livre + 1)
      {
         String titre = entrée.nextLine();
         if (titre.length() > longueurMinimum)
         {
            System.out.println(titre);
            longueurMinimum = titre.length();
         }
      }
   }
}
```

</details>
