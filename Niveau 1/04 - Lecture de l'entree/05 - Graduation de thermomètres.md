# Graduation de thermomètres

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Tu dois afficher des valeurs les unes après les autres, mais pas depuis zéro. Tu sais faire, ça serait trop facile. Ici tu dois donc récupérer la valeur min et la valeur max et imprimer tes valeurs à partir de la valeur min et donc jusqu'à la valeur max.

```
Je récupère la tempMin
Je récupère la tempMax
Je définis ma température de départ identique à tempMin
Je répète autant de fois que vaut tempMax - tempMin + 1
  j'affiche température
  je rajoute + 1 à température

Je calcule tempMax - tempMin + 1 pour avoir le bon nombre de répétition et donc de valeurs affichées

Si je reprends l'exemple du sujet :
tempMin = 9 ; tempMAx = 14
9 10 11 12 13 14 <= il y a 6 valeurs
14 - 9 = 5 <= il manque 1 valeur, d'où le + 1
```

## Python

<details>
  <summary>Solution</summary>

```Python
tempMin = int(input())
tempMax = int(input())
temperature = tempMin
for loop in range(tempMax - tempMin + 1):
   print(temperature)
   temperature = temperature + 1
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
      int tempMin = entrée.nextInt();
      int tempMax = entrée.nextInt();
      int température = tempMin;
      for (int loop = 1; loop <= tempMax - tempMin + 1; loop = loop + 1) {
         System.out.println(température);
         température = température + 1;
      }
   }
}
```

</details>
