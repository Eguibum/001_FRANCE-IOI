# Origami

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

On utilise une variable nommée épaisseur pour stocker l'épaisseur courante du pliage. Au début, cette épaisseur est de 0,11 millimètres. Pour faire doubler l'épaisseur, on utilise une affectation pour mettre la valeur épaisseur × 2 dans la variable épaisseur. On place cette affectation dans une boucle pour la répéter 15 fois de suite. Pour convertir en centimètres à la fin, il suffit de diviser le résultat par 10. 

```
épaisseur <- 0.11
Répéter 15 fois
   Multiplier épaisseur par 2
Afficher (épaisseur / 10)
```

## Python

<details>
  <summary>Solution</summary>

```Python
epaisseur = 0.11
for loop in range(15):
    epaisseur = epaisseur * 2
print(epaisseur / 10)
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
class Main
{
   public static void main(String[] args)
   {
      double épaisseur = 0.11;
      for (int loop = 1; loop <= 15; loop = loop + 1)
      {
         épaisseur = épaisseur * 2;
      }
      System.out.println(épaisseur / 10);
   }
}
```

</details>
