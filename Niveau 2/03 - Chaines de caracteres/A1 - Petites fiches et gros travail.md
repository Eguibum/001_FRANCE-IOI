# Petites fiches et gros travail

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 L’algorithme à utiliser est simple, car il suffit de faire 6 fois (donc à l’aide d’une boucle) les opérations suivantes :

    Lire la ligne contenant le nom de l’auteur
    Lire la ligne contenant le titre du livre
    Afficher le titre du livre
    Afficher le nom de l’auteur


```

```

## Python

<details>
  <summary>Solution</summary>

```Python
for idLivre in range(6):
   nomAuteur = input()
   titreLivre = input()
   print(titreLivre)
   print(nomAuteur)
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
      Scanner input = new Scanner(System.in);
      for (int livre = 0; livre < 6; livre = livre + 1)
      {
         String auteur = input.nextLine();
         String titre  = input.nextLine();
         System.out.println(titre);
         System.out.println(auteur);
      }
   }
}
```

</details>
