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
## Constructors  

## Encapsulation
Encapsulating fields and methods

## Abstraction
Creating abstract classes  
Traits

## Inheritance

## Polymorphism

