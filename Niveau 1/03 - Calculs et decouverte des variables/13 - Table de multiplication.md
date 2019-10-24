# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

La table de multiplication ressemble un peu à l'exercice du jeu de dames, mais cette fois-ci il faut prendre en compte 2 variables qui vont évoluer au fil des boucle. Si on écrivait ça sur papier, on aurait un tableau avec en lignes les nombres de 1 à 20 et en colonne les nombres de 1 à 20, ça ressemblerait à ça :

1 2 3 4 5
2
3
4
5

En gardant ça en mémoire, on va définir nos variables et nos boucles.

```
Je définis ma variable ligne à 1
Je répète 20 fois
  Je définis ma variable colonne à 1
  Je répète 20 fois
    J'affiche le résultat de ligne * colonne
    Je rajoute & à colonne
  J'affiche une ligne vide
  Je rajoute 1 a ligne
```

## Python

<details>
  <summary>Solution</summary>

```Python
ligne = 1
for loop in range(20):
   colonne = 1
   for loop in range(20):
      print(colonne * ligne, end = " ")
      colonne = colonne + 1
   print()
   ligne = ligne + 1
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
class Main {
   public static void main(String[] args) {
      int ligne = 1;
      for (int loop1 = 1; loop1 <= 20; loop1 = loop1 + 1) {
         int colonne = 1;
         for (int loop2 = 1; loop2 <= 20; loop2 = loop2 + 1) {
            System.out.print((colonne * ligne) + " ");
            colonne = colonne + 1;
         }
         System.out.println();
         ligne = ligne + 1;
      }
   }
}
```

</details>
