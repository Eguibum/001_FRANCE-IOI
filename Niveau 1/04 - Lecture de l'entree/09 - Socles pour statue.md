# Socles pour statues

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Tu récupère la largeur de départ, ainsi que le nombre de niveau. Tu sais que chaque niveau diminue de 1 en largeur en montant. Avec tout ça, tu as tout ce qu'il faut pour programmer ton petit robot.

```
Je récupère la largeur
Je récupère le nombre de niveau
J'initialise mon total béton à 0
Je répète autant de fois que de niveau
  Je calcule le volume de béton du niveau
  J'ajoute ce volume à mon total
  je réduit ma largeur de 1
J'affiche le total béton
```

## Python

<details>
  <summary>Solution</summary>

```Python
largeurBas = int(input())
largeurHaut = int(input())
 
volume = 0
largeur = largeurHaut
for loop in range(largeurBas - largeurHaut + 1):
   volume = volume + largeur * largeur
   largeur = largeur + 1
 
print(volume)
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
import algorea.Scanner;
class Main {
   static Scanner entrée = new Scanner(System.in);
   public static void main(String[] args) {
      int largeurBas = entrée.nextInt();
      int largeurHaut = entrée.nextInt();
      int volume = 0;
      int largeur = largeurHaut;
      for (int loop = 1; loop <= largeurBas - largeurHaut + 1; loop = loop + 1) {
         volume = volume + largeur * largeur;
         largeur = largeur + 1;
      }
      System.out.println(volume);
   }
}
```

</details>
