# Banquet municipal

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

L'algorithme est constitué de trois parties : lire les numéros initiaux, faire les changements, afficher les valeurs finales. Seule la deuxième partie demande à être détaillée. En effet, la principale difficulté est de savoir comment inverser les valeurs de deux éléments d'un tableau.

Une première idée, pour inverser les éléments d'indices 0 et 2, consiste à utiliser le code suivant :
```
numero <- [1, 2, 3]    # numero contient 1,2,3
numero[0] <- numero[2] # numero contient 3,2,3
numero[2] <- numero[0] # numero contient 3,2,3
```

mais on voit que cela ne marche pas, car on a effacé la valeur de "numero[0]" avant de pouvoir la lire pour la mettre dans "numero[2]". Il faut donc trouver un moyen de stocker cette valeur quelque part, par exemple dans une autre variable :
```
numero <- [1, 2, 3]    # numero contient 1,2,3
temp <- numero[0]      # numero contient 1,2,3 et temp contient 1
numero[0] <- numero[2] # numero contient 3,2,3 et temp contient 1
numero[2] <- temp      # numero contient 3,2,1 et temp contient 1
```

Une fois cette difficulté surmontée, le reste du programme est facile à écrire. 

```
nbPersonnes <- LireEntier()
nbChangements <- LireEntier()
identifiant <- Tableau de taille nbPersonnes contenant des 0
Pour idPersonne allant de 0 à nbPersonnes-1
   identifiant[idPersonne] <- LireEntier()
Répéter nbChangements fois
   premier <- LireEntier()
   second <- LireEntier()
   temp <- identifiant[premier]
   identifiant[premier] <- identifiant[second]
   identifiant[second] <- temp
Pour idPersonne allant de 0 à nbPersonnes-1
   Afficher identifiant[idPersonne]
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbPersonnes = int(input())
nbChangements = int(input())
identifiant = [0] * nbPersonnes
for idPersonne in range(nbPersonnes):
   identifiant[idPersonne] = int(input())
for idChang in range(nbChangements):
   premier = int(input())
   second = int(input())
   temp = identifiant[premier]
   identifiant[premier] = identifiant[second]
   identifiant[second] = temp
for idPersonne in range(nbPersonnes):
   print(identifiant[idPersonne])
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
      int nbPersonnes = entrée.nextInt();
      int nbChangements = entrée.nextInt();
      int[] identifiant = new int[nbPersonnes];
      
      for (int idPersonne = 0; idPersonne < nbPersonnes; idPersonne = idPersonne + 1)
      {
         identifiant[idPersonne] = entrée.nextInt();
      }
       
      for (int idChang= 0; idChang < nbChangements; idChang = idChang + 1)
      {
         int premier = entrée.nextInt();
         int second = entrée.nextInt();
         int temp = identifiant[premier];
         identifiant[premier] = identifiant[second];
         identifiant[second] = temp;
      }
       
      for (int idPersonne = 0; idPersonne < nbPersonnes; idPersonne = idPersonne + 1)
      {
         System.out.println(identifiant[idPersonne]);
      }
   }
}
```

</details>
