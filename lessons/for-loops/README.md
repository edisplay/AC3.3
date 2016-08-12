- title: For Loops
- tags: loops, for, strings

# Objectives

- Understand the components of a for loop
- Properly use 'continue' and 'break'
- Iterate through a String using a standard loop

# Resources

[Oracle Docs](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/for.html)
[Java For-Loops Examples](http://www.java-examples.com/loop)


# Lecture

Loops are another power control structure, and a great way for your program to do a repeated set of actions.

A for loop has three important components that help determine how many times it will loop.

- Initialization
- Termination/Condition
- Increment

```java
for (initialization; termination; increment) {
    // do something
}
```


1. The *initialization* is executed once, beginning the loop.
2. When the *termination* expression is `false`, the loop terminates; this is analogous to the condition in a `while` statement. i.e, the condition must remain true for the loop to continue.
3. The *increment* expression is executed after each iteration; this can also decrement.

As with `if` and `while`, for loops have a body denoted by a pair of opening and closing braces.

All loops have a body, and any code within the body of your loop will run however many times your loop runs.

**Exercise** Rewrite the following `while` loop as a `for` loop:
 ```java
 int i = 0;
 while (i <= 100) {
     i++;
     System.out.println(i);
 }
```
- Loops include conditional logic.
- You may also need to add an if-statement to the body of your loop.




The hardest part about `for` loops is properly stopping the loop. Programmers often make mistakes when setting the termination condition for a loop. In particular, we are often off-by-one. This kind of bug it so common, it has its own [Wikipedia page](http://en.wikipedia.org/wiki/Off-by-one_error).



> **Exercise:** [Counting Machine](http://programmingbydoing.com/a/counting-machine.html): Write a program that counts from 0 to a user-specified number.


> **Exercise:** [harder] [Counting Machine Revisited](http://programmingbydoing.com/a/counting-machine-revisited.html): Now let the user input the initial value, the max value, and the increment.

> **Exercise:** "FizzBuzz" is a very famous program, up there with "Hello World!". Write [FizzBuzz](http://programmingbydoing.com/a/fizzbuzz.html) using a `for` loop.



`break` and `continue`
=

Remember `break`?

> *Definition:* `break` terminates a loop or switch statement and transfers execution to the statement immediately following the loop or switch.

Java also has another useful keyword, `continue`:

> *Definition:* `continue` jumps to the next iteration of the loop.

`continue` can be useful for skipping over some unnecessary computation.

A continue statement causes the loop to skip the remainder of its body and immediately retest its condition prior to reiterating.

```java
for (int i = 1; i <= 20; i++) {
    if (i % 2 == 0) continue;
    System.out.println(i);
}
```


> **Exercise:** Simplify your code for FizzBuzz using `continue`.

Iterating over strings
-

Often, programmers need to iterate over text. Java provides two functions, `String.length()` and `String.charAt()` that make iterating over a `String` fun. Here is how to use them:

```java
System.out.println("Queens!".length()); // 7
```

The function `String.charAt()` returns the `char` at the index provided. For example:

```java
System.out.println("Queens!".charAt(3)); // e
```


> **In-class assignment:** [String exercise](string-loops.md)



> **In-class assignment:** [hard] Below is a quote from [Grace Hopper](http://en.wikipedia.org/wiki/Grace_Hopper), the inventor of the first compiler. Write a program that uses a `for` loop to count how many times she says the word "data". You'll need to call two `String` functions in order to complete this assignment. Make sure to verify your answer.

> > "We must include in any language with which we hope to describe complex **data**-processing situations the capability for describing **data**. We must also include a mechanism for determining the priorities to be applied to the **data**. These priorities are not fixed and are indicated in many cases by the **data**.

> > "Thus we must have a language and a structure that will take care of the **data** descriptions and priorities, as well as the operations we wish to perform. If we think seriously about these problems, we find that we cannot work with procedures alone, since they are sequential. We need to define the problem instead of the procedures. The Language Structures Group of the Codasyl Committee has been studying the structure of languages that can be used to describe **data**-processing problems. The Group started out by trying to design a language for stating procedures, but soon discovered that what was really required was a description of the **data** and a statement of the relationships between the **data** sets. The Group has since begun writing an algebra of processes, the background for a theory of **data** processing.

> > "Clearly, we must break away from the sequential and not limit the computers. We must state definitions and provide for priorities and descriptions of **data**. We must state relationships, not procedures."

### [Exit Ticket](http://bit.ly/2aFLSKE)
