# Jeu de dames

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Cet exercice est le premier à réellement prendre la tête, car il faut imbriquer des boucles. Attention, prends bien en compte le fait que des boucles imbriquées ne peuvent PAS avoir le même nom ! Sache que tu peux remplacer "loop" par le nom que tu veux tant que c'est clair et que tu t'y retrouves (on évitera cependant les noms type x, y, cft, et autres lâché de doigts aléatoire sur le clavier n__n").

Sinon d'un poids de vu gymnastique cérébrale, il faut décomposer chaque étape.
Tu veux répéter x fois XO sur une ligne, puis OX sur une ligne en dessous, et tu veux répéter x fois ces 2 lignes. C'est là que l'imbrication et l'indentation sont importentes.

Comme c'est un damier de 40 sur 40 et que tout est multiple de 2, on va partir là dessus, voilà ce que donne le pseudo-code.

```
Je répète 20 fois
  Je répète 20 fois
    j'imprime OX sur la même ligne
  Je vais à la ligne
  Je répète 20 fois
    J'imprime X0 sur la même ligne
  Je vais à la ligne
```

## Python

<details>
  <summary>Solution</summary>

```Python
for loop in range(20):
   for loop in range(20):
      print("OX", end = "")
   print()
   for loop in range(20):
      print("XO", end = "")
   print()
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
      for (int loop = 1; loop <= 20; loop = loop + 1) {
         for (int loop2 = 1; loop2 <= 20; loop2 = loop2 + 1) {
            System.out.print("OX");
         }
         System.out.println();
    
         for (int loop2 = 1; loop2 <= 20; loop2 = loop2 + 1) {
            System.out.print("XO");
         }
         System.out.println();
      }
   }
}
```

</details>
