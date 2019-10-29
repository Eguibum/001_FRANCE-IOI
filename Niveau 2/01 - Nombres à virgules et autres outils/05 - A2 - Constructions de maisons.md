# Construction de maisons

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 On commence par calculer le nombre de sacs qu'il faudra acheter en divisant la quantité de ciment par 60 : cela nous donne un nombre de sacs sous la forme d'un nombre décimal et on arrondi alors cette valeur à l'entier supérieur pour connaitre le nombre de sacs.

Une fois le nombre de sacs connu, il suffit de mutiplier cette valeur par le prix d'un sac pour connaitre le coût total du ciment. 

```
quantiteCiment <- LireDecimal()
nbSacs <- ArrondiSuperieur(quantiteCiment / 60)
prix <- nbSacs * 45
Afficher prix
```

## Python

<details>
  <summary>Solution</summary>

```Python
from math import *
 
quantiteCiment = float(input())
nbSacs = ceil(quantiteCiment / 60)
prix = nbSacs * 45
print(prix)
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
import static java.lang.Math.*;
class Main
{
   public static void main(String[] args)
   {
      Scanner entrée = new Scanner(System.in);
      double quantitéCiment = entrée.nextDouble();
      int nbSacs = (int)ceil(quantitéCiment / 60);
      int prix = nbSacs * 45;
      System.out.println(prix);
   }
}
```

</details>
