# Âge des petits-enfants

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Un exercice de correction. C'est toujours intéressant, car ça apprend à lire le code de quelqu'un d'autre. Il ne faut pas se leurrer, on ne code pas tous exactement de la même manière. Donc c'est instructif de voir si l'on est capable de comprendre le raisonnement d'un autre et d'y détecter, s'il yen a, des erreurs.

```
Il manque le System.in dans l'import du Scanner ligne 5
Il manque les () après nextInt ligne 6
Il faut utiliser nextInt() et pas nextint() ligne 7
La variable s'appelle âgeCadet et non âgeDuCadet ligne 8
```

## Python

<details>
  <summary>Solution</summary>

```Python
âgeCadet = int(input())
âgeAîné = int(input())
différence = âgeAîné - âgeCadet
print(différence)
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
      int âgeCadet = entrée.nextInt();
      int âgeAîné = entrée.nextInt();
      int différence = âgeAîné - âgeCadet;
      System.out.println(différence);
   }
}
```

</details>
