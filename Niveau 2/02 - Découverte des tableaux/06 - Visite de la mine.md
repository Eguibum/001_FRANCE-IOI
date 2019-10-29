# Visite de la mine

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 Dans le principe, on commence par lire tous les déplacements faits puis il faut les afficher, en partant de la fin, en inversant à chaque fois les déplacements. On pourrait donc avoir un code du type
```
Si deplacement = 1
   deplacement <- 2
SinonSi deplacement = 2
   deplacement  <- 1
SinonSi deplacement = 4
   deplacement <- 5
SinonSi deplacement = 5
   deplacement <- 4
```

C'est cependant assez répétitif et on sent qu'il est possible de faire mieux. On peut en effet utiliser un tableau qui nous donnera, pour chaque déplacement, le déplacement inverse :

```
deplacementInverse <- [0, 2, 1, 3, 5, 4]
deplacement <- deplacementInverse[deplacement]
```

Cette technique est très courante et permet d'avoir des codes plus courts. Vous aurez l'occasion de la réutiliser à de nombreuses occasions.

On notera que si un tableau a `nbDeplacements` éléments, alors son dernier élément a pour indice `nbDeplacements` - 1.

```
deplacementInverse <- [0, 2, 1, 3, 5, 4]
nbDeplacements <- LireEntier()
chemin <- Tableau de taille nbDeplacements contenant des 0
Pour numero allant de 0 à nbDeplacements-1
   chemin[numero] <- LireEntier()
Pour numero allant de nbDeplacements-1 à 0
   deplacement <- chemin[numero]
   Afficher deplacementInverse[deplacement]
```

## Python

<details>
  <summary>Solution</summary>

```Python
deplacementInverse = [0, 2, 1, 3, 5, 4]
nbDeplacements = int(input())
chemin = [0] * nbDeplacements
for numero in range(nbDeplacements):
   chemin[numero] = int(input())
for numero in range(nbDeplacements-1, -1, -1):
   deplacement = chemin[numero]
   print(deplacementInverse[deplacement])
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
      int[] deplacementInverse = {0, 2, 1, 3, 5, 4};
 
      int nbDeplacements = entrée.nextInt();
      int[] chemin = new int[nbDeplacements];
       
      for (int numero = 0; numero < nbDeplacements; numero = numero + 1)
      {
         chemin[numero] = entrée.nextInt();
      }
       
      for (int numero = nbDeplacements-1; numero >= 0; numero = numero - 1)
      {
         int deplacement = chemin[numero];
         System.out.println(deplacementInverse[deplacement]);
      }
   }
}
```

</details>
