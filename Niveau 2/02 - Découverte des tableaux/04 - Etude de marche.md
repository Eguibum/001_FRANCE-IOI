# Etude de marché

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 On commence par créer un tableau qui contiendra le nombre de personnes désirant chaque produit. Ce tableau a donc une taille dépendant du nombre total de produits disponibles.

Ensuite on lit les souhaits de chaque personne et on met à chaque fois à jour ce tableau en ajoutant 1 dans la bonne case.

Enfin, il ne nous reste qu'à afficher chaque élément du tableau. 

```
nbProduits <- LireEntier()
nbSouhaits <- Tableau de taille nbProduits contenant des 0
nbPersonnes <- LireEntier()
Répéter nbPersonnes fois
   numeroProduit <- LireEntier()
   nbSouhaits[numeroProduit] <- nbSouhaits[numeroProduit] + 1
Pour numeroProduit allant de 0 à nbProduits-1
   Afficher nbSouhaits[numeroProduit]
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbProduits = int(input())
nbSouhaits = [0] * nbProduits
nbPersonnes = int(input())
for idPersonne in range(nbPersonnes):
   numeroProduit = int(input())
   nbSouhaits[numeroProduit] = nbSouhaits[numeroProduit] + 1
for numeroProduit in range(nbProduits):
   print(nbSouhaits[numeroProduit])
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
      int nbProduits = entrée.nextInt();
      
      int[] nbSouhaits = new int[nbProduits];
      for (int numeroProduit = 0; numeroProduit < nbProduits; numeroProduit = numeroProduit + 1)
      {
         nbSouhaits[numeroProduit] = 0;
      }
      
      int nbPersonnes = entrée.nextInt();
      for (int idPersonne = 0; idPersonne < nbPersonnes; idPersonne = idPersonne + 1)
      {
         int numeroProduit = entrée.nextInt();
         nbSouhaits[numeroProduit] = nbSouhaits[numeroProduit] + 1;
      }
       
      for (int numeroProduit = 0; numeroProduit < nbProduits; numeroProduit = numeroProduit + 1)
      {
         System.out.println(nbSouhaits[numeroProduit]);
      }
   }
}
```

</details>
