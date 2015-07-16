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
To access the fields:
```scala
var calc:Calculator = new Calculator
calc.make = "HP"
calc.model = "some-model-123"
println(calc.make) // HP
println(calc.model) // some-model-123

var calc2 = new Calculator // notice that the type is omitted.
calc2.make = "HP"
calc2.model = "some-model-123"
println(calc2.make)
println(calc2.model)

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

We may also have scala infer the type of our method:
```scala
class Calculator {
  def hello() = {
      println("Hello")
  }
}

new Calculator().hello // output: Hello
```

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

