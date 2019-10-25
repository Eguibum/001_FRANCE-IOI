# Espion étranger

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Tu as une plage horaire dateMin et dateMax. Pour un nombre nbEntrées, tu dois vérifier si leur date est dans la plage horaire que l'on va te donner. Si c'est vrai, alors le nbPersonnes augmente de 1. Et tu affiches le nombre de personnes suspects.

```
Je récupère dateMin
Je récupère dateMax
Je récupère nbEntrées
J'initialise nbPersonnes à 0
Je répète autant de fois qu'il y a nbEntrées
  Je récupère date
  Si dateMin <= date et date <= date fin
    J'augmente nbPersonnes de 1
J'affiche nbPersonnes
```

## Python

<details>
  <summary>Solution</summary>

```Python
dateDébut = int(input())
dateFin = int(input())
nbEntrées = int(input())
nbPersonnes = 0
for loop in range(nbEntrées):
   date = int(input())
   if dateDébut <= date and date <= dateFin:
      nbPersonnes = nbPersonnes + 1
print(nbPersonnes)
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
      int dateDébut = entrée.nextInt();
      int dateFin = entrée.nextInt();
      int nbEntrées = entrée.nextInt();
      int nbPersonnes = 0;
      for (int loop = 1; loop <= nbEntrées; loop = loop + 1)
      {
         int date = entrée.nextInt();
         if( (dateDébut <= date) && (date <= dateFin) )
         {
            nbPersonnes = nbPersonnes + 1;
         }
      }
      System.out.println(nbPersonnes);
   }
}
```

</details>
