# Tarif du bateau

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Le but est de savoir combien va payer le passant selon son âge. Plutôt que de répéter les conditions avec uniquement des if, on va utiliser la forme if / else qui se traduit par si / sinon. Si le passant a strictement moins de 21 il pait le tarif réduit, sinon il paie le tarif plein.

```
Je récupère l'age de la personne
Si la personne a strictement moins de 21 ans
  J'affiche Tarif réduit
Sinon
  J'affiche Tarif plein
```

## Python

<details>
  <summary>Solution</summary>

```Python
âge = int(input())
if âge < 21:
   print("Tarif réduit")
else:
   print("Tarif plein")
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
      int âge = entrée.nextInt();
      if (âge < 21) {
         System.out.println("Tarif réduit");
      } else {
         System.out.println("Tarif plein");
      }
   }
}
```

</details>
