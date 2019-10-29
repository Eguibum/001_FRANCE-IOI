# Journée des cadeaux

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 Pour trouver la (les deux) valeur(s) du milieu on peut commencer par stocker toutes les valeurs dans un tableau puis trier ce tableau. Il faut ensuite faire attention au calcul de l'indice du milieu. Une bonne technique pour cela est de regarder sur un exemple. On a deux cas à traiter, selon la parité du nombre d'éléments :

    - Cas impair (11 élements) : on cherche à avoir la sixième valeur donc celle d'indice égal à 5. Pour obtenir 5 à partir de 11 on fait tout simplement (11 - 1) / 2.

    - Cas pair (12 élements) : on cherche à calculer la moyenne des sixième et septième valeurs donc celles d'indices égaux à 5 et 6. Pour obtenir 5 et 6 à partir de 12 on fait tout simplement (12 / 2 - 1) et (12 / 2).

La valeur qu'on demandait de calculer dans cet exercice s'appelle la médiane de l'ensemble des fortunes. 

```
nbPersonnes <- LireEntier()
fortune <- Tableau de taille nbPersonnes contenant des 0
Pour idPersonne allant de 0 à nbPersonnes-1 fois
   fortune[idPersonne] <- LireEntier()
Trier(fortune)
Si Modulo(nbPersonnes, 2) = 1
   milieu <- (nbPersonnes - 1) / 2
   Afficher fortune[milieu]
Sinon
   milieu <- nbPersonnes / 2
   Afficher ( fortune[milieu - 1] + fortune[milieu] ) / 2
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbPersonnes = int(input())
fortune = [0] * nbPersonnes
for idPersonne in range(nbPersonnes):
   fortune[idPersonne] = int(input())
fortune.sort()
if nbPersonnes % 2 == 1:
   milieu = (nbPersonnes - 1) // 2
   print( fortune[milieu] )
else:
   milieu = nbPersonnes // 2
   print( ( fortune[milieu - 1] + fortune[milieu] ) / 2 )
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
import static java.util.Arrays.*;
class Main
{
   public static void main(String[] args)
   {
      Scanner entrée = new Scanner(System.in);
      int nbPersonnes = entrée.nextInt();
      int [] fortune = new int[nbPersonnes];
      for (int idPersonne = 0; idPersonne < nbPersonnes; idPersonne = idPersonne + 1)
      {
         fortune[idPersonne] = entrée.nextInt();
      }
       
      sort(fortune);
       
      if ((nbPersonnes % 2) == 1)
      {
         int milieu = (nbPersonnes - 1) / 2;
         System.out.println( fortune[milieu] );
      }
      else
      {
         int milieu = nbPersonnes / 2;
         System.out.println( (double)( fortune[milieu - 1] + fortune[milieu] ) / 2 );
      }
   }
}
```

</details>
