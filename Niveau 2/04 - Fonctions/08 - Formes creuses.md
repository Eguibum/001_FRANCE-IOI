# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On crée une fonction par forme. Pour la ligne, on écrit une version de ligne pleine et une creuse, avec le motif au début et à la fin et des espaces entre les deux. On peut utiliser cette fonction pour créer les autres formes. 

```
Fonction ligne(longueur, motif)
   Répéter longueur fois
      Afficher motif (sans retour à la ligne)
   Aller à la ligne
Fonction ligneCreuse(longueur, motif)
   Si longueur > 1 alors
      Afficher motif (sans retour à la ligne)
      Répéter longueur - 2 fois
         Afficher " " (sans retour à la ligne)
   Afficher motif
   Aller à la ligne
Fonction rectangle(hauteur, largeur, motif)
   Si hauteur > 1 alors
      ligne(largeur, motif)
      Répéter hauteur - 2 fois
         ligneCreuse(largeur, motif)
   ligne(largeur, motif)
Fonction triangle(hauteur, motif)
   Pour iLigne allant de 1 à hauteur - 1 faire
      ligneCreuse(iLigne, motif)
   ligne(hauteur, motif)
longueurLigne <- lireEntier()
ligne(longueurLigne, "X")
Aller à la ligne
hauteurRectangle <- lireEntier()
largeurRectangle <- lireEntier()
rectangle(hauteurRectangle, largeurRectangle, "#")
Aller à la ligne
hauteurTriangle <- lireEntier()
triangle(hauteurTriangle, "@")
```

## Python

<details>
  <summary>Solution</summary>

```Python
def ligne(longueur, motif):
   for iCol in range(longueur):
      print(motif, end = "")
   print()
def ligneCreuse(longueur, motif):
   if longueur > 1:
      print(motif, end = "")
      for iEspace in range(longueur - 2):
         print(" ", end = "")
   print(motif)
def rectangle(hauteur, largeur, motif):
   if hauteur > 1:
      ligne(largeur, motif)
      for iLigne in range(hauteur - 2):
         ligneCreuse(largeur, motif)
   ligne(largeur, motif)
def triangle(hauteur, motif):
   for iLigne in range(1, hauteur):
      ligneCreuse(iLigne, motif)
   ligne(hauteur, motif)
longueurLigne = int(input())
ligne(longueurLigne, "X")
print()
hauteurRectangle = int(input())
largeurRectangle = int(input())
rectangle(hauteurRectangle, largeurRectangle, "#")
print()
hauteurTriangle = int(input())
triangle(hauteurTriangle, "@")
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
   static void ligne(int longueur, char motif) {
      for (int iCol = 1; iCol <= longueur; iCol = iCol + 1) {
         System.out.print(motif);
      }
      System.out.println();
   }
   static void ligneCreuse(int longueur, char motif) {
      if (longueur > 1) {
         System.out.print(motif);
         for (int iCol = 2; iCol < longueur; iCol = iCol + 1) {
            System.out.print(' ');
         }
      }
      System.out.println(motif);
   }
   static void rectangle(int hauteur, int longueur, char motif) {
      if (hauteur > 1) {
         ligne(longueur, motif);
         for (int iLigne = 2; iLigne < hauteur; iLigne = iLigne + 1) {
            ligneCreuse(longueur, motif);
         }
      }
      ligne(longueur, motif);
   }
   static void triangle(int hauteur, char motif) {
      for (int iLigne = 1; iLigne < hauteur; iLigne = iLigne + 1) {
         ligneCreuse(iLigne, motif);
      }
      ligne(hauteur, motif);
   }
   public static void main(String[] args) {
      int longueurLigne = entrée.nextInt();
      ligne(longueurLigne, 'X');
      System.out.println();
      int hauteurRectangle = entrée.nextInt();
      int largeurRectangle = entrée.nextInt();
      rectangle(hauteurRectangle, largeurRectangle, '#');
      System.out.println();
      int hauteurTriangle = entrée.nextInt();
      triangle(hauteurTriangle, '@');
   }
}
```

</details>
