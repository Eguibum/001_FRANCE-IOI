# Cour de récréation

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Toutes les instructions sont données dans l'exercice, il suffit de connaître la formule du périmètre et de l'aire.

```
Je calcule la longueur d'un côté de la cours que je stocke dans une variable
Je calcule et j'imprime l'aire longueur * longueur
Je calcule et j'imprime le périmètre longueur * 4
```

## Python

<details>
  <summary>Solution</summary>

```Python
longueur = 17 * 5 + 7 * 2 + 5 * 1 + 2 * 2
print(longueur * longueur)
print(longueur * 4)
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
      int longueur;
      longueur = 17 * 5 + 7 * 2 + 5 * 1 + 2 * 2;
      System.out.println(longueur * longueur);
      System.out.println(4 * longueur);
   }
}
```

</details>
