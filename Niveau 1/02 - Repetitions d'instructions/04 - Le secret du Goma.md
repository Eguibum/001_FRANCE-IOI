# Le secret du goma

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Mais qu'est-ce donc que ce Goma ? Tu le sauras dans la correction ;)
Concernant les insctructions, on n'oublie pas son module robot. Ensuite, on détaille les étapes, comme d'habitude. L'allée fait 17 cases, mais la dernière case n'a pas de Goma. Tu peux donc la laisser hors boucle. Tu vas donc répéter 16 fois les mêmes actions et rajouter un déplacement et une action APRES ta boucle.

```
Répéter 16 fois
  Je vais à droite
  Je ramasse
Je vais à droite
Je dépose
```

## Python

<details>
  <summary>Solution</summary>

```Python
from robot import *
for loop in range(15):
   droite()
   ramasser()
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
      for (int loop = 1; loop <= 15; loop = loop + 1) {
         droite();
         ramasser();
      }
      droite();
      deposer();
   }
}
```

</details>
