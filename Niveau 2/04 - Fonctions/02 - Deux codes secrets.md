# Deux codes secrets

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

L"exercice est très similaire au précédent, nous introduisons ci-dessous un argument entier codeSecret dans la fonction. En gros, l'argument de la fonction est le code secret à trouver. Tant que la tentative du joueur est différente, ça tourne :)

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
def lireCode(code):
   tentative = code + 1
   while tentative != code:
      print("Entrez le code :")
      tentative = int(input())
lireCode(4242)
print("Premier code bon.")
lireCode(2121)
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
   static void attendreCode(int codeSecret) {
      int tentative;
      do {
         System.out.println("Entrez le code :");
         tentative = entrée.nextInt();
      }
      while (tentative != codeSecret);
   }
   public static void main(String[] args) {
      attendreCode(4242);
      System.out.println("Premier code bon.");
      attendreCode(2121);
      System.out.println("Bravo.");
   }
}
```

</details>
