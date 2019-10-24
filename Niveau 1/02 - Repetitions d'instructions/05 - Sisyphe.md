# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

Petit robot présent ! Ajoutes ton module et liste tes instructions. Pour visualiser correctement les déplacements, un dessin sur papier peut s'avérer très utile (personnellement, je fais un pseudo-code papier avec illustration quasiment à chaque fois).
Il est important de comprendre le sens des déplacements. D'abord tu montes puis tu vas à droite. L'erreur est ensuite de dire tu descends puis tu vas à gauche. Mais non. L'inverse de haut - droite, c'est gauche - bas, et non bas - gauche ! Tu répètes ces 4 instructions autant de fois que nécessaire ;)

```
Je répète 21 fois
  je vais en haut
  je vais à droite
Je répète 21 fois
  Je vais à gauche
  Je vais à droite
```

## Python

<details>
  <summary>Solution</summary>

```Python

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
import static algorea.Robot.*;
class Main {
   public static void main(String[] args) {
      for (int loop = 1; loop <= 21; loop = loop + 1) {
         haut();
         droite();
      }
      for (int loop = 1; loop <= 21; loop = loop + 1) {
         gauche();
         bas();
      }
   }
}
```

</details>
