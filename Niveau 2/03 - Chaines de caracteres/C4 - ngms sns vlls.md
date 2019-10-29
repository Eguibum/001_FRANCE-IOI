# Ngms sns vlles

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On a donc deux lignes de texte (le titre du livre et le nom de l’auteur) sur lesquelles il faut appliquer exactement le même traitement : on va donc répéter deux fois la même chose.
```
Répéter 2 fois
   Lire la ligne
   Traiter la ligne
```

Pour traiter la ligne, on va regarder ses caractères un par un et ne les afficher que s’il ne s’agit pas d’une espace et pas d’une voyelle. 

```
Pour Java, il est nécessaire d'utiliser une fonction. Comme nous ne les avons pas encore vu et que j'ai bien galéré sur un code hyper moche mais qui fonctionne, je me permets de la partager ici en tant que conseil : 

JAVA : 
final static String INDESIRABLES = "AEIOUY ";

Cette ligne est à placer juste après class Main et avant public static void main

Python :
def estVoyelle(car):
   voyelles = "AEIOUY"

Ces lignes sont à mettre au début du programme
```

## Python

<details>
  <summary>Solution 1 : sans fonction</summary>

```Python
for loop in range(2):
   ligne = input()
   for idLettre in range(len(ligne)):
      car = ligne[idLettre]
      if (car != " " and car != "A" and car != "E" and car != "I" and
          car != "O" and car != "U" and car != "Y"):
         print(car, end = "")
   print()
```

</details>

<details>
  <summary>Solution 2 : avec fonction</summary>

```Python
# Première version
# def estVoyelle2(car):
#    return car == "A" or car == "E" or car == "I" or car == "O" or  car == "U" or car == "Y"
   
# Seconde version
def estVoyelle(car):
   voyelles = "AEIOUY"
   for idLettre in range(6):
      if car == voyelles[idLettre]:
         return True
   return False
def main():
   for loop in range(2):
      ligne = input()
      for idCaractere in range(len(ligne)):
         car = ligne[idCaractere]
         if car != " " and not estVoyelle(car):
            print(car, end = "")
      print()
main()
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
   final static String INDESIRABLES = "AEIOUY ";
   public static void main(String[] args)
   {
      Scanner input= new Scanner(System.in);
      
      for (int iLigne = 0; iLigne < 2; iLigne++)
      {
         String ligne = input.nextLine();
         for (int iCar = 0; iCar < ligne.length(); iCar++)
         {
            char caractere = ligne.charAt(iCar);
            if ( !appartient(caractere, INDESIRABLES) )
               System.out.print(caractere);
         }
         System.out.println();
      }
   }
   
   static boolean appartient(char caractere,String ensemble)
   {
      for (int iCar = 0; iCar < ensemble.length(); iCar++)
         if (caractere == ensemble.charAt(iCar))
            return true;
      return false;
   }
}
```

</details>
