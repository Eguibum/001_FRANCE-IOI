# Protection du village

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Cet exercice est un peu chiadé, avouons-le ! Tu vas un peu te prendre la tête dessus, il faut prendre son temps. Tu dois calculer un périmètre rectangulaire de protection qui entoure toutes les maisons dont on va te donner les abscisses et ordonnées. Jusque là, ça va ? Super !

Pour calculer un périmètre, il te faut une longueur et une largeur. Pour calculer cette longueur et cette largeur, tu dois déterminer les maximales et minimales des abscisses et ordonnées. En effet, abcisseMax - abcisseMin = largeur, ordonnéeMax - ordonnéeMin = longueur. Tu suis toujours ? Parfait !

On te dit que les valeurs sont comprises entre 0 et 1000000 (ouaip, tout ça). Pour déterminer l'abscisse et l'ordonnée maximales, il faut que les valeurs que tu récupères soit supérieur à 0 (pour pouvoir les comparer). pour déterminer l'abscisse et l'ordonnées minimales, les valeurs doivent être inférieur à 1000000. Et oui, logique. A partir de là, c'est simple.

Tu définis tes absMin et ordMin à 1000000 et tes absMAx et ordMax à 0, et il ne reste que des comparaisons à faire, pour récupérer les min et max et calculer le reste. On y va ?

```
J'initialise abcisseMin à 100000
J'initialise ordonnéeMin à &00000
J'initialise abcisseMax à 0
J'initialise ordonnéeMax à 0
Je récupère le nombre de maisons
Je répète autant de fois qu'il y a de maison
  Je récupère abcisseMaison
  Je récupère ordonnéeMaison
  Si abcisseMaison est inférieur à abcisseMin
    abscisseMin prend la valeur de abcisseMaison
  Si ordonnéeMaison est inférieur à ordonnéeMin
    ordonnéeMin prend la valeur de ordonnéeMaison
  Si abcisseMaison est supérieur à abcisseMax
    abscisseMax prend la valeur de abcisseMaison
  Si ordonnéeMaison est supérieur à ordonnéeMax
    ordonnéeMax prend la valeur de ordonnéeMaison
Je calcule largeur = abcisseMAx - abcisseMin
Je calcule longueur = ordonnéeMax - ordonnéeMin
J'initialise périmètre = (longueur + largeur) * 2
J'affiche périmètre
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbMaisons = int(input())
xMin = 1000 * 1000
xMax = 0
yMin = 1000 * 1000
yMax = 0
for loop in range(nbMaisons):
   posX = int(input())
   posY = int(input())
   if posX < xMin:
      xMin = posX
   if posX > xMax:
      xMax = posX
   if posY < yMin:
      yMin = posY
   if posY > yMax:
      yMax = posY
      
largeur = xMax - xMin
hauteur = yMax - yMin
perimetre = 2 * (largeur + hauteur)
print(perimetre)
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
class Main
{
   public static void main(String[] args)
   {
      Scanner entrée = new Scanner(System.in);
      int nbMaisons = entrée.nextInt();
      
      int infini = 1000 * 1000;
      int xMin = infini, xMax = 0, yMin = infini, yMax = 0;
      
      for (int loop = 1; loop <= nbMaisons; loop = loop + 1)
      {
         int posX = entrée.nextInt();
         int posY = entrée.nextInt();
         if(posX < xMin)
         {
            xMin = posX;
         }
         if(posX > xMax)
         {
            xMax = posX;
         }
         if(posY < yMin)
         {
            yMin = posY;   
         }
         if(posY > yMax)
         {
            yMax = posY;
         }
      }     
      int largeur = xMax - xMin, hauteur = yMax - yMin;
      int périmètre = 2 * (largeur + hauteur);
      System.out.println(périmètre);
   }
}
```

</details>
