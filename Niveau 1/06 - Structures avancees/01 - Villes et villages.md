# Villes et villages

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Il faut définir si les lieux que tu visites sont des villes ou des villages, par rapport au nombre d'habitants. Il faut ensuite afficher le nombre de villes uniquement. Boucles et conditions seront de la partie.

```
Je récupère le nombre de lieux
J'initialise le nombre de villes à 0
Je répète autant de fois qu'il y a de lieux
  Je récupère la population du lieux
  Si la population est supérieur à 10 000 habitants
    J'incrémente de 1 le nombre de villes
J'affiche le nombre de villes
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbLieux = int(input())
nbVilles = 0
for loop in range(nbLieux):
   population = int(input())
   if population > 10 * 1000:
      nbVilles = nbVilles + 1
print(nbVilles)
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
      int nbLieux = entrée.nextInt();
      int nbVilles = 0;
      for (int loop = 1; loop <= nbLieux; loop = loop + 1)
      {
         int population = entrée.nextInt();
         if (population > 10 * 1000)
         {
            nbVilles = nbVilles + 1;
         }
      }
      System.out.println(nbVilles);
   }
}
```

</details>
