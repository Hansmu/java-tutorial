# Variables

There are primitives and objects in Java.

Everything that is not a primitive is an object.

```java
int myFirstNumber = 5;
boolean someVal = false;
char letter = 'a';
```

In order to improve readability of large numbers, you can separate sections using an underscore.
````java
int someNumber = 10_000;
````

For numbers, Java, by default, uses int. If you want a long value, you need to add a suffix of `l` or `L`.
Preferably capital, as it's more readable with different fonts.
Situations where you would need this is if you're assigning a value to the long, which exceeds the allowed int size.

```java
long someLong = 2_147_483_648; // Errors
long someLong = 2_147_483_648L; // Works
```

If you want to cast a number, then you can add the type in the parenthesis.

````java
int someValue = 128;
byte thing = (byte)(someValue / 2); // Without the casting it'd error, as Java isn't sure if the value could fit
````

The double is the default type for any decimal in Java.

If you want to specify that something is a float, then you can add f/F to the end.

If you need to guarantee precise calculations, then you should use BigDecimal.

A string could be defined with:
```java
String myString = "This is a string";
```