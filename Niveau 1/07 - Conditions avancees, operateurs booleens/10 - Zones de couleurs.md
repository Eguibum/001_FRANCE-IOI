# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 Il y a plusieurs manières d'exprimer les conditions. Celle que nous présentons fonctionne comme suit :

    Si le jeton est entièrement en dehors du rectangle, on affiche « En dehors de la feuille ».

    Un jeton est hors de la feuille si son x est inférieur à 0 ou supérieur à 90, ou bien si son y est inférieur à 0, ou supérieur à 70.

    Sinon, si le jeton est dans une zone rouge, on affiche « Dans une zone rouge ».

    Un jeton qui est dans la feuille est dans une zone rouge si son y est supérieur à 60, et que son x est soit entre 15 et 45, soit entre 60 et 85.

    Sinon, si le jeton est dans une zone bleue, on affiche « Dans une zone bleue ».

    Un jeton qui est dans la feuille est dans une zone bleue s'il est dans le rectangle tel que x est entre 10 et 85, et que y est entre 10 et 55, mais qu'il n'est pas dans le petit rectangle jaune tel que x est entre 25 et 50, et y est entre 20 et 45.

    Sinon, on affiche « Dans une zone jaune ».

    En effet, si le jeton n'est ni en dehors du rectangle, ni dans une zone rouge ou bleue, c'est qu'il est dans une zone jaune.


```
nbJetons <- lireEntier()
Répéter nbJetons fois
   x <- lireEntier()
   y <- lireEntier()
   Si x < 0 ou x > 90 ou y < 0 ou y > 70
      Afficher "En dehors de la feuille"
   Sinon, si y > 60 et ((x > 15 et x < 45) ou (x > 60 et x < 85))
      Afficher "Dans une zone rouge"
   Sinon, si x > 10 et x < 85 et y > 10 et y < 55 et pas (x > 25 et x < 50 et y > 20 et y < 45)
      Afficher "Dans une zone bleue"
   Sinon
      Afficher "Dans une zone jaune"
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbJetons = int(input())
for loop in range(nbJetons):
   x = int(input())
   y = int(input())
   if x < 0 or x > 90 or y < 0 or y > 70:
      print("En dehors de la feuille")
   elif y > 60 and ((x > 15 and x < 45) or (x > 60 and x < 85)):
      print("Dans une zone rouge")
   elif x > 10 and x < 85 and y > 10 and y < 55 and not(x > 25 and x < 50 and y > 20 and y < 45):
      print("Dans une zone bleue")
   else:
      print("Dans une zone jaune")
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
class Main {
   static Scanner entrée = new Scanner(System.in);
   public static void main(String[] args) {
      int nbPoints = entrée.nextInt();
      
      for (int loop = 1; loop <= nbPoints; loop = loop + 1) {
         int x = entrée.nextInt();
         int y = entrée.nextInt();
         if (x < 0 || x > 90 || y < 0 || y > 70) {
            System.out.println("En dehors de la feuille");
         } else if (y > 60 && ((x > 15 && x < 45) || (x > 60 && x < 85))) {
            System.out.println("Dans une zone rouge");
         } else if (x > 10 && x < 85 && y > 10 && y < 55 && !(x > 25 && x < 50 && y > 20 && y < 45)) {
            System.out.println("Dans une zone bleue");
         } else {
            System.out.println("Dans une zone jaune");
         }
      }
   }
}
```

</details>
