# Augmentation des taxes

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

 On utilisera les abréviations HT (prix Hors-Taxe) et TTC (prix Toutes-Taxes-Comprises) pour désigner les prix avant et après l'application de la taxe.

On va commencer par calculer le nouveau prix du produit sans s'occuper d'arrondir au centime près. Pour calculer ce nouveau prix on cherche à déterminer le prix hors-taxe. On sait que

ancienPrixTTC=prixHT×(1+ancienneTaxe100)

et on en déduit que

prixHT=ancienPrixTTC(1+ancienneTaxe100)

Il faut maintenant appliquer la nouvelle taxe, on a donc au final :

nouveauPrixTTC=ancienPrixTTC(1+ancienneTaxe100)×(1+nouvelleTaxe100)

Une fois qu'on connait ce prix, il faut donc calculer le bon arrondi, en utilisant la fonction d'arrondi "au plus proche" (ce nom dépend du langage que vous utilisez). Cependant cette fontion permet uniquement d'arrondir à l'entier le plus proche et ici nous avons besoin d'un arrondi au centime le plus proche. On va donc calculer l'arrondi sur les centimes et pour cela on multiplie le prix du légume par cent (ce qui donne bien un prix en centimes), puis on calcule l'arrondi et enfin on calcule à nouveau un prix en écus, en divisant par 100 le prix en centimes. 

```
taxeActuelle <- LireDecimal()
taxeFuture <- LireDecimal()
prixLegume <- LireDecimal()

nouveauPrix <- prixLegume / ( 1 + taxeActuelle / 100) * (1 + taxeFuture / 100)
nouveauPrix <- ArrondiPlusProche(nouveauPrix * 100) / 100
Afficher nouveauPrix
```

## Python

<details>
  <summary>Solution</summary>

```Python
from math import *
 
taxeActuelle = float(input())
taxeFuture = float(input())
prixLegume = float(input())

nouveauPrix = prixLegume / ( 1 + taxeActuelle / 100) * (1 + taxeFuture / 100)
nouveauPrix = round(nouveauPrix * 100) / 100
print(nouveauPrix)
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
      double taxeActuelle = entrée.nextDouble();
      double taxeFuture = entrée.nextDouble();
      double prixLégume = entrée.nextDouble();
       
      double nouveauPrix =
         prixLégume / ( 1 + taxeActuelle / 100) * (1 + taxeFuture / 100);
      nouveauPrix = (double)round(nouveauPrix * 100) / 100;
      System.out.println(nouveauPrix);
   }
}
```

</details>
