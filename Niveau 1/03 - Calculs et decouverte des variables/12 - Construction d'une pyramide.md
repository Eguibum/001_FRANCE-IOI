# Construction d'une pyramide

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Ici il faut partir du sommet, et non de la base. En effet, on ne sait pas si on aura assez de petits cubes. Chaque niveau s'élargit de 2 par rapport au nireau précédent, cela nous donne une indication sur l'incrémentation à faire. On sait qu'ils envisagent de construire une base de 17 (donc impair), et qu'il y a 9 impairs entre 1 et 17. On a notre nombre de boucles !

```
Je définis mon nbCubes à 0
Je définis largeurArrête de mon niveau à 1
Je répète 9 fois
  je calcule nbCubes en lui rajoutant la somme du volume de largeurArrête
  je rajoute 2 a largeurArrête
J'affiche nbCubes 
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbCubes = 0
largeurArête = 1
for loop in range(9):
   nbCubes = nbCubes + largeurArête * largeurArête * largeurArête
   largeurArête = largeurArête + 2
print(nbCubes)
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
      int nbCubes = 0;
      int largeurArête = 1;
      for (int loop = 1; loop <= 9; loop = loop + 1) {
         nbCubes = nbCubes + largeurArête * largeurArête * largeurArête;
         largeurArête = largeurArête + 2;
      }
      System.out.println(nbCubes);
   }
}
```

</details>
