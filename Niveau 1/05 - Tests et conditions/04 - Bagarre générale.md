# Bagarre générale

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Il faut calculer la surface de chaque champ et vérifier qu'il n'y a pas plus de 10 de différence entre les 2 champs.

```
Je récupère la valeur du champ Arignon
Je récupère la valeur du champ Evaran
Si la différence entre champ Arignon et champ Evaran est supérieur à 10
  J'affiche la famille Arignon a un champ trop grand
Si la différence entre champ Evaran et champ Arignon est supérieur à 10
  J'affiche la famille Evaran a un champ trop grand
```

## Python

<details>
  <summary>Solution</summary>

```Python
superficieArignon = int(input())
superficieEvaran = int(input())
if superficieArignon > superficieEvaran + 10:
   print("La famille Arignon a un champ trop grand")
if superficieEvaran > superficieArignon + 10:
   print("La famille Evaran a un champ trop grand")
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
      int aireArignon = entrée.nextInt();
      int aireEvaran = entrée.nextInt();
      if (aireArignon  - aireEvaran  > 10) {
         System.out.println("La famille Arignon a un champ trop grand");
      }
      if (aireEvaran  - aireArignon  > 10) {
         System.out.println("La famille Evaran a un champ trop grand");
      }
   }
}
```

</details>
