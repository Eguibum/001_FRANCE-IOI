# Analyse de fréquence

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 Il est nécessaire de compter le nombre de mots ayant 1 lettre, 2 lettres… 100 lettres. Il faut donc utiliser un tableau, car on ne va pas utiliser 100 variables différentes.

Une fois le tableau initialisé avec uniquement des zéros, il faut lire l’ensemble du texte ligne à ligne et/ou mot à mot, selon le langage utilisé. Ensuite, on va calculer la longueur de chaque mot lu, puis mettre à jour la valeur dans l’histogramme.

À la fin, il faut analyser l’histogramme et dès qu’on trouve une valeur différente de zéro (c’est-à-dire qu’il y avait au moins un mot de cette longueur dans le texte), alors on affiche la longueur, puis le nombre de mots de cette longueur, selon le format donné dans l’énoncé. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
nbLignes, nbMots = map(int, input().split(" "))
histogramme = [0] * 101
for loop in range(nbLignes):
   mots = input().split(" ")
   for idMot in range(nbMots):
      longueur = len(mots[idMot])
      histogramme[longueur] = histogramme[longueur] + 1
for longueur in range(101):
   if histogramme[longueur] > 0:
      print("{} : {}".format(longueur, histogramme[longueur]))
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
   public static void main(String [] args)
   {
      Scanner input = new Scanner(System.in);
      
      int nbLignes = input.nextInt();
      int nbMots = input.nextInt();
      int[] histogramme = new int[101];
      for (int iLigne = 0; iLigne < nbLignes; iLigne = iLigne + 1)
      {
         for (int iMot = 0; iMot < nbMots; iMot = iMot + 1)
         {
            String mot = input.next();
            int nbCar = mot.length();
            histogramme[nbCar] = histogramme[nbCar] + 1;
         }
      }
      for (int nbCar = 1; nbCar <= 100; nbCar = nbCar + 1)
      {
         if (histogramme[nbCar] > 0)
         {
            System.out.println(nbCar + " : " + histogramme[nbCar]);
         }
      }
   }
}
```

</details>
