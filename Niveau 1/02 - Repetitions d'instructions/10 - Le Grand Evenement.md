# Le Grand évènement

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

C'EST LE CHALLENGE !!! Mais ne t'inquiètes pas, ça va bien se passer :)
Pour cet exercice, je recommande VIVEMENT un petit dessin papier pour que tu VISUALISES le chemin à faire afin d'être sûr(e) de ne pas repasser é fois au même endroit.

Le pseudo-code ci-dessous se base sur le chemin le plus logique et le plus simple, mais si tu veux t'amuser à faire des zig et des zag, grand bien te fasse, tant que tu passes une seule fois par case (une fois l'exercice fini, ça peut être drôle de faire le chemin de l'homme bourré xD ).

Bref, le plus simple est donc de faire un trajet de haut en bas, en se déplaçant vers la droite, puis de revenir sur la dernière ligne en bas.
 _    _
| |_ | |_ <= tu vas donc enchainer des trajets comme ça. Il existe plusieurs méthodes de découpage là encore, je vais partir sur la plus simple. Lis bien le pseudo-code ci-dessous, dessine les déplacements pour bien visualer le chemin et bien comprendre.

```
Je vais en haut
// Là tu es sur la case juste après le départ
// A partir d'ici tu vas faire des allers-retours sur 8 colonnes, sur 9 lignes

Je répète 4 fois
  Je répète 8 fois
    Aller en haut
  Aller à droite
  Je répète 8 fois
    Aller en bas
  Aller à droite
// Là tu as couvert la plus grande partie de la salle.

Je répète 8 fois
  Aller en haut
Aller à droite
// La tu es sur la case en haut à droite de la salle, tu ne peux pas aller plus à droite

Je répète 9 fois
  Aller en bas
// Là tu es tout en bas à droite de la salle

Je répète 9 fois
  Aller à gauche
// Là tu es tout en bas à droite de la salle

```

## Python

<details>
  <summary>Solution</summary>

```Python
from robot import *
haut()
# Allers-retours sur les 9 lignes du haut, pour les 8 premières colonnes
for loop in range(4):
   for loop in range(8):
      haut()
   droite()
   for loop in range(8):
      bas()
   droite()
# Deux dernières colonnes avec redescente jusqu'en bas
for loop in range(8):
   haut()
droite()
for loop in range(9):
   bas()
# Et on rentre à la position de départ
for loop in range(9):
   gauche()
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
      haut();
      // Allers-retours sur les 9 lignes du haut,
      // pour les 8 premières colonnes
      for (int loop = 1; loop <= 4; loop = loop + 1) {
         for (int loop2 = 1; loop2 <= 8; loop2 = loop2 + 1) {
            haut();
         }
         droite();
         for (int loop2 = 1; loop2 <= 8; loop2 = loop2 + 1) {
            bas();
         }
         droite();
      }
    
      // Deux dernières colonnes avec redescente jusqu'en bas
      for (int loop = 1; loop <= 8; loop = loop + 1) {
         haut();
      }
      droite();
      for (int loop = 1; loop <= 9; loop = loop + 1) {
         bas();
      }
    
      // Et on rentre à la position de départ
      for (int loop = 1; loop <= 9; loop = loop + 1) {
         gauche();
      }
   }
}
```

</details>
