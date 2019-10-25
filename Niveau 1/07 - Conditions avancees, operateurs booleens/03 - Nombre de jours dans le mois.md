# Nombre de jours dans le mois

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Ici, plutôt que de faire une suite de if / else, il vaut mieux regrouper les conditions. On peut voir qu'un seul mois à 29 jours et que 4 mois ont 30 jours. Les autres mois ont tous 30 jours. On va donc aller de la condition la plus petite à la plus vaste.

```
Je récupère mois
Si mois == 1
  J'affiche 29
sinon 
  si mois >= 4 ET mois <=6 OU mois == 10
    J'affiche 31
  sinon
    J'affiche 30
```

## Python

<details>
  <summary>Solution</summary>

```Python
numero = int(input())
if numero == 11:
   print(29)
else:
   if ( (4 <= numero) and (numero <= 6) ) or (numero == 10):
      print(31)
   else:
      print(30)
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
      int numéro = entrée.nextInt();
       
      if(numéro == 11)
      {
         System.out.println("29");
      }
      else
      {
         if( ( (4 <= numéro) && (numéro <= 6) ) || (numéro == 10) )
         {
            System.out.println("31");
         }
         else
         {
            System.out.println("30");
         }
      }
   }
}
```

</details>
