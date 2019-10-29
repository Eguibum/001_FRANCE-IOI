# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Une fois lu le nombre total de lignes, on va lire chacune des lignes, puis tester si son numéro est impair (à l’aide de l’opérateur "modulo") et l’afficher si c’est le cas. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
nbLignes = int(input())
for idLigne in range(nbLignes):
   ligne = input()
   if idLigne % 2 == 0:
      print(ligne)
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
import java.util.Scanner;
class Main
{
   public static void main(String[] args)
   {
      Scanner entrée = new Scanner(System.in);
      int nbLignes = entrée.nextInt();
      for (int iLigne = 0; iLigne < nbLignes; iLigne = iLigne + 1)
      {
         String ligne = entrée.nextLine();
         if (iLigne % 2 == 0)
         {
            System.out.println(ligne);
         }
      }
   }
}
```

</details>
