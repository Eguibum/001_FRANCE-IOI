# Code secret deux fois

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

La solution algorithmique est similaire à ce que nous avons pu voir dans le chapitre sur la répétition « tant que ». Nous utilisons ci-dessous une fonction attendreCode pour séparer ce bloc du reste du programme, et rendre celui-ci plus court et plus clair. 

Nous profitons de cette correction pour vous présenter une boucle pilotée par le bas : « faire … tant que » qui existe dans certains langages ; elle est similaire à une boucle « tant que » sauf que le premier tour est toujours exécuté. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
def attendreCode():
   tentative = 0
   while tentative != 4242:
      print("Entrez le code :")
      tentative = int(input())
attendreCode()
print("Encore une fois.")
attendreCode()
print("Bravo.")
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
   static void attendreCode() {
      int tentative = 0;
      do {
         System.out.println("Entrez le code :");
         tentative = entrée.nextInt();
      }
      while (tentative != 4242);
   }
   public static void main(String[] args) {
      attendreCode();
      System.out.println("Encore une fois.");
      attendreCode();
      System.out.println("Bravo.");
   }
}
```

</details>
