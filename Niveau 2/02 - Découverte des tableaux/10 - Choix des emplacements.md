# Choix des emplacements

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Dans l'entrée, on nous fournit pour chaque emplacement le numéro du marchand qui s'y trouve. On pourrait donc créer le tableau suivant :
```Pour iEmp de 0 à nbEmplacements - 1
   marchands[iEmp] <- lireEntier()```

Or, ce qu'on nous demande au contraire, c'est d'afficher la liste des emplacements correspondant à chaque marchand dans l'ordre de leurs numéros, ou plus simplement d'indiquer pour chaque marchand son emplacement. Il faut donc « inverser » les données ! Au lieu d'un tableau qui met les marchands à leur emplacement, on crée un tableau dans lequel on va mettre les emplacements au numéro du marchand qui le possède. On peut découper la lecture et la mise à jour du tableau (ce qui permet de nommer la valeur) :
```iMarchand <- lireEntier()
   emplMarchands[iMarchand] <- iEmp```

Dans certains langages, on n'a d'ailleurs pas d'autre choix. Remarquez que dans un sens, on nomme le tableau marchands, donc uniquement en fonction du rôle des valeurs contenues, et dans l'autre sens, on le nomme emplMarchands (raccourci pour « emplacements des marchands »), donc en combinant le contenu et le rôle des indices. Nous estimons ainsi que les emplacements sont des éléments que l'on se représentera plus intuitivement sous une forme numérique et ordonnée, et donc qu'en nommant notre tableau simplement marchands, on comprend à partir de l'énoncé du problème que les cases correspondent aux emplacements, et les valeurs aux marchands. Nous vous invitons à juger par vous-même. 

```
nbEmplacements <- lireEntier()
emplMarchands <- tableau de nbEmplacements entiers initialisés à 0
Pour iEmp allant de 0 à nbEmplacements - 1
   emplMarchands[lireEntier()] <- iEmp
Pour iMarchand allant de 0 à nbEmplacements - 1
   Afficher emplMarchands[iMarchand]
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbEmplacements = int(input())
emplMarchands = [0] * nbEmplacements
for iEmp in range(nbEmplacements):
   emplMarchands[int(input())] = iEmp
for iMarchand in range(nbEmplacements):
   print(emplMarchands[iMarchand])
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
      int nbEmplacements = entrée.nextInt();
      int[] emplMarchands = new int[nbEmplacements];
      for (int iEmp = 0; iEmp < nbEmplacements; iEmp = iEmp + 1) {
         emplMarchands[entrée.nextInt()] = iEmp;
      }
      for (int iMarchand = 0; iMarchand < nbEmplacements; iMarchand = iMarchand + 1) {
         System.out.println(emplMarchands[iMarchand]);
      }
   }
}
```

</details>
