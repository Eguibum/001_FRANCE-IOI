# Convertisseurs d'unités

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Pour commencer, on définit les constantes correspondant aux valeurs du sujet (montré en C et C++). On utilise ensuite ces constantes pour créer trois fonctions de conversion : une pour chaque unité de départ. Nous faisons appel dans ce programme à l'instruction « selon », proposée sous le nom switch dans certains langages.

```
PIED_EN_MÈTRES = 0.3048
GRAMME_EN_LIVRES = 0.002205
   
Fonction celsiusVersFarenheit(celsius)
   Retourner 32 + celsius * 1.8
nbValeurs <- lireEntier()
Répéter nbValeurs fois
   valeur <- lireFlottant()
   unité <- lireCaractère()
   Selon unité
      Cas 'm'
         Afficher valeur / PIED_EN_MÈTRES, 'p'
      Cas 'g'
         Afficher valeur * GRAMME_EN_LIVRES, 'l'
      Cas 'c'
         Afficher celsiusVersFarenheit(valeur), 'f'
```

## Python

<details>
  <summary>Solution avec fonction</summary>

```Python
def mètresVersPieds(mètres):
   return mètres / .3048
def grammesVersLivres(grammes):
   return grammes * .002205
def celsiusVersFarenheit(celsius):
   return 32 + celsius * 1.8
nbValeurs = int(input())
for loop in range(nbValeurs):
   valeur, unité = input().split()
   valeur = float(valeur)
   if unité == 'm':
      print(mètresVersPieds(valeur), 'p')
   elif unité == 'g':
      print(grammesVersLivres(valeur), 'l')
   elif unité == 'c':
      print(celsiusVersFarenheit(valeur), 'f')
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
  <summary>Solution avec fonction</summary>


```Java
import algorea.Scanner;
class Main {
   static Scanner entrée = new Scanner(System.in);
   static double mètresVersPieds(double mètres) {
      return mètres / .3048;
   }
   static double grammesVersLivres(double grammes) {
      return grammes * .002205;
   }
   static double celsiusVersFarenheit(double celsius) {
      return celsius * 1.8 + 32;
   }
   public static void main(String[] args) {
      int nbValeurs = entrée.nextInt();
      for (int loop = 0; loop < nbValeurs; loop++) {
         double valeur = entrée.nextDouble();
         char unité = entrée.next().charAt(0);
         switch (unité) {
            case 'm':
               System.out.println(mètresVersPieds(valeur) + " p");
               break;
            case 'g':
               System.out.println(grammesVersLivres(valeur) + " l");
               break;
            case 'c':
               System.out.println(celsiusVersFarenheit(valeur) + " f");
               break;
         }
      }
   }
}
```

</details>

<details>
  <summary>Solution sans fonction - c'est la mienne, pas celle de IOI</summary>


```Java
import algorea.Scanner;

class Main {

   static Scanner input = new Scanner(System.in);
   
   static double footInMeter = 0.3048;
   static double poundInGramme = 0.002205;
   
   public static void main(String[] args) {
   
      int nbConversions = input.nextInt();
      
      for (int iConversion = 0; iConversion < nbConversions; iConversion++) {
         double toDoConversion = input.nextDouble();
         char unitéConversion = input.next().charAt(0);
         double conversion = 0;
         
         if (unitéConversion == 'm') {
         conversion = toDoConversion / footInMeter;
            System.out.println(conversion + " p");
         } else if (unitéConversion == 'g') {
         conversion = toDoConversion * poundInGramme ;
            System.out.println(conversion + " l");
         } else if (unitéConversion == 'c'){
         conversion = (toDoConversion * 9/5) + 32;
            System.out.println(conversion + " f");
         }
      } 
   }
}
```

</details>
