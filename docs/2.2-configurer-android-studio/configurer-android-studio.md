---
layout: default
chapitre: Configurer android studio
presentation: Configurer android studio
order: 3
---

# Question


- Donnez les définitions des termes suivants :

- JVM
- JRE
- JDK
- IDE
- Android Gradle
- Android API Levels






# Configurer android studio

## JRE

- ![JRE](/besoin/2.2-configurer-android-studio/configurer-android-studio.md){: width="700px" }*Figure : JRE*


- The Java Runtime Environment, or JRE, is a software layer that runs on top of a computer’s operating system software and provides the class libraries and other resources that a specific Java program requires to run.


## How does JRE work ?

- JRE interact with one another to create a sustainable runtime environment that enables the seamless execution of Java-based applications in virtually any operating system. These attributes make up the JRE runtime architecture:

- ClassLoader
The Java ClassLoader dynamically loads all classes necessary to run a Java program. Since Java classes are only loaded into memory when they're required, the JRE uses ClassLoaders to automate this process on demand.

- Bytecode verifier
The bytecode verifier ensures the format and accuracy of Java code before it passes to the interpreter. If code violates system integrity or access rights, the class will be considered corrupted and won't be loaded.

- Interpreter
After the bytecode successfully loads, the Java interpreter creates an instance of the JVM that allows the Java program to be run natively on the underlying machine.



- Reference 
- [https://www.ibm.com/topics/jre](https://www.ibm.com/topics/jre)