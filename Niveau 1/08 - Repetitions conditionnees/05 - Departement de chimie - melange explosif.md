# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On va utiliser une boucle « tant que » pour traiter les mesures de températures. C'est la condition de cette boucle qui est le point difficile : il faut à la fois que le numéro de la température qu'on mesure ne soit pas plus grand que le nombre total de températures à mesurer, mais aussi que la température soit dans le bon intervalle de valeurs. Dans la boucle, on va lire la mesure de température, et on doit donc afficher le commentaire correspondant. Notez alors que l'on a écrit deux fois le test pour vérifier qu'une température est valide. Aussi, on devra initialiser la variable température avant la boucle pour pouvoir la tester.  On utilise la valeur de tempMin pour être sûr de bien rentrer dans la boucle. À la place, on va plutôt se servir d'un booléen tempValide pour stocker le résultat du test lorsqu'une température est reçue. 

```
nbMesures <- lireEntier()
tempMin <- lireEntier()
tempMax <- lireEntier()
numMesure <- 1
tempValide <- Vrai
Tant que numMesure <= nbMesures et tempValide
   température <- lireEntier()
   tempValide <- (tempMin <= température et température <= tempMax)
   Si tempValide
      Afficher "Rien à signaler"
   Sinon
      Afficher "Alerte !!"
   numMesure <- numMesure + 1
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbMesures = int(input())
tempMin = int(input())
tempMax = int(input())
numMesure = 0
tempValide = True
while numMesure < nbMesures and tempValide:
   température = int(input())
   tempValide = (tempMin <= température and température <= tempMax)
   if tempValide:
      print("Rien à signaler")
   else:
      print("Alerte !!")
   numMesure = numMesure + 1
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
      int nbMesures = entrée.nextInt();
      int tempMin = entrée.nextInt();
      int tempMax = entrée.nextInt();
      int numMesure = 0;
      boolean tempValide = true;
      while (numMesure < nbMesures && tempValide)
      {
         int température = entrée.nextInt();
         tempValide = (tempMin <= température && température <= tempMax);
         if (tempValide) {
            System.out.println("Rien à signaler");
         }
         else {
            System.out.println("Alerte !!");
         }
         numMesure = numMesure + 1;
      }
   }
}
```

</details>
