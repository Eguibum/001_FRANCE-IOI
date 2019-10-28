# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Il s'agit de compter combien d'intervalles parmi ceux des invités intersectent la période de présence estimée de l'espion. Vous savez que pour tester une intersection d'intervalle il est plus court de tester qu'ils ne s'intersectent pas mais ici on ne veut faire quelque chose que s'ils s'intersectent ! C'est une bonne occasion d'utiliser l'opérateur "non". 

```
Je récupère espionDébut
Je récupère espionFin
Je récupère nbInvités
J'initialise nbSuspects à 0
Je répète autant de fois qu'il y a d'invités
  Je récupère invitéDébut
  Je récupère invitéFin
  Si espionFin n'est pas inférieur à invitéDébut ou invitéFin n'est pas inférieur à espionDébut
    Alors je rajoute 1 à nbSuspects
J'affiche nbSuspects
```

## Python

<details>
  <summary>Solution</summary>

```Python
espionDebut = int(input())
espionFin = int(input())
nbInvites = int(input())
nbSuspects = 0
for loop in range(nbInvites):
   debut = int(input())
   fin = int(input())
   if not( (espionFin < debut) or (fin < espionDebut) ):
      nbSuspects = nbSuspects + 1
print(nbSuspects)
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
      int espionDébut = entrée.nextInt();
      int espionFin = entrée.nextInt();
      int nbInvités = entrée.nextInt();
       
      int nbSuspects = 0;
      for (int loop = 1; loop <= nbInvités; loop = loop + 1)
      {
         int début = entrée.nextInt();
         int fin = entrée.nextInt();
         if( !( (espionFin < début) || (fin < espionDébut) ) )
         {
            nbSuspects = nbSuspects + 1;
         }
      }
      System.out.println(nbSuspects);
   }
}
```

</details>
