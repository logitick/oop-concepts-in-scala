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
### Returning values
Scala will return the last statement inside of the method:
```scala
class Calculator {
  def getPi() = {
      3.14159265359
  }
}

println(new Calculator().getPi) //3.14159265359
```
In the example above, ``getPi``'s return type is ``Double``.

Scala also allows returning multiple values from a method
```scala
class Calculator {
  def getNumbers() = {
      (3.14159265359, 2.7182818284)
  }
}

println(new Calculator().getNumbers) // returns (3.14159265359,2.7182818284)
```

### One-liners
You can omit the braces for methods consisting only of one statement. The parenthesis can also be omitted if the method takes no arguments.
```scala
class Calculator {
  def getPi() = 3.14159265359
  def hello = println("Hello")
}

println(new Calculator().getPi) //3.14159265359
new Calculator().hello // Hello
```
### Parameters
To add parameters/arguments to our method, declare variables inside the parentheses omittin the ``var`` keyword.
```scala
class Calculator {
  def hello(name:String):Unit = {
      println("Hello, " + name)
  }
}

new Calculator().hello("paul") // prints Hello, paul
```   
To use multiple parameters, you may add a comma in between them.
```scala
class Calculator {
  def hello(firstName:String, lastName: String) = {
      println("Hello, " + firstName + " " + lastName)
  }
}

new Calculator().hello("Paul Daniel", "Iway") // prints Hello, Paul Daniel Iway
```
Scala supports named paramters
```
class Calculator {
  def hello(firstName:String, lastName: String) = {
      println("Hello, " + firstName + " " + lastName)
  }
}

new Calculator().hello(lastName ="Iway", firstName = "Paul Daniel") // prints Hello, Paul Daniel Iway
```
### Arithmetics as methods
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

