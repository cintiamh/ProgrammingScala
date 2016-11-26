# Fist Steps in Scala

You can install Scala in your machine following the instructions here: http://www.scala-lang.org/download/. 
You can also use plugins in your favorite IDE like Eclipse, InteliJ, or Netbeans.

## Step 1: Learn to use the Scala interpreter
 
The Scala interpreter is an interactive "shell" for writing Scala expressions and programs.

```
$ scala

scala>
```

Then you can press in expressions like:

```
scala> 1 + 2
res0: Int = 3
```

The response includes:

* `res0`: an automatically generated name to refer to the computed value.
* `: Int`: a colon, followed by the type of the expression.
* `= 3`: the value resulting from evaluating the expression.

All Java's primitive types have corresponding class in the `scala` package. Scala's `Int` corresponds to
Java's `int`.

```
scala> println("Hello, world!")
Hello, world!
```

## Step 2: Define some variables

Scala has two types of variables:

* `val`: once initialized, a `val` can never be reassigned.
* `var`: can be reassigned throughout its lifetime.

```
scala> val msg = "Hello, world!"
msg: String = Hello, world!
```

Here Scala inferred the type of `msg` to be `String`. When the Scala interpreter can infer types, it is
often best to let it do so rather than fill the code with unnecessary, explicit type annotations.

```
scala> val msg2: java.lang.String = "Hello again, world!"
msg2: String = Hello again, world!
```

Or since `java.lang` types are visible with their simple names in Scala programs, simply:

```
scala> val msg3: String = "Hello yet again, world!"
msg3: String = Hello yet again, world!
```

## Step 3: Define Some Functions

```
scala> def max(x: Int, y: Int): Int = {
     | if (x > y) x
     | else y
     | }
max: (x: Int, y: Int)Int
```

Functions definitions start with `def`. A type annotation must follow every function parameter, because 
Scala compiler does not infer function parameter types. After the parameters list, you have the result type
of the max function.

```
scala> def greet() = println("Hello, world!")
greet: ()Unit
```

The function `greet()` doesn't return any interesting value. `Unit` is `greet` result's type, which 
indicates the function returns no interesting value. Scala's `Unit` type is similar to Java's `void` type.

```
scala> :quit
```

To exit Scala's interpreter.
