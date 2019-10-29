# Inscription d'étudiants

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On commence par lire le nom complet, puis on regarde si le premier caractère du nom est inférieur ou égal au caractère "F". Si oui alors c’est la première personne, sinon on compare ce caractère à la lettre "P", pour déterminer si c’est la seconde ou la troisième personne. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
nom = input()
if nom[0] <= "F":
   print(1)
elif nom[0] <= "P":
   print(2)
else:
   print(3)
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
      String nom = entrée.next();
      char premier = nom.charAt(0);
      
      if (premier < 'G')
      {
         System.out.println(1);
      }
      else if (premier > 'P')
      {
         System.out.println(3);
      }
      else
      {
         System.out.println(2);
      }
   }
}
```

</details>
