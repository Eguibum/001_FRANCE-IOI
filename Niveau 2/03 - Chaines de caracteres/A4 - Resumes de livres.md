# Résumés de livres

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On va utiliser une boucle pour lire le titre et le résumé de chacun des livres. On teste alors si la longueur du résumé est suffisante et si ce n'est pas le cas, on affiche le titre du livre. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
nbLivres = int(input())
longueurMinimale = int(input())
for loop in range(nbLivres):
   titre = input()
   resume = input()
   if len(resume) < longueurMinimale:
      print(titre)
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
      int longMinResumé = entrée.nextInt();
      for (int idLivre = 0; idLivre < nbLivres; idLivre = idLivre + 1)
      {
         String titre = entrée.nextLine();
         String résumé = entrée.nextLine();
         if (résumé.length() < longMinResumé)
         {
            System.out.println(titre);
         }
      }
   }
}
```

</details>
