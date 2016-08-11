- title: Classes II
- tags: wrapper classes, auto-boxing, static methods, exception handling

# Objectives
- To understand what wrapper classes are
- To become comfortable with the subject of auto-boxing and unboxing
- To understand about static methods of the Integer Class
- To understand what exception handling is and how to use it

# Lecture

## Wrapper classes 

A **wrapper class** wraps (encloses) around a data type and gives it an object appearance. Wherever the data type is required as an object, this object can be instead. Wrapper classes include methods to unwrap the object and give back the original data type. 

Instead of:

```java
Integer i = new Integer(9);
```

use this instead:

```java
Integer l = 9;
```

A primitive-wrapper class in the Java language is one of eight classes provided in the `java.lang package` to provide object methods for the eight primitive types. All of the primitive wrapper classes in Java are immutable. J2SE 5.0 introduced **auto-boxing** of primitive types into their wrapper object, and automatic **unboxing** of the wrapper objects into their primitive value — the implicit conversion between the wrapper objects and primitive values.


| Primitive type  | Wrapper Class | Constructor Arguments |
|---|---|---|
| `byte` | `Byte` | `byte` or `String` |
| `short` | `Short` | `short` or `String`	 |
| `int` | `Integer` | `int` or `String` |
| `long` | `Long` | `long` or `String` |
| `float` | `Float` | `float`, `double` or `String` |
| `double` | `Double` | `double` or `String` |
| `char` | `Character` | `char` |
| `boolean` | `Boolean` | `boolean` or `String` |


## Auto-boxing and unboxing

**Auto-boxing** is the term for getting a reference type out of a value type just through type conversion (either implicit or explicit). The compiler automatically supplies the extra source code which creates the object.

If we move in the opposite direction, then it's called **unboxing**.

![Autoboxing/unboxing](https://github.com/accesscode-2-1/unit-0/blob/master/images/AutoBoxing_UnBoxing.png)

##### Here are a couple of examples:

- Value passed as a parameter

```java
List<Integer> numbers = new ArrayList<Integer>();

numbers.add(5); // Although the add method asks for a parameter of type Integer, we can use 
                // the primitive 5 because it gets automatically auto-boxed into 
                // an object of type Integer implicitly.

numbers.add(6);

System.out.println(numbers.get(0)); // prints 5

System.out.println(numbers.get(1)); // prints 6
```

- Value passed to a variable

```java
Integer number = 13;
```


#### Why should you care? 
- Autoboxing/unboxing is heavily used in java collections. More on this later!


## Static methods

A **static method** is a method that belongs to a class, not an instance of the class.

You can call a static method directly on the class, for example:

```java
String.format("Formatting the number %d", 9);
```

#### A useful static method  of the Integer class:

```java
static int parseInt(String s) 
```

This method parses the string argument as a signed decimal integer.

The following will generate a compiler error:

```java
String strNum1 = "1000"; 
int val = strNum1;
System.out.println(val);
```

Output:
```java
java: incompatible types
required: int
found: java.lang.String
```

#### Instead use:

```java
// Outputs 1000
String strNum1 = "1000";     
int val = Integer.parseInt(strNum1);
System.out.println(val);
```

## Exception handling

```java
String strNum1 = "1000cats";
int val = Integer.parseInt(strNum1);
System.out.println(val);
```

Generates a NumberFormatException exception therefore you may wish to properly handle it:

```java
try{

   String strNum1 = "1000cats";
   int val = Integer.parseInt(strNum1);
   System.out.println(val);

} catch (NumberFormatException e){

   System.out.println("Not a proper integer value!");

}
```

Outputs: Not a proper integer value!

##### But at least the exception is handled and the program execution is able to continue.
