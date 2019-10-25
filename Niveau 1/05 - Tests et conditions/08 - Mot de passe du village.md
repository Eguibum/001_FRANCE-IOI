# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Cette fois, au lieu de tester la différence (stricte ou égale), on cherche à trouver une égalité. LA subtilité, c'est le == au lieu de = : un seul = assigne une valeur, alors que == compare les valeurs ;)

Donc ici, le robot doit avoir en mémoire le code secret, et les gens lui donnent un code. Si le code donné est identique au code enregistré, ils peuvent passer, sinon ils doivent partir.

```
Je récupère le code proposé
Si le code proposé est égal au code secret
  J'affiche Bon festin !
Sinon
  J'affiche Allez-vous-en !
```

## Python

<details>
  <summary>Solution</summary>

```Python
tentative = int(input())
if tentative == 64741:
   print("Bon festin !")
else:
   print("Allez-vous-en !")
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
      int tentative = entrée.nextInt();
      if (tentative == 64741) {
         System.out.println("Bon festin !");
      } else {
         System.out.println("Allez-vous-en !");
      }
   }
}
```

</details>
