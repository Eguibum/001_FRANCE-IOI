# La bataille

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Si l'on a jamais joué à la bataille il est bon de prendre quelques exemples et de les traiter "à la main". Ils seront utiles ensuite pour tester le programme. Trois exemples au moins sont nécessaires (égalité parfaite, 1 gagne car il possède une meilleure carte, 1 gagne car 2 n'a plus de cartes). Ensuite on peut commencer à penser à la structure du programme. Si on se base sur ce que l'on a fait à la main, on a envie d'écrire :
```
Lire les chaines de caractères cartes1 et cartes2
Tant que le vainqueur est inconnu
  on continue à jouer en comptant les égalités
Afficher le vainqueur et le nombre d'égalités
```

Maintenant que l'on a fixé les grandes lignes du code, on peut rentrer dans les détails. Que signifie « le vainqueur est inconnu » ?

Cela correspond au cas où toutes les cartes étaient identiques et que chaque joueur à encore au moins une carte. Et dans ce cas que signifie « on continue à jouer » ?

```
On passe à la carte suivante.
nbCartes1 <- longueur(cartes1)
nbCartes2 <- longueur(cartes2)
nbEgalités <- 0
tour <- 0
Tant que tour < nbCartes1 ET tour < nbCartes2 ET cartes1[tour] = cartes2[tour]
   nbEgalités <- nbEgalités + 1
   tour <- tour + 1
```

Un examen plus attentif nous montre que les variables tour et nbEgalités sont identiques. Cette dernière variable est donc inutile. Et le code se simplifie donc en :

```
tour <- 0
Tant que tour < nbCartes1 ET tour < nbCartes2 ET cartes1[tour] = cartes2[tour]
   tour <- tour + 1
```

Reste à afficher les résultats. Le plus simple est le cas d'égalité parfaite.

```
Si tour = nbCartes1 ET tour = nbCartes2
```

Si l'on n'est pas dans ce cas c'est que l'un des joueur à gagné. Par exemple, le joueur 1 à gagné quand le joueur 2 n'a plus de cartes ou quand il lui reste une carte et quelle est meilleure que celle de son adversaire. Ce qui se traduit par

```
sinon si tour = nbCartes2 OU (tour < nbCartes1 ET cartes1[tour] < cartes2[tour])
```

## Python

<details>
  <summary>Solution</summary>

```Python
main1 = input()
main2 = input()
tour = 0
while tour < len(main1) and tour < len(main2) and main1[tour] == main2[tour]:
   tour = tour + 1
if tour == len(main1) and tour == len(main2):
   print("=")
elif tour == len(main2) or (tour < len(main1) and main1[tour] < main2[tour]):
   print(1)
else:
   print(2)
print(tour)
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
   public static void main(String [] args)
   {
      Scanner entree = new Scanner(System.in);
      String main1 = entree.next();
      String main2 = entree.next();
      int long1 = main1.length();
      int long2 = main2.length();
      int tour = 0;
      while (tour < long1 && tour < long2 && main1.charAt(tour) == main2.charAt(tour))
         tour++;
      if (tour ==long1 && tour == long2)
         System.out.println("=");
      else if (tour == long2 || (tour < long1 && main1.charAt(tour) < main2.charAt(tour)))
         System.out.println("1");
      else
         System.out.println("2");
      System.out.println(tour);
   }
}
```

</details>

<details>
  <summary>Ma solution, avec l'aide de plusieurs membres du site (dont la-prof)</summary>


```Java
import algorea.Scanner;
class Main {
   static Scanner input = new Scanner(System.in);
   
   public static void main(String[] args) {
   
      String joueur1 = input.nextLine();
      String joueur2 = input.nextLine();
      String gagnant = "unknown";
      
      // Je calcule la longueur minimale
      int longueurMin = 0;
      if (joueur1.length() < joueur2.length()) {
         longueurMin = joueur1.length();
      } else if (joueur2.length() < joueur1.length()) {
         longueurMin = joueur2.length();
      } else if (joueur1.length() == joueur2.length()){
         longueurMin = 26;
      }
      
      // tant que les joueurs ont des cartes similaires, j'incrémente l'égalité et je passe à la carte suivante
      int égalité = 0;
      int numChar= 0;
      while((numChar < longueurMin-1) && (joueur1.charAt(numChar) == joueur2.charAt(numChar))) {
         égalité++;
         numChar++;
      }
      if (joueur1.charAt(numChar) == joueur2.charAt(numChar)){
           égalité++;
      }if (joueur1.charAt(numChar) < joueur2.charAt(numChar)){
       gagnant="1";
        } else if (joueur1.charAt(numChar) == joueur2.charAt(numChar) && (joueur1.length() > joueur2.length())){
         gagnant = "1"; 
          
         } else if (joueur1.charAt(numChar) > joueur2.charAt(numChar)){
         gagnant = "2";
         } else if (joueur1.charAt(numChar) == joueur2.charAt(numChar) && (joueur1.length() < joueur2.length())){
         gagnant = "2"; 
         } else if (joueur1.charAt(longueurMin-1) == joueur2.charAt(longueurMin-1)){
         gagnant = "=";
      } 
      System.out.println(gagnant);
      System.out.println(égalité);
   }
}
```

</details>
