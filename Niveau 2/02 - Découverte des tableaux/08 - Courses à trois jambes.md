# Courses à trois jambes

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On commence par lire toutes les valeurs, puis on les trie. Ensuite, on utilise une variable idPremier qui représente la position dans le tableau de la première personne. Cette variable vaut à l'origine 0 et augmente de 1 à chaque couple, jusqu'à valoir nbPersonnes ÷ 2 − 1, c'est-à-dire à être au milieu du tableau. À chaque fois, la position de la seconde personne vaut donc nbPersonnes − 1 − idPremier :

```
0 <--> nbPersonnes - 1 - 0 = nbPersonnes - 1
1 <--> nbPersonnes - 1 - 1 = nbPersonnes - 2
2 <--> nbPersonnes - 1 - 2 = nbPersonnes - 3
...
nbPersonnes / 2 - 1 <--> nbPersonnes - 1 - (nbPersonnes / 2 - 1) = nbPersonnes / 2
```

Le pseudo-code
```
nbPersonnes <- lireEntier()
numéros <- tableau de taille nbPersonnes contenant des 0
Pour idPersonne allant de 0 à nbPersonnes - 1
   numéros[idPersonne] <- lireEntier()
Trier numéros
Pour idPremier allant de 0 à nbPersonnes / 2 - 1
   idSecond <- nbPersonnes - 1 - idPremier
   Afficher numéros[idPremier], " ", numéros[idSecond]
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbPersonnes =  int(input())
numeros = [0] * nbPersonnes
for idPersonne in range(nbPersonnes):
   numeros[idPersonne] = int(input())
 
numeros.sort()
for idPremier in range(nbPersonnes // 2):
   idSecond = nbPersonnes - 1 - idPremier
   print("{} {}".format(numeros[idPremier], numeros[idSecond]))
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
      int[] numeros = new int[nbPersonnes];
      for (int idPersonne = 0; idPersonne < nbPersonnes; idPersonne = idPersonne + 1)
      {
         numeros[idPersonne] = entrée.nextInt();
      }
        
      sort(numeros);
        
      for (int idPremier = 0; idPremier  < nbPersonnes / 2; idPremier = idPremier  + 1)
      {
         int idSecond = nbPersonnes - 1 - idPremier;
         System.out.println( numeros[idPremier] + " " + numeros[idSecond] );
      }
   }
}
```

</details>
