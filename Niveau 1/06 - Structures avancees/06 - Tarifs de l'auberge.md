# Tarifs de l'auberge

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Pour commencer, il faut bien compartimenter les différentes conditions. Si tu as moins de 10 ans, c'est 5 écus, si tu as 60 ans c'est gratuit, pour les autres c'est 30 écus + supplément de 10 écus SI ton bagage fait plus de 20 kilos. Rédigeons le pseudo-Code

```
Je récupère la valeur age
Je récupère la valeur poidBagage
Si age est strictement inférieur à 10
  j'affiche 5
Sinon si age vaut 60
  J'affiche 0
Sinon dans les autres cas
  Si poidBagage est supérieur ou égal à 20
    J'affiche 40
  Sinon
    J'affiche 30
```

## Python

<details>
  <summary>Solution</summary>

```Python
age = int(input())
poids = int(input())
if age < 10:
   print(5)
else:
   if age == 60:
      print(0)
   else:
      if poids >= 20:
         print(40)
      else:
         print(30)
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
      int âge = entrée.nextInt();
      int poids = entrée.nextInt();
      if(âge < 10)
      {
         System.out.println("5");
      }
      else
      {
         if(âge == 60)
         {
            System.out.println("0");
         }
         else
         {
            if(poids >= 20)
            {
               System.out.println("40");
            }
            else
            {
               System.out.println("30");
            }
         }
      }
   }
}
```

</details>
