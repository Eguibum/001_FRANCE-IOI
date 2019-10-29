# Fiches d'inscription

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Pour chacune des personnes il faut lire le prénom et le nom puis les afficher à nouveau, en commençant par le nom puis le prénom. 

```

```

## Python

<details>
  <summary>Solution</summary>

```Python
nbPersonnes = int(input())
for loop in range(nbPersonnes):
   mots = input().split(" ")
   print("{} {}".format(mots[1], mots[0]))
```

Variante possible

```Python
nbPersonnes = int(input())
for loop in range(nbPersonnes):
   prenom, nom = input().split(" ")
   print("{} {}".format(nom, prenom))
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
      for (int personne = 0; personne < nbPersonnes; personne = personne + 1)
      {
         String prenom = entrée.next();
         String nom = entrée.next();
         System.out.println(nom+" "+prenom);
      }
   }
}
```

</details>
