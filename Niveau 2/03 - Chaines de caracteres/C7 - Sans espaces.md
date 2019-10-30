# Sans espaces

## Pseudo-Code

_Le pseudo-code est important, c'est l'étape qui permet de mettre à plat ses idées. Le mieux est de le faire sur papier et d'écrire le déroulement de l'algorithme, en français, comme si tu rédigeais une liste de choses à faire._

**Conseil France IOI :**

**Lisez bien les exemples ! Ils sont là pour vous aider, pour que vous compreniez bien quelles sont les données à lire et ce que doit calculer votre programme.**

**Les exemples du sujet sont d'excellents supports pour vous assurer que vous avez bien compris le problème posé. À chaque fois, essayez pour chaque exemple de calculer vous-même le résultat à partir des données d'entrée, et vérifiez que la sortie correspond. Si vous n'êtes pas d'accord avec l'exemple, vous aurez beaucoup de mal à résoudre l'exercice !**

Après avoir lu la ligne de texte, il existe deux variantes pour cet exercice :

  - remplacer les espaces par des '_' dans le texte puis l'afficher,
  - regarder les caractères un par un et les afficher (ou afficher '_' s'il s'agit d'un espace).

Ci-dessous nous vous présentons les deux variantes, n'hésitez pas à les comparer afin de voir celle que vous préférez. 

```

```

## Python

<details>
  <summary>Solution 1 : avec modification de texte</summary>

```Python
texte = list(input())
for pos in range(len(texte)):
   if texte[pos] == " ":
      texte[pos] = "_"
print("".join(texte))
```

</details>

<details>
  <summary>Solution 2 : sans modification de texte</summary>

```Python
texte = list(input())
for pos in range(len(texte)):
   if texte[pos] == " ":
      texte[pos] = "_"
print("".join(texte))
```

</details>

## Java

Code minimal Java

<details>
  <summary>Minimum fonctionnel</summary>

```Java
texte = input()
for pos in range(len(texte)):
   if texte[pos] == " ":
      print("_", end = "")
   else:
      print(texte[pos], end = "")
print()
```

</details>

</br>
Et avec les instructions :)
</br>
</br>

<details>
  <summary>Solution 1 : avec modification de texte</summary>


```Java
import algorea.Scanner;
class Main
{
   public static void main(String[] args)
   {
      Scanner input = new Scanner(System.in);
      StringBuffer texte = new StringBuffer(input.nextLine());
      for (int iLettre = 0; iLettre < texte.length(); iLettre = iLettre + 1)
      {
         if (texte.charAt(iLettre) == ' ')
         {
            texte.setCharAt(iLettre,'_');
         }
      }
      System.out.println(texte);
   }
}
```

</details>

<details>
  <summary>Solution 2 : sans modification de texte</summary>


```Java
import algorea.Scanner;
class Main
{
   public static void main(String[] args)
   {
      Scanner input = new Scanner(System.in);
      String texte = input.nextLine();
      for (int iLettre = 0; iLettre < texte.length(); iLettre = iLettre + 1)
      {
         char car = texte.charAt(iLettre);
         if (car  == ' ')
         {
            System.out.print('_');
         }
         else
         {
            System.out.print(car);
         }
      }
      System.out.println();
   }
}
```

</details>
