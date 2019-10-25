# Mathématiques de base

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Ici il s'agit d'une simple correction. Lis bien le texte, relis les chapitres précédents sur les erreurs communes et tout devrait bien se passer.

```
 Il fallait corriger trois erreurs :

  il y avait plusieurs erreurs sur la ligne du for : un ; manquant et un < au lieu d'un <=,
  il manquait un guillemet autour du texte à afficher.

```

## Python

<details>
  <summary>Solution</summary>

```Python
for loop in range(13):
   print("9 * 8 = 72")
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
      for (int loop = 1; loop <= 13; loop = loop + 1) {
         System.out.println("9 * 8 = 72");
      }
   }
}
```

</details>
