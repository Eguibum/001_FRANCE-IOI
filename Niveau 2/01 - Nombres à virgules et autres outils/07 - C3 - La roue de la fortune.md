# La roue de la fortune

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 On utilise simplement l'opérateur modulo afin de déterminer dans quelle zone on arrive.

La difficulté est que l'opérateur modulo ne donne pas toujours un résultat positif : si on l'utilise avec un nombre négatif on peut avoir un résultat compris entre -23 et 0. On pourrait donc faire ainsi :
```
nbZones <- LireEntier()
numero <- Reste(nbZones, 24)
Si numero < 0
   numero <- numero + 24
Afficher numero
```

On utilise en général une écriture plus courte, sans test :
```
numero <- Reste(nbZones, 24)
numero <- Reste(numero + 24, 24)
```

Ainsi, on utilise un premier modulo pour avoir un nombre dans l'intervalle [-23;23] puis on ajoute 24, ce qui nous amène dans l'intervalle [1;47] puis un dernier modulo nous amène dans [0;23], ce qu'on voulait !

C'est une "astuce" à retenir, dès que vous avez à calculer des modulo avec des nombres qui peuvent être négatifs. 

```
nbZones <- LireEntier()
Afficher Reste(nbZones, 24)
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbZones = int(input())
print(nbZones % 24)
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
      int nbZones = entrée.nextInt();
      System.out.println(((nbZones % 24) + 24 ) % 24);
   }
}
```

</details>
