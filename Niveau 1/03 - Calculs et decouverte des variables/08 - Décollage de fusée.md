# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

Même principe que la partie de cache-cache, sauf que cette fois-ci, on part de 100 pour aller à 0. Il s'agit donc d'un décompte.

```
Je définis ma variable décompte à 100
Je répète 101 fois (pour intégrer le 0)
  J'affiche décompte
  J'enlève 1 à décompte
J'affiche Décollage !
```

## Python

<details>
  <summary>Solution</summary>

```Python
compte = 100
for loop in range(101):
   print(compte)
   compte = compte - 1
print("Décollage !")
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
      int compte = 100;
      for (int loop = 1; loop <= 101; loop = loop + 1) {
         System.out.println(compte);
         compte = compte - 1;
      }
      System.out.println("Décollage !");
   }
}
```

</details>
