# Analyse d'une langue

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Il suffit de lire les lignes une par une, puis de comparer chacun de leurs caractères à la lettre dont on doit chercher le nombre d’apparitions. Dès qu’on trouve cette lettre dans le texte, on augmente de 1 le compteur nbFois dont on affichera la valeur à la fin. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
lettre = input()
nbLignes = int(input())
nbFois = 0
for loop in range(nbLignes):
   ligne = input()
   for idLettre in range(len(ligne)):
      if ligne[idLettre] == lettre:
         nbFois = nbFois + 1
print(nbFois)
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
      
      char cible = input.next().charAt(0);
      int nbLignes = input.nextInt();
      int compte = 0;
      for (int iLigne = 0; iLigne < nbLignes; iLigne = iLigne + 1)
      {
         String ligne = input.nextLine();
         for (int iLettre = 0; iLettre < ligne.length(); iLettre = iLettre + 1)
         {
            if (ligne.charAt(iLettre) == cible)
            {
               compte = compte + 1;
            }
         }
      }
      System.out.println(compte);
   }
}
```

</details>
