# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Ici, il faut tester si une valeur est présente dans une liste que l'on va nous donner. Donc il faut comparer la valeur recherchée avec les valeurs qu'on nous donne, et vérifier si elles sont "vraie" ou "fausse". Il faut donc initialiser une variable à false "Faux" et la passer à true "Vrai" quand le chiffre recherché nous est donné.

```
Je récupère le numéro de la personne recherchée
Je récupère la taille de la liste
J'initialise ma variable estSorti à false
Je répète autant de fois que la taille de la liste
  Je récupère le numéro d'un habitant
  Si ce numéro est égal au numéro recherché
    Alors estSorti passe à true
Si estSorti est true
  Alors j'affiche Sorti de la ville
Sinon
  J'affiche Encore dans la ville
```

## Python

<details>
  <summary>Solution</summary>

```Python
numeroPersonne = int(input())
tailleListe = int(input())
estSorti  = False
for loop in range(tailleListe):
   numero = int(input())
   if numero == numeroPersonne:
      estSorti = True
if estSorti:
   print("Sorti de la ville")
else:
   print("Encore dans la ville")
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
      int numéroPersonne = entrée.nextInt();
      int tailleListe = entrée.nextInt();
      boolean estSorti = false;
      
      for (int loop = 1; loop <= tailleListe; loop = loop + 1)
      {
         int numéro = entrée.nextInt();
         if(numéro == numéroPersonne)
         {
            estSorti = true;
         }
      }
       
      if(estSorti)
      {
         System.out.println("Sorti de la ville");
      }
      else
      {
         System.out.println("Encore dans la ville");
      }
   }
}
```

</details>
