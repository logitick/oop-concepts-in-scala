# Basics

## Expressions
Let’s begin with evaluating expressions in Scala. Scala is
a very expressive language. If you don’t have Scala on your 
computer you may use a [web REPL](http://codebunk.com/b/).

Scala will evaluate arithemtic expressions you enter in its REPL.
These expressions can be as simple as 1 + 1
```scala
scala> 1 + 1 
res0: Int = 2    
```

```scala
scala> 2 * 3                                                                    
res1: Int = 6    
```
```scala
scala> 2 * 3                                                                    
res2: Int = 6    
```


## Types
Everything in Scala is an object. The numbers used in the examples above are of type ``Int``. Methods/functions are also objects. All objects in Scala extend the class ``Any``.

## Variables
To declare a variable, use the key word ``var`` followed by its identifier, type, and initialization.
```scala
var oneDigitNumber = 5
```
