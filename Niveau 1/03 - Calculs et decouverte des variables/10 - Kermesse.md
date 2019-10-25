# Kermesse

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Il faut bien comprendre ici que le numéro de tir correspond au nombres de bonbons que tu gagnes. Au premier tir tu gagnes 1 bonbons, au deuxième tir, tu gagnes 2 bonbons, au troisième tir tu gagnes 3 bonbons, etc... Et ces bonbons s'ajoutent entre eux ! Donc au deuxième tir tu as 1 + 2 = 3 bonbons, au 3ème tir 3 + 3 = 6 et ainsi de suite...

```
Je définis nbBonbons à 0
Je définis nbTir à 1 (il n'y a pas de tir 0)
Je répète 50 fois
  Je calcule le nombre de bonbons en y rajoutant le numéro du tir à chaque boucle
  J'imprime le nombre de bonbons
  Je rajoute 1 au nombre de tir
```

## Python

<details>
  <summary>Solution</summary>

```Python
totalBonbons = 0
numTir = 1
for loop in range(50):
   totalBonbons = totalBonbons + numTir
   print(totalBonbons)
   numTir = numTir + 1
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
class Main {
   public static void main(String[] args) {
      int totalBonbons = 0;
      int numTir = 1;
      for (int loop = 1; loop <= 50; loop = loop + 1) {
         totalBonbons = totalBonbons + numTir;
         System.out.println(totalBonbons);
         numTir = numTir + 1;
      }
   }
}
```

</details>
