# `if-else` Statements

We often refer to an `if` statement as a one-way selector, as it has only one direction to go: when the **boolean expression** is `true`. If it is `true`, it executes code, otherwise it skips it and moves on. A common question then, is why would we only select one-way, when there are two boolean options: `true` and `false`?

---

## `if-else` Statements

An **`if-else` statement** is commonly referred to as a **two-way selector**, as it will have two things to choose from: one when the boolean expression is `true`, and the other when the boolean expression is `false`. We might typically rephrase it as a sentence like "if this is `true`, then we will do `x`, otherwise, we will do `y`." In this exemplar sentence, `x` will happen *only* when the boolean expression is `true` and likewise `y` will happen *only* whent he boolean is `false`. This means our `if-else` statement will now skip some code no matter what: either it skips `x` when the expression is `false` or it skips `y` when the expression is `true`.

Here is an example of this in action from the `NotesIfElse1.java` file:

```java
int num = 10;

if (num > 15) {
    System.out.println(num + " is greater than 15.");
} else {
    System.out.println(num + " is less than or equal to 15.");
}
System.out.println("num is " + num + ".");
```

We can see the beginning portion of an `if-else` statement is just a regular `if` statement, except after we close the curly bracket, we use the keyword `else` and open another curly bracket to put the next section of code. The top section is for when `num > 15` is `true`, and the bottom portion (the `else` portion) is for when `num > 15` is `false`. In this case, we know that `10 > 15` is `false`, so we expect to run the bottom portion that should print `"10 is less than or equal to 15"`, and then exit the `if-else` statement and print `"num is 10"`. It produces the following output:

```
10 is less than or equal to 15.
num is 10.
```

It is important to consider why when we check if `num > 15` that the opposite would be `num <= 15` instead of `num < 15`. This comes down to options. If I told you the number I am thinking of is **not** greater than `15`, then you know that it could be any number less than `15`, or it could be `15` itself.

We could have produced this same code with just the `if` statements from Unit 3 Section 2, but it would have looked like this example from the `NotesIf1.java` file:

```java
int num = 10;

if (num > 15) {
    System.out.println(num + " is greater than 15.");
} 
if (num <= 15) {
    System.out.println(num + " is less than or equal to 15.");
}
System.out.println("num is " + num + ".");
```

This produces the same output, but notice that it takes a little more effort as we have to write a second boolean expression for the second `if` statement, instead of it being a part of one larger `if-else` statement.

---

## Assignment

Now that you have gone through the notes for this section, you can check out the `Try.md` and `Try.java` files to try a short assignment using this material.
