# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On utilise une boucle pour lire chaque ligne de texte, l’une après l’autre. Pour chaque ligne, il faut alors afficher les caractères en partant de la fin. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
nbLignes = int(input())
for loop in range(nbLignes):
   ligneTexte = input()
   longueur = len(ligneTexte)
   for idCaractere in range(longueur):
      print(ligneTexte [longueur - 1 - idCaractere], end = "")
   print()
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
      for (int iLigne = 0; iLigne < nbLignes; iLigne = iLigne + 1)
      {
         String ligne = input.nextLine();
         for (int iCar = ligne.length() - 1; iCar >= 0; iCar = iCar - 1)
         {
            System.out.print(ligne.charAt(iCar));
         }
         System.out.println("");
      }
   }
}
```

</details>
