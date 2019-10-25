# Traversée du pont

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Ici on récupère 2 entiers qui équivaut à 2 jets de dés. Si leur somme est supérieure ou égale à 10, on paie la taxe spéciale, sinon on paie deux fois la somme des dés.

```
Je récupère le premier jet de dé
Je récupère le deuxième jet de dé
J'initialise ma valeur somme avec la somme des deux jets de dés
Si la somme est supérieur ou égale à 10
  J'affiche Taxe spéciale !
  J'affiche 36
Sinon
  J'affiche Taxe régulière
  J'affiche somme * 2
```

## Python

<details>
  <summary>Solution</summary>

```Python
premierDé = int(input())
secondDé = int(input())
somme = premierDé + secondDé
if somme >= 10:
   print("Taxe spéciale !")
   print(36)
else:
   print("Taxe régulière")
   print(2 * somme)
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
      int premierDé = entrée.nextInt();
      int secondDé = entrée.nextInt();
      int somme = premierDé + secondDé;
      if (somme >= 10) {
         System.out.println("Taxe spéciale !");
         System.out.println(36);
      } else {
         System.out.println("Taxe régulière");
         System.out.println(2 * somme);
      }
   }
}
```

</details>
