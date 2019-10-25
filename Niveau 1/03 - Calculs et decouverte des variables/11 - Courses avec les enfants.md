# Courses avec les enfants

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Ici le piège est qu'il ne faut pas aller chercher les anneaux les uns après les autres dans la foulée, mais qu'il faut à chaque fois ramener l'anneau au point de départ.

En prenant en compte cela, le code se fait de lui même. Pour l'anneau 1, je me déplace d'une case, je reviens au départ, pour l'anneau 2 de deux cases, je reviens au départ, etc. Il va falloir imbriquer des boucles dont 2 se basent sur le numéro de l'anneau

```
Je définis ma variable anneau à 1
Je répète autant de fois qu'il y a d'anneau (ici 10 anneaux)
  Je répète autant de fois que l'anneau que je vais chercher ( ex : si je vais chercher l'anneau 3, je répète 3 fois)
    Aller à droite
  Ramasser l'anneau
  Je répète autant de fois que l'anneau que je vais chercher
    Aller à gauche
  Déposer l'anneau
  Je rajoute 1 à mon anneau pour passer à l'anneau suivant
```

## Python

<details>
  <summary>Solution</summary>

```Python
from robot import *
anneau = 1
for loop in range(10):
   for loop in range(anneau):
      droite()
   ramasser()
   for loop in range(anneau):
      gauche()  
   deposer()
   anneau = anneau + 1
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
      int anneau = 1;
      for (int loop1 = 1; loop1 <= 10; loop1 = loop1 + 1) {
         for (int loop2 = 1; loop2 <= anneau; loop2 = loop2 + 1) {
            droite();
         }
         ramasser();
         for (int loop2 = 1; loop2 <= anneau; loop2 = loop2 + 1) {
            gauche();
         }
         deposer();
         anneau = anneau + 1;
      }
   }
}
```

</details>
