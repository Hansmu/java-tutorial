# Introduction

Java is a language, which uses the JVM (Java Virtual Machine) to run code.

The written Java code is compiled into bytecode(.class files) by the Java compiler (javac).
Not directly into machine code (as opposed to C, for example).

The bytecode runs on the JVM (Java Virtual Machine),
which interprets or JIT-compiles it into native instructions at runtime.

This makes it platform independent.

## JIT - just in time compilation

When you compile a Java program (.java → .class), you don't get native machine code.
You get bytecode - a portable, intermediate representation that runs on the JVM.

At runtime, the JVM can execute this bytecode in two main ways:

Interpretation: Execute bytecode line by line (slow but flexible).

JIT Compilation: Convert frequently used bytecode into native machine code (fast).

The JVM uses both — that's what makes it “just-in-time.”

### How It Works

1. You start a Java program → JVM begins interpreting bytecode.

2. The JVM monitors performance and identifies “hot” methods — methods that are run many times.

3. These “hot spots” are compiled to native machine code by the JIT compiler.

4. Next time those methods run, the JVM executes the native code directly — much faster than interpretation.

That’s why Java programs often get faster after running for a while — the JVM is optimizing on the fly.

## JShell

Since version 9, Java ships with JShell (Java Shell Tool), which is a REPL.

JShell imports some libraries by default from Java.

## Binaries

There used to be two distributions that were available:
* JRE - Java Runtime Environment
  * Included:
    * JVM (Java Virtual Machine)
    * Core libraries
    * Supporting files
  * It had no compiler (javac), so you couldn't compile .java files.
  * Intended for end users
* JDK - Java Development Kit
  * Included:
    * Everything in the JRE
    * Development tools (like javac, javadoc, jar, etc).
  * Intended for developers

Since Java 11, it's no longer the case, now you only need a JDK.