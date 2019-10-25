# Bornes kilométriques

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Tu récupères 2 numéros de bornes et tu dois calculer la différence entre les 2. Le piège, c'est qu'il ne peut pas y avoir de résultat négatif ou nul, or tu ne sais pas dans quel ordre vont être données ces valeurs. L'astuce, quand un résultat est négatif, c'est d'afficher son contraire en rajoutant le symbole - devant. En effet, comme en maths, - et - = +.

```
Je récupère ma valeur 1
Je récupère ma valeur 2
Je calcule écart = valeur 1 - valeur 2
Si écart est inférieur à 0
  je passe sa valeur en positif écart = - écart
J'affiche écart
```

## Python

<details>
  <summary>Solution</summary>

```Python
numéroMatin = int(input())
numéroSoir = int(input())
écart = numéroSoir - numéroMatin
if écart < 0:
   écart = -écart
print(écart)
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
      int numéroMatin = entrée.nextInt();
      int numéroSoir = entrée.nextInt();
      int écart = numéroSoir - numéroMatin;
      if (écart < 0) {
         écart = -écart;
      }
      System.out.println(écart);
   }
}
```

</details>
