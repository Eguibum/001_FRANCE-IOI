# Moyennes des notes

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On lit d'abord le nombre total de notes. Ensuite, on utilise une boucle dont le nombre d'exécutions dépend de ce nombre de notes. À chaque exécution de la boucle, on lit une nouvelle note et on l'ajoute à la somme en cours. Au début, la somme est égale à zéro. À la fin, on calcule la moyenne en divisant la somme des notes par le nombre de notes. 

```
nombreNotes <- LireEntier()
sommeNotes = 0
Répéter nombreNotes fois
   note <- LireEntier()
   sommeNotes = sommeNotes + note
Afficher (sommeNotes / nombreNotes)
```

## Python

<details>
  <summary>Solution</summary>

```Python
nombreNotes = int(input())
sommeNotes = 0
for loop in range(nombreNotes):
   note = int(input())
   sommeNotes = sommeNotes + note
print(sommeNotes / nombreNotes)
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
      int nombreNotes = entrée.nextInt();
      int sommeNotes = 0;
      for (int loop = 1; loop <= nombreNotes; loop = loop + 1)
      {
         int note = entrée.nextInt();
         sommeNotes = sommeNotes + note;
      }
      // Trans-typage explicite
      System.out.println((double)sommeNotes / (double)nombreNotes);
   }
}
```

</details>
