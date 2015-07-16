# OOP Concepts in Scala

## Basics
Expressions  
Variables
Types

## Classes
## Creating a class  
Creating a class in Scala uses the ``class`` keyword followed by the class name and its opening and closing brackets.
```scala 
class Calculator {}
```
To create an instance of this class, we use the ``new`` keyword.
```scala
new Calculator()
new Calculator // we can also emit the parentheses
```
## Fields  
```scala 
class Calculator {
  var make:String = ""
  var model = "" // leaving off the type is allowed because it is inferred by Scala
}
```
Scala actually automatically generates accessors and mutators for your fields.
```scala
var calc = new Calculator // type is also inferred here
calc.make = "HP"
calc.model = "some-model-123"
```
## Methods  
Methods are defined using ``def``
```scala
class Calculator {
  def hello():Unit = {
      println("Hello")
  }
}

new Calculator().hello() // output: Hello
new Calculator().hello // output: Hello
```
The method ``hello``'s return type here is ``Unit`` which can be treated as an equivalent of ``void`` in java,c,c++

To add parameters/arguments to our method, declare variables inside the parentheses omittin the ``var`` keyword.
```scala
class Calculator {
  def hello(name:String):Unit = {
      println("Hello, " + name)
  }
}

new Calculator().hello("paul") // prints Hello, paul
```

Arithmetic operations are also methods
```scala

1 + 5  // plus here is a method of the class Int. This expression's result is 6
1.+(5) // the method above is translated into this

```
In the last example the number 1 is an ``Int`` having the method ``+`` taking the number 5 as its parameter.


## Constructors  

## Encapsulation
Encapsulating fields and methods

## Abstraction
Creating abstract classes  
Traits

## Inheritance

## Polymorphism

