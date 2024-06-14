## 4. [Define of thread:](https://www.simplilearn.com/tutorials/java-tutorial/thread-in-java#:~:text=A%20thread%20in%20Java%20is,starting%20of%20the%20program's%20execution.)

- A thread in [Java](https://www.simplilearn.com/best-java-programs-article "Java") is the direction or path that is taken while a program is being executed. Generally, all the programs have at least one thread, known as the main thread, that is provided by the JVM or [Java Virtual Machine](https://www.simplilearn.com/jvm-and-the-implications-of-sandbox-model-rar41-article "Java Virtual Machine") at the starting of the program’s execution.
- **A thread is an execution thread in a program**. 
- Multiple threads of execution can be run concurrently by an application running on the Java Virtual Machine. 
- The priority of each thread varies. Higher priority threads are executed before lower priority threads.
- Thread in Java enables concurrent execution, dividing tasks for improved performance. 
- It's essential for handling operations like I/O and network communication efficiently.
![[Pasted image 20240614184037.png]]
<img src="Pasted image 20240614184037.png" alt="thread" />

![[Pasted image 20240614184222.png]]

<img src="Pasted image 20240614184222.png" alt="thread_output" />


## 3. What is Exception in Java?

**Dictionary Meaning:** Exception is an abnormal condition.

In Java, an exception is an event that disrupts the normal flow of the program. It is an object which is thrown at runtime.

#### What is Exception Handling?

Exception Handling is a mechanism to handle runtime errors such as ClassNotFoundException, IOException, SQLException, RemoteException, etc.

#### Types of Java Exceptions

There are mainly two types of exceptions: checked and unchecked. An error is considered as the unchecked exception. However, according to Oracle, there are three types of exceptions namely:

1. Checked Exception
2. Unchecked Exception
3. Error

#### 1) Checked Exception

The classes that directly inherit the Throwable class except RuntimeException and Error are known as checked exceptions. For example, IOException, SQLException, etc. Checked exceptions are checked at compile-time.

#### 2) Unchecked Exception

The classes that inherit the RuntimeException are known as unchecked exceptions. For example, ArithmeticException, NullPointerException, ArrayIndexOutOfBoundsException, etc. Unchecked exceptions are not checked at compile-time, but they are checked at runtime.

#### 3) Error

Error is irrecoverable. Some example of errors are OutOfMemoryError, VirtualMachineError, AssertionError etc.

```java
**JavaExceptionExample.java**

1. public class JavaExceptionExample{  
2.   public static void main(String args[]){  
3.    try{  
4.       //code that may raise exception  
5.       int data=100/0;  
6.    }catch(ArithmeticException e){System.out.println(e);}  
7.    //rest code of the program   
8.    System.out.println("rest of the code...");  
9.   }  
10. }
```

```
**Output:**

Exception in thread main java.lang.ArithmeticException:/ by zero
rest of the code...
```

## 1. Java Conditions and If Statements

You already know that Java supports the usual logical conditions from mathematics:

- Less than: a < b
- Less than or equal to: a <= b
- Greater than: a > b
- Greater than or equal to: a >= b
- Equal to a == b
- Not Equal to: a != b

You can use these conditions to perform different actions for different decisions.

Java has the following conditional statements:

- Use `if` to specify a block of code to be executed, if a specified condition is true
- Use `else` to specify a block of code to be executed, if the same condition is false
- Use `else if` to specify a new condition to test, if the first condition is false
- Use `switch` to specify many alternative blocks of code to be executed

#### The if Statement

Use the `if` statement to specify a block of Java code to be executed if a condition is `true`.

```java
int x = 20;
int y = 18;
if (x > y) {
  System.out.println("x is greater than y");
}
```

#### Else:

```java
int time = 20;
if (time < 18) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
// Outputs "Good evening."
```

Else if:

```java
int time = 22;
if (time < 10) {
  System.out.println("Good morning.");
} else if (time < 18) {
  System.out.println("Good day.");
} else {
  System.out.println("Good evening.");
}
// Outputs "Good evening."
```

#### Short Hand if...else

There is also a short-hand [if else](https://www.w3schools.com/java/java_conditions.asp), which is known as the **ternary operator** because it consists of three operands.

It can be used to replace multiple lines of code with a single line, and is most often used to replace simple if else statements:

### Syntax

```java
variable = (condition) ? expressionTrue :  expressionFalse;
```
## [2. Inheritance in Java](https://www.geeksforgeeks.org/inheritance-in-java/)

- Inheritance is an important pillar of OOP(Object-Oriented Programming). 
- It is the mechanism in Java by which one class is allowed to inherit the features(fields and methods) of another class. 
- In Java, Inheritance means creating new classes based on existing ones. 
- A class that inherits from another class can reuse the methods and fields of that class. 
- In addition, you can add new fields and methods to your current class as well.

#### Why Do We Need Java Inheritance?

- ****Code Reusability:**** The code written in the Superclass is common to all subclasses. Child classes can directly use the parent class code.
- ****Method Overriding:**** [Method Overriding](https://www.geeksforgeeks.org/overriding-in-java) is achievable only through Inheritance. It is one of the ways by which Java achieves Run Time Polymorphism.
- ****Abstraction:**** The concept of abstract where we do not have to provide all details is achieved through inheritance. [Abstraction](https://www.geeksforgeeks.org/abstraction-in-java-2) only shows the functionality to the user.

#### ****Important Terminologies Used in Java Inheritance****

- ****Class:**** 
	- Class is a set of objects which shares common characteristics/ behavior and common properties/ attributes. Class is not a real-world entity. 
	- It is just a template or blueprint or prototype from which objects are created.
- ****Super Class/Parent Class:**** 
	- The class whose features are inherited is known as a superclass(or a base class or a parent class).
- ****Sub Class/Child Class:**** 
	- The class that inherits the other class is known as a subclass(or a derived class, extended class, or child class). 
	- The subclass can add its own fields and methods in addition to the superclass fields and methods.
- ****Reusability:**** 
	- Inheritance supports the concept of “reusability”, i.e. when we want to create a new class and there is already a class that includes some of the code that we want, we can derive our new class from the existing class. 
	- By doing this, we are reusing the fields and methods of the existing class.

#### Syntax:

```
class DerivedClass extends BaseClass    
{    
   //methods and fields    
}
```

```java
// Java Program to illustrate Inheritance (concise)

import java.io.*;

// Base or Super Class
class Employee {
    int salary = 60000;
}

// Inherited or Sub Class
class Engineer extends Employee {
    int benefits = 10000;
}

// Driver Class
class Gfg {
    public static void main(String args[])
    {
        Engineer E1 = new Engineer();
        System.out.println("Salary : " + E1.salary
                           + "\nBenefits : " + E1.benefits);
    }
}
```

```
**Output**

Salary : 60000
Benefits : 10000
```

#### ****Java Inheritance Types****

Below are the different types of inheritance which are supported by Java.

1. Single Inheritance
2. Multilevel Inheritance
3. Hierarchical Inheritance
4. Multiple Inheritance
5. Hybrid Inheritance


## 5. Features of Java:

#### **1. Simple and Easy to Learn**

Java is easy to learn and simple to use as a programming language. It is because of following reasons:

- Java comprises the same syntax as C, and C++.
- It holds automatic garbage collection features.


#### **2. Object-Oriented Programming**

Almost everything written in Java is object and class, making it a true object-oriented programming (OOP) language. The basic concept of OOP is:

- **Object:** Object is a real-world entity in Java that encompasses state, functionality, and identity.
- **Class:** Class is a logical entity which includes a group of objects with common properties. It contains fields, methods, constructors, blocks, nested classes and interfaces.
- **Inheritance:** It’s a concept in Java through which developers can create new classes built upon existing classes to achieve runtime polymorphism.
- **Polymorphism:** A Mechanism in Java through which you can perform a single action in multiple ways. Polymorphism can be of two types- Compile time and runtime.
- **Abstraction:** It’s a method to hide internal processing and show only essential things to the users.

#### **3. Platform Independence**

Unlike other languages, Java is not limited to any specific machine and dependent on other factors to run. The Java platform is independent because:

- It uses a runtime environment of its own, i.e. JVM.
- It is a write-once, run-anywhere language.
- It is a software-based platform that runs on top of other hardware-based platforms.
- Its code can be executed on multiple platforms, including Windows, Linux, Sun Solaris, and Mac/OS.
- The Java code is compiled by the compiler and converted into bytecode.

#### **4. Automatic Memory Management**

Automatic memory management is a crucial feature of Java programming. It helps in:

- Create high-performance system.
- Automatically allocate and free up space for objects.
- Eliminating the worries about memory management.
- Issues like object destruction don’t occur.
- There is no need to add memory management logic.

#### **5. Security**

Java programming language is known for its security. With it, you can create virus-free systems because:

- Java programming language runs inside a virtual machine.
- It uses its own runtime environment- JVM.
- Java includes a security manager, which determines what resources a class can access, such as reading and writing to the local disk.
- In Java run time, a class loader separates the package for the classes of the local file system from the files imported from network sources.
- Java also consists of Bytecode Verifier, which checks the code fragments for illegal code.

#### **6. Rich API**

Being one of the oldest programming languages, Java has a rich API. Some popular Java APIs are:

- Java Advanced Imaging (JAI)
- Java Data Objects (JDO)
- Java Media Frameworks (JMF)
- Java Persistence API (JPA)
- Java 3D (J3D)

#### **7. Multithreading**

Multithreading is an essential feature of Java that makes Java programming exclusive. It offers several benefits:

- It lets Java developers execute multiple threads at the same time.
- It’s used to achieve multitasking.
- It saves time.
- It’s mostly used in games and animation.
- Threads work independently and don’t impact other threads, even if created simultaneously.

#### **8. High Performance**

Java is a programming language with a high-performance rate. It is because:

- Java uses bytecode that can be easily translated into native machine code.
- It has multiple easy-to-use frameworks.
- It is compatible with multiple platforms, including Windows, Linux, Sun Solaris, and Mac/OS.
- It is a write-once, run-anywhere language.
- Java also automatically clears the garbage to enhance its performance.

#### **9. Scalability**

Java offers its users scalability, which means it can deal with more and more users and works. It is so because:

- Java is an object-oriented programming language.
- It has the ability to handle large databases.
- Java doesn’t require multiple resources while running.
- It uses multithreading and multiprocessing.\
- Java includes a higher volume of code.

#### **10. Simplified Syntax**

Java is one of the most used programming languages with simplified syntax. Some basic features of writing syntax for Java:

- Java programming language is easily understood by the compiler and computer.
- It is case-sensitive, which means “hello world” or “HelloWorld” are two different things.
- It includes a bunch of objects and classes.
- The Java code statements end with semicolons (;).
- In Java syntax, there are delimiters “{…}” that denote a block of code.