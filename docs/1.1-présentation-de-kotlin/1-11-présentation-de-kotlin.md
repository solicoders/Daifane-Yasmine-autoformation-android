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




- Inférence de type ?

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



 - we have this error `Val cannot be reassigned`


##  Variables and data types



## Références 
- https://developer.android.com/training/kotlinplayground