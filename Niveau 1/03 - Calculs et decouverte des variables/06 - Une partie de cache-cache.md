# TITRE DE L'EXERCICE

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

Dans cet exercice tu vas voir comment modifier la valeur du variable. Après tout, son but est bien de varier, non ?

Ici, tu dois compter. Donc partir d'un nombre et ajouter une certaine valeur à chaque fois. Comment faire ? Dans une boucle pardi !

```
Je définis ma variable compte et je l'initialise à 1
Je répète 100 fois
  J'imprime ma variable compte
  Je rajoute 1 à ma variable compte
J'imprime J'arrive !
```

## Python

<details>
  <summary>Solution</summary>

```Python
compte = 1
for loop in range(100):
   print(compte)
   compte = compte + 1
print("J'arrive !")
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
      int compte = 1;
      for (int loop = 1; loop <= 100; loop = loop + 1) {
         System.out.println(compte);
         compte = compte + 1;
      }
      System.out.println("J'arrive !");
   }
}
```

</details>
