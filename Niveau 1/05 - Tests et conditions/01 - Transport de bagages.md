# Transport de bagages

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

A partir de ce chapitre, on rentre dans les conditions de tests. Ici, tu récupère donc 2 valeurs à assigner respectivement à nombrePaquets et poidsPaquets, tu calcules le total et tu vérifies si le poidsTotal dépasse 105. En conséquence, tu affiche Surcharge ! si le poids dépasse, sinon rien.

```
Je récupère le nombre de paquets
je récupère le poids des paquets
je calcule le total = nombres de paquets * poids des paquets
Si total dépasse 105
  j'affiche Surcharge !
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbPaquets = int(input())
poidsPaquet = int(input())
if nbPaquets * poidsPaquet > 105:
   print("Surcharge !")
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
      int nbPaquets = entrée.nextInt();
      int poidsPaquet = entrée.nextInt();
      if (nbPaquets * poidsPaquet > 105) {
         System.out.println("Surcharge !");
      }
   }
}
```

</details>
