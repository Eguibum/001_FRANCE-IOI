# Tarifs dégressifs

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Là, il y a de quoi faire chauffer les neurones. Il faut bien prendre en compte toutes les situations pour savoir quel prix afficher. Le tarif dépend de l'heure d'arrivée, mais il ne peut pas dépasser 53 pièces ! Il y a donc une condition à faire à partir du tarif calculé pour afficher le bon prix. Le prix de départ de la chambre est de 10 pièces, auquel tu rajoutes 5 pièces par heure après midi. Avec tout ça, tu peux faire ton calcul.

```
Je récupère l'heure d'arrivée
Je calcule dans une variable total le prix de la chambre + 5 * heure d'arrivée
Si total est supérieur à 53
  total prend la valeur 53
J'affiche total
```

## Python

<details>
  <summary>Solution</summary>

```Python
heure = int(input())
prix = 10 + 5 * heure
if prix > 53:
   prix = 53
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
class Main {
   static Scanner entrée = new Scanner(System.in);
   public static void main(String[] args) {
      int heure = entrée.nextInt();
      int prix = 10 + 5 * heure;
      if (prix > 53) {
         prix = 53;
      }
      System.out.println(prix);
   }
}
```

</details>
