# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

Ici, tu utilises ton robot. Donc n'oublie pas de l'importer. Ensuite, les étapes sont simples.
Ta position de départ compte comme 0. Donc quand tu te déplaces, le premier déplacement vaut 1, le deuxième 2, etc... C'est ce décompte qui te donne le nombre de répétition dans tes boucles.

```
J'importe le robot.
Je répète 2 fois
  Je me déplace à gauche
Je dis "Bonjour, laissez-moi vous aider"
Je ramasse
Je répète 32 fois
  Je me déplace à droite
Je dépose
```

## Python

<details>
  <summary>Solution</summary>

```Python
from robot import *
for loop in range(2):
   gauche()
print("Bonjour, laissez-moi vous aider")
ramasser()
for loop in range(32):
   droite()
deposer()
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
      gauche();
      gauche();
      System.out.println("Bonjour, laissez-moi vous aider");
      ramasser();
      for (int loop = 1; loop <= 32; loop = loop + 1) {
         droite();
      }
      deposer();
   }
}
```

</details>
