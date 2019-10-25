# Planning de la journée

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Par rapport à ta position, il faut déterminer quels villages te sont accessibles dans un rayon de 50 kilomètres, quelque soit la direction. Tu es en borne X, si tu avances la borne augmente, si tu recules la borne diminue. Il faut donc calculer la différente entre ta borne et celle du village, si le résultat est négatif le passer en positif, et si ce positif est inférieur ou égal à 50, alors tu peux y accéder dans la journée.

```
Je récupère le numéro de ma borne
Je récupère le nombre de villages
J'initialise à 0 le nombre de villages accessibles
Je répète autant de fois qu'il y a de villages
  Je récupère la borne du village
  Je calcule ma borne - la borne du village
  Si le résultat est négatif
    Je le passe en positif
  Si le résultat est inférieur ou égal à 50
    Je rajoute +1 au nombre de villages accessibles
J'affiche le nombre de villages accessibles
```

## Python

<details>
  <summary>Solution</summary>

```Python
posActuelle = int(input())
nbVillages = int(input())
nbAccessibles = 0
for loop in range(nbVillages):
   posVillage = int(input())
   ecart = posActuelle - posVillage
   if ecart < 0:
      ecart = -ecart
   if ecart <= 50:
      nbAccessibles = nbAccessibles + 1
print(nbAccessibles) 
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
      int posActuelle = entrée.nextInt();
      int nbVillages = entrée.nextInt();
      int nbAccessibles = 0;
       
      for (int loop = 1; loop <= nbVillages; loop = loop + 1)
      {
         int posVillage = entrée.nextInt();
         int écart = posActuelle - posVillage;
         if(écart < 0)
         {
            écart = -écart;
         }
         if(écart <= 50)
         {
            nbAccessibles = nbAccessibles + 1;
         }
      }
      System.out.println(nbAccessibles);
   }
}
```

</details>
