# Amitiés entre gardes

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Il y a énormément de possibilité d'intersections dans cet exercice, les énumérer tous seraient chronophages et très compliqué à maintenir à jour. Mais il y a des infos intéressants. On te dit que si, sur le planning, 2 gardes se sont vu ne serait-ce qu'une seconde, ils sont amis. Le plus simple est donc de regarder quand leur emploi du temps ne se chevauchent pas et ne se touchent même pas. Si c'est le cas, s'il n'y a aucun contact entre les deux, alros ils ne sont pas amis. Dans le cas contraire, ils sont amis.

```
Je récupère dateDébutGarde1
Je récupère dateFinGArde1
Je récupère dateDébutGarde2
Je récupère dateFinGarde2
Si dateFinGarde1 < dateDébutGarde2 OU si dateFinGarde2 < dateDébutGarde1
  J'affiche Pas amis
Sinon
  J'affiche Amis
```

## Python

<details>
  <summary>Solution</summary>

```Python
dateDebutPremier = int(input())
dateFinPremier = int(input())
dateDebutSecond = int(input())
dateFinSecond = int(input())
if (dateFinSecond < dateDebutPremier) or (dateFinPremier < dateDebutSecond):
   print("Pas amis")
else:
   print("Amis")
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
      int dateDébutPremier = entrée.nextInt();
      int dateFinPremier = entrée.nextInt();
      int dateDébutSecond = entrée.nextInt();
      int dateFinSecond = entrée.nextInt();
       
      if ( (dateFinSecond < dateDébutPremier) || (dateFinPremier < dateDébutSecond) )
      {
         System.out.println("Pas amis");
      }
      else
      {
         System.out.println("Amis");
      }
   }
}
```

</details>
