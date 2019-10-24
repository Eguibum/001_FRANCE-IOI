# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

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
