# Invasion de batraciens

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Là il y a une petite subtilité. Il faut assigner le résultat du calcul à la variable que tu as définis. Tu as un nombre X de crapaud en début de semaine. La semaine suivante, tu as é fois plus de crapauds. Donc ta variable crapaud = valeur de crapaud + valeur de crapaud !

```
Je définis ma variable nbCrapauds à 1337
Je répète 12 fois
  nbCrapauds = nbCrapauds * 2
J'affiche nbCrapauds
```

## Python

<details>
  <summary>Solution</summary>

```Python
nbCrapauds = 1337
for loop in range(12):
    nbCrapauds = nbCrapauds * 2
print(nbCrapauds)
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
      int nbCrapauds = 1337;
      for (int loop = 1; loop <= 12; loop = loop + 1) {
         nbCrapauds = nbCrapauds * 2;
      }
      System.out.println(nbCrapauds);
   }
}
```

</details>
