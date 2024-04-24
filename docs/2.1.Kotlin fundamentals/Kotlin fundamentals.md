---
layout: default
chapitre: kotlin-fundamentals
presentation: kotlin-fundamentals
order: 6
---


## generic types

When you want a property to have differing data types, subclassing is not the answer. Instead, Kotlin provides something : 
- called generic types that allow you to have a single property that can have differing data types, depending on the specific use case

- You should now have three instances of the Question class—each with different data types for the answer—instead of three different classes, or instead of using inheritance. If you want to handle questions with a different answer type, you can reuse the same Question class.
  
  - fun main() {
    val question1 = Question<String>("Quoth the raven ___", "nevermore", "medium")
    val question2 = Question<Boolean>("The sky is green. True or false", false, "easy")
    val question3 = Question<Int>("How many days are there between full moons?", 28, "hard")
}

- An enum class is used to create types with a limited set of possible values.
- enum class Difficulty {
    EASY, MEDIUM, HARD
}

- Each possible value of an enum is called an enum constant. Enum constants are placed inside the curly braces separated by commas. The convention is to capitalize every letter in the constant name .


## Data class 
-  only contain data. They don't have any methods that perform an action .
-  Defining a class as a data class allows the Kotlin compiler to make certain assumptions, and to automatically implement some methods :
-   equals() and hashCode() functions that compare the properties of the class and return true if they are equal .
-   toString()  function that returns a string representation of the class. 
-   componentN() functions that let you get the values of the properties in the order of their declaration.

-   copy() function that lets you create a new instance of the class with some property values changed.



- Data classes are a special type of class in Kotlin that are designed to hold data. They are not meant to be subclassed or extended, and therefore cannot be declared as abstract, open, sealed, or inner.
  
- Abstract classes cannot be instantiated and are meant to be subclassed. They are used to define a common interface for a group of related classes.
Open classes can be subclassed, but they are not sealed. This means that subclasses can be defined in any file.
- Sealed classes can be subclassed, but only in the same file where the sealed class is defined. This helps to ensure that all subclasses of a sealed class are known at compile time.
- Inner classes are classes that are defined within another class. They have access to the private members of the outer class.

 

 - Nullable types are variables that can hold null.
- Non-null types are variables that can't hold null.  

```bash
fun main()  {
    var favoriteActor: String? = "Sandra Oh"
    println(favoriteActor)

    favoriteActor = null
    println(favoriteActor)
           }
```

## access to nullable variables  

- ?. if the variable is null, the expression after the ?. will not be evaluated. 
- ?:  if the variable is null, the expression after the ?: will be evaluated and returned.
- !!  if the variable is null, the program will crash.

```bash
fun main() {
    var favoriteActor: String? = "Sandra Oh"
    println(favoriteActor?.length)
}
```


| Modifier  | Accessible in same class | Accessible in subclass | Accessible in same module | Accessible outside module |
|-----------|--------------------------|------------------------|---------------------------|---------------------------|
| private   | ✔                        | ❌                      | ❌                         | ❌                         |
| protected | ✔                        | ✔                      | ❌                         | ❌                         |
| internal  | ✔                        | ✔                      | ✔                         | ❌                         |
| public    | ✔                        | ✔                      | ✔                         | ✔                         |



- A package in Kotlin is like a directory or a folder used to group related classes, functions, and other declarations together. It helps in organizing and managing the codebase in a logical and structured manner.
  - package com.example.myapp
  
- Module : 
 - In Kotlin Multiplatform projects, modules are used to define common code shared across different platforms (e.g., JVM, Android, iOS).
-  Modules can contain one or more packages and serve as logical units that contribute to the overall structure and organization of the project .
-  

## The difference between IS-A and HAS-A relationships.