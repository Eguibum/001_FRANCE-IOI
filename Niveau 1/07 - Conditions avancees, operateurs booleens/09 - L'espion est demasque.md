# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On commence par lire chacune des caractéristiques de la personne et à chaque fois on teste si la personne remplit le critère associé. On utilise une variable nbCriteres pour compter le nombre de critères remplis par la personne. Enfin, selon le nombre de critères vérifiés, on affiche le bon texte. 

```
nbPersonnes <- LireEntier()
Répéter nbPersonnes fois
   nbCriteres <- 0
   taille <- LireEntier()
   Si 178 <= taille et taille <= 182
      nbCriteres <- nbCriteres + 1
   age <- LireEntier()
   Si age >= 34
      nbCriteres <- nbCriteres + 1
   poids <- LireEntier()
   Si poids < 70
      nbCriteres <- nbCriteres + 1
   aCheval <- LireEntier()
   Si aCheval = 0
      nbCriteres <- nbCriteres + 1
   aLesCheveuxBruns <- LireEntier()
   Si aLesCheveuxBruns = 1
      nbCriteres <- nbCriteres + 1
   
   Si nbCriteres = 0
      Afficher "Impossible"
   SinonSi nbCriteres = 5
      Afficher "Très probable"
   SinonSi nbCriteres >= 3
      Afficher "Probable"
   Sinon
      Afficher "Peu probable"
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbPersonnes = int(input())
for loop in range(nbPersonnes):
   nbCriteres = 0
   taille = int(input())
   if (178 <= taille) and (taille <= 182):
      nbCriteres = nbCriteres + 1
   age = int(input())
   if age >= 34:
      nbCriteres = nbCriteres + 1
   poids = int(input())
   if poids < 70:
      nbCriteres = nbCriteres + 1
   aCheval = int(input())
   if aCheval == 0:
      nbCriteres = nbCriteres + 1
   aLesCheveuxBruns = int(input())
   if aLesCheveuxBruns == 1:
      nbCriteres = nbCriteres + 1
   
   if nbCriteres == 0:
      print("Impossible")
   elif nbCriteres == 5:
      print("Très probable")
   elif nbCriteres >= 3:
      print("Probable")
   else:
      print("Peu probable")
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
      int nbPersonnes = entrée.nextInt();
    
      for (int loop = 1; loop <= nbPersonnes; loop = loop + 1)
      {
         int taille = entrée.nextInt();
         int âge = entrée.nextInt();
         int poids = entrée.nextInt();
         int aCheval = entrée.nextInt();
         int aLesCheveuxBruns = entrée.nextInt();
         
         int nbCritères = 0;
         if((178 <= taille) && (taille <= 182))
         {
            nbCritères = nbCritères+ 1;
         }
         if(âge >= 34)
         {
            nbCritères = nbCritères+ 1;
         }
         if(poids < 70)
         {
            nbCritères = nbCritères+ 1;
         }
         if(aCheval == 0)
         {
            nbCritères = nbCritères+ 1;
         }
         if(aLesCheveuxBruns == 1)
         {
            nbCritères = nbCritères+ 1;
         }
           
         if(nbCritères == 0)
         {
            System.out.println("Impossible");
         }
         else if(nbCritères == 5)
         {
            System.out.println("Très probable");
         }
         else if(nbCritères >= 3)
         {
            System.out.println("Probable");
         }
         else
         {
            System.out.println("Peu probable");
         }
      }
   }
}
```

</details>
