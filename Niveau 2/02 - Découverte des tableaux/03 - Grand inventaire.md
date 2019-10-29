# Grand inventaire

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 On commence par créer un tableau qui contiendra la quantité de chaque produit. Au début tout est à zéro, puis on va lire chacune des lignes du livre de comptes et à chaque fois on modifiera la quantité du produit correspondant. À la fin, il suffit d'afficher les éléments du tableau, l'un après l'autre.

La difficulté de cet exercice c'est que les indices démarrent à 1 et pas 0, comment faire ?

    Changer à chaque fois les indices, c'est-à-dire leur enlever 1 : cette solution n'est pas conseillée car on a alors deux systèmes d'indices. Un dans lequel les indices démarrent à 0, dans le code. Un dans lequel les indices démarrent à 1, dans le sujet et les tests. On risque alors de confondre les deux systèmes et de faire des bugs !
    Utiliser un tableau plus grand : on utilise un tableau de taille 11 mais on ne s'occupera que des 10 derniers éléments, on ne touchera jamais à celui d'indice 0. C'est la solution recommandée.

La deuxième solution est fortement conseillée car elle permet de manipuler les mêmes indices que ceux des tests et du sujet. Ce n'est pas du tout un problème de ne pas utiliser une des cases du tableau. 

```
quantite <- [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
nbLignes <- LireEntier()
Répéter nbLignes fois
   numeroProduit <- LireEntier()
   variation <- LireEntier()
   quantite[numeroProduit] <- quantite[numeroProduit] + variation
Pour numeroProduit allant de 1 à 10
   Afficher quantite[numeroProduit]
```

## Python

<details>
  <summary>Solution</summary>

```Python
quantite = [0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0]
nbLignes = int(input())
for idLigne in range(nbLignes):
   numeroProduit = int(input())
   variation = int(input())
   quantite[numeroProduit] = quantite[numeroProduit] + variation
for numeroProduit in range(1, 11):
   print(quantite[numeroProduit])
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
      int[] quantite = {0, 0, 0, 0, 0, 0, 0, 0, 0, 0, 0};
      int nbLignes = entrée.nextInt();
      for (int idLigne = 0; idLigne < nbLignes; idLigne = idLigne + 1)
      {
         int numeroProduit = entrée.nextInt();
         int variation = entrée.nextInt();
         quantite[numeroProduit] = quantite[numeroProduit] + variation;
      }
      for (int numeroProduit = 1; numeroProduit <= 10; numeroProduit = numeroProduit + 1)
      {
         System.out.println(quantite[numeroProduit]);
      }
   }
}
```

</details>
