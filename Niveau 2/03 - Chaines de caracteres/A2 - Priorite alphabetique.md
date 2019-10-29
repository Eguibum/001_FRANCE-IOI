# Priorité alphabétique

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On commence par lire les deux noms, puis il faut les comparer pour savoir lequel est le plus petit selon l’ordre alphabétique. Il suffit alors de l’afficher. Il faut bien faire attention à ne rien afficher si les deux noms sont égaux. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
nom1 = input()
nom2 = input()
if nom1 < nom2:
   print(nom1)
elif nom1 > nom2:
   print(nom2)
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
      String nom1 = input.nextLine();
      String nom2 = input.nextLine();
      int ordre = nom1.compareTo(nom2);
      if (ordre < 0)
      {
         System.out.println(nom1);
      }
      else if (ordre > 0)
      {
         System.out.println(nom2);
      }
   }
}
```

</details>
