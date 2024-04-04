---
layout: default
chapitre: introduction
presentation: introduction
order: 2
---
# présentation-de-kotlin

## Befor u begin
Compose  :
- Android's modern toolkit for building native UI
-  simplifies and accelerates UI development
-  It requires less code to implement a UI compared to the Android View system
-   makes your app easier to maintain
##  Android Basics with Compose
- Android devices
  - tvs ,phones , cars, tablets,watches
  - android studio  tool we use to write our code 
  - emulator if u don't have android phone gonna help us stimulate an android device in ur computer 
  ## Your first program in Kotlin
  ### Kotline 
  - is a modern programming language recommended by Google when creating new Android apps .
  - more concise code 
  - Apps that are built with Kotlin are also less likely to crash
  - with Kotlin, you can write better Android apps in a shorter amount of time
  ### Codelab 
  - explore and modify simple programs in Kotlin
  - code editor : 
    - autocomplete
    -  suggestions while you type,
    -   and displays error messages when code is incorrect
- Kotline Playground : to see the output of the code 
- Kotlin compiler
  
  ### Your first program in Kotlin
  - function :  is a segment of a program that performs a specific task
  - fun : is a keywords  used before the name of the function
  - Function names `takePhoto`:
    - should follow the camel case convention :
    -  where the first word of the function name is all lower case.
    -    there are no spaces between words, 
    -    and all other words should begin with a capital letter.
-  An input is : a piece of data that a function needs to perform its purpose. 
    -  When you define a function, you can require that certain inputs be passed in when the function is called. 
    -  If there are no inputs required for a function, the parentheses are empty ()
  
  
  ```bash
  fun main() {
    println("Hello , Word !")
  }
  ```

  - ![function in kotlin](/android/1.1-présentation-de-kotlin/images/functionkotlin.png){:width="900px"}*figure: function kotlin*




- Inférence de type :  The Kotlin compiler automatically infers the types of  variables without explicit declaration.
  - val count = 2
  - val count: Int

- Expliquer le message d'erreur de ce code : 

  ```bash
  fun main() {
    var nom = "Fouad"
    var bonjour_nom = Bonjour(nom)
    println (bonjour_nom)
    println (nom)
   }

  fun Bonjour(nom:String):String{
    nom =  "Bonjour" + nom
    return nom
     }
  ```



```bash
 fun main() {
  val birth = 2002
  val now  = 2024
    
   println("You have ${now-birth} unread messages")    
   }

   `Output = You have 22 unread messages`
```

 - we have this error `Val cannot be reassigned`


##  Variables and data types

- Keyword to define new variable
To define a new variable, start with the Kotlin keyword val (which stands for value). Then the Kotlin compiler knows that a variable declaration is in this statement.
- val keyword - Use when you expect the variable value will not change.
- var keyword - Use when you expect the variable value can change.

## Questions
- Créer un programme qui demande deux valeurs à l'utilisateur. Ensuite, il calcule la somme de ces deux valeurs.

```bash
fun main() {
   println("Entrez la première valeur :")
    val valeur1 = readLine()!!.toInt()

    println("Entrez la deuxième valeur :")
    val valeur2 = readLine()!!.toInt()

    val somme = valeur1 + valeur2
    println("La somme de $valeur1 et $valeur2 est : $somme")
  }
```


## Références 
- https://developer.android.com/training/kotlinplayground