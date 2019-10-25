# Punition

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

C'est l'heure de l'initiation aux boucles ! Le but est de répéter plusieurs fois une même instruction sans se les tartiner à la main. Parce que bon, soyons honnêtes, entre répéter 5 fois et répéter 500 fois, c'est pas la même limonade !
Il est très important de comprendre l'indentation à partir d'ici. En effet, si le code est mal indenté, le résultat peut être totalement différent de ce à quoi tu t'attends.

```
Répéter 135 fois
  Je dois respecter le Grand Sorcier.
```

## Python

<details>
  <summary>Solution</summary>

```Python
for loop in range(135):
   print("Je dois respecter le Grand Sorcier.")
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
      for (int loop = 1; loop <= 135; loop = loop + 1) {
         System.out.println("Je dois respecter le Grand Sorcier.");
      }
   }
}
```

</details>
