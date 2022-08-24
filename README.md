# Comments

## Learning Goals

- Define what comments are in Java
- Discuss javadocs and their purpose

## Introduction

Let's face it - code isn't always the easiest to read. That's why we're in this
course together! To learn how to code! But even though we may be learning how
to read code, it would be nice for someone to explain in plain text what the
code may be doing.

This is why comments were invented.

## What are comments?

**Comments** are statements in Java that are not executed by the compiler and
the interpreter. These statements tend to make the code simpler to read and
understand, which in turn make the code easier to maintain and look for
potential errors.

We can add comments to our code in a couple of different ways:

1. We can add a single-line comment using two forward slashes (`//`).
2. We can add a multi-line comment using a combination of forward slashes and
asterisks (`/* This is a comment */`).
3. We can add a documentation comment using javadocs and annotations.

Let's look at these types of comments in more detail.

## Single-Line Comment

A **single-line comment** is a comment with only one line of code.
This may be used to quickly state something about the code in context.
The syntax for a single-line comment always starts with two forward slashes
(`//`) and is followed by text. Any text in front of the slashes will be
compiled and interpreted.

```java
// This is a comment in Java!
```

Let's see how this might be more helpful by looking back at our `SimpleSample`
class.

```java
public class SimpleSample {
    // Enter the main method
    public static void main(String[] args) {
        System.out.println("Hello World");    // Print "Hello World" to the console
    }
}
```

Notice how we have a single-line comment on its own line and another
comment inline with executable code. Both of these are valid examples of how
we may use the single-line comment. Again, the
`System.out.println("Hello World")` expression will be executed because it is
before the forward slashes.

## Multi-Line Comments

A **multi-line comment** is a comment that spans multiple lines of code.
This might be used to explain or elaborate on a particular complex code snippet.
The syntax for a multi-line comment always starts with a forward slash followed
by an asterisk (`/*`) and then closed with an asterisk followed by a forward
slash (`*/`). The text will lay between the `/*` and `*/` and will not be
compiled or interpreted.

```java
/* This is a 
   comment
   in Java!     
 */
```

Let's apply this to some code for context by looking at an implementation of the
`SimpleSample` class.

```java
public class SimpleSample {
    public static void main(String[] args) {
        /* We want to print out a message to the user
           so, we print out the message "Hello World" */
        System.out.println("Hello World");
    }
}
```

Multi-line comments are also helpful if we want to possibly comment out code.
We may comment out code to isolate a block of it to test or look for any
errors.

```java
public class SimpleSample {
    public static void main(String[] args) {
        /* Commenting out this line so we can print a different message
        System.out.println("Hello World");
         */
        
        System.out.println("I hope you are well today!");
    }
}
```

## Documentation Comments

**Documentation comments** are comments that embed information about the code
into the program itself. This is a way for programmers to clearly communicate
and document their code in a readable format. It uses a similar syntax to
multi-line comments. Documentation comments start with a forward slash
followed by two asterisks (`/**`) and are closed with an asterisk followed by
a forward slash (`*/`). The text will lay between the `/**` and `*/` and each
new line of text will start with a space and an asterisk (`*`).

Documentation comments also make use of the javadoc utility. **javadocs** are
tags or annotations that help extract the information and put it into an HTML
file. Consider the table of javadoc tags below:

![javadoc annotations](https://curriculum-content.s3.amazonaws.com/java-mod-1/comments/Javadoc-Annotations.png)

[Reference: Java, A Beginner's Guide, 5th Edition](https://www.oreilly.com/library/view/java-a-beginners/9780071606325/appblev1sec1.html)

Annotations that start with the at-symbol (@) are called **block tags** or
**stand-alone tags** and must be at the beginning of a documentation comment
line. Annotations surrounded by curly-braces ({@code}) are **inline tags** to
be used in a larger description. We will see some of these tags used more than
others, but it is good to keep this chart handy in case we ever get our hands
on the Oracle Java documentation - that is the documentation for the Java
programming language. That documentation makes use of these annotations quite
frequently.

Let's look at our `SimpleSample` class again and apply some documentation
comments.

```java
/**
 * This class is a simple class that prints
 * a sample message to the console.
 * @author Flatiron School
 * @version 1.0
 */
public class SimpleSample {
    
    /**
     * Main method for the class to be made "runnable"
     * @param args : String[] - array of arguments
     */
    public static void main(String[] args) {
        System.out.println("Hello World");
    }
}
```

Note that we started the documentation comments with a main description of the
class or method to follow. Documentation comments will more likely be attached
to classes and methods rather than individual variables themselves.

## Resources

[Java, A Beginner's Guide, 5th Edition](https://www.oreilly.com/library/view/java-a-beginners/9780071606325/appblev1sec1.html)
