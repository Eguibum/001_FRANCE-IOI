# Conversions des distances

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

La première chose à faire est de lire le nombre de lieues et de le stocker dans une variable. Pour trouver le nombre de kilomètres correspondant, on peut remarquer que si 1 kilomètre = 0.707 lieues alors 1 lieu = 1/0.707 kilomètres, 2 lieues = 2/0.707 kilomètres... 

```
lieues <- LireDecimal()
kilometres <-  lieues / 0.707
Afficher kilometres
```

## Python

<details>
  <summary>Solution</summary>

```Python
lieues = float(input())
kilometres = lieues / 0.707
print(kilometres)
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
      double lieues = entrée.nextDouble();
      System.out.println(lieues / 0.707);
   }
}
```

</details>
