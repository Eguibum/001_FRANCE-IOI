# Retraite spirituelle

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Encore du calcul à faire ! Ici on te dit que lors de cette retraite, chaque seconde, pendant 16h par jour, tu répètes une incantation. L'inconnue, c'est le nombre de jour, donc c'est cela que tu récupère. Ensuite, il te fait le nombre de seconde. A savoir : 60 *  60 = 3 600. Il y a donc 3 600 secondes dans u&H. A partir de là, c'est plutôt facile.

```
Je récupère le nombre de jours
J'affiche le nombre de jours * 16h * 3 600 secondes
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbJours = int(input())
print(3600 * 16 * nbJours)
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
      int nbJours = entrée.nextInt();
      System.out.println(nbJours * 16 * 3600);
   }
}
```

</details>
