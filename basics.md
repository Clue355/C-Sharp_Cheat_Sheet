# C# Cheat Sheet

## Basics

Double Quotes (`"double-quotes"`) make your characters into a string literal meaning you literally wanted your
characters sent to the output.

This line of code below helps you output Hello World! to the terminal. It also appends a space at the end.

```C#
Console.WriteLine("Hello World!")
```

Ex output: `Hello World!`

This code is similar to the one above, but it does not append a space at the end. That is why Hello World! apears the
same in the example output

```C#
Console.Write("Hello ")
Console.Write("World!")
```

Ex output: `Hello World!`

Single quotes (`'single-quotes'`) create a character literal or a char data type. Which is a single character. if you
put more than one character in single quotes you would get an error saying there's too many characters in the character
literal

```C#
Console.WriteLine('b');
```

To display integer literals or integers also known as int. You don't need to have quotes

```C#
Console.WriteLine(123);
```

C# supports three data types to represent decimal numbers: float, double, and decimal

```C#
Float Type    Precision
----------------------------
float         ~6-9 digits
double        ~15-17 digits
decimal        28-29 digits
```

To create a float literal, append the letter F after the number. The F is called a literal suffix. The literal suffix
tells the compiler you wish to work with a value of float type. You can use either a lower-case f or upper-case F as the
literal suffix for a float. it's best to use this data type for fixed fractional values to avoid unexpected computation
errors.

```C#
Console.WriteLine(0.25F);
```

To create a double literal, just enter a decimal number. The compiler defaults to a double literal when a decimal number
is entered without a literal suffix.

```C#
Console.WriteLine(2.625);
```

To create a decimal literal, append the letter m after the number. The m is called a literal suffix. The literal suffix
tells the compiler you wish to work with a value of decimal type. You can use either a lower-case m or upper-case M as
the literal suffix for a decimal.

```C#
Console.WriteLine(12.39816m);
```

Boolean literals also known as bool use true and false. They can also represent 1 and 0

```C#
Console.WriteLine(true);
Console.WriteLine(false);
```

To declare a variable you must give it a data type and name. In this case, you're creating a new variable of type string
called firstName. From now on, this variable can only hold string values.

```C#
string firstName;
```

Here's a few important considerations about variable names:

-   Variable names can contain alphanumeric characters and the underscore character. Special characters like the hash
    symbol # (also known as the number symbol or pound symbol) or dollar symbol $ are not allowed.
-   Variable names must begin with an alphabetical letter or an underscore, not a number.
-   Variable names are case-sensitive, meaning that string Value; and string value; are two different variables.
-   Variable names must not be a C# keyword. For example, you cannot use the following variable declarations: decimal
    decimal; or string string;.

Here are some coding conventions for variables:

-   Variable names should use camel case, which is a style of writing that uses a lower-case letter at the beginning of
    the first word and an upper-case letter at the beginning of each subsequent word. For example, string
    thisIsCamelCase;.
-   Variable names should begin with an alphabetical letter. Developers use the underscore for a special purpose, so try
    to not use that for now.
-   Variable names should be descriptive and meaningful in your app. Choose a name for your variable that represents the
    kind of data it will hold.
-   Variable names should be one or more entire words appended together. Don't use contractions or abbreviations because
    the name of the variable (and therefore, its purpose) may be unclear to others who are reading your code.
-   Variable names shouldn't include the data type of the variable. You might see some advice to use a style like string
    strValue;. That advice is no longer current.

Examples of declarations:

```C#
char userOption;

int gameScore;

decimal particlesPerMillion;

bool processedCustomer;
```

Assigning a value is also referred to as "setting the variable", or simply, a "set" operation. You use singe equals to
assign a variable

> Note: you can't assign a int data type to a string. These data types are enforced and you will get an error.

```C#
string firstName;
firstName = "Bob";
```

This is how you would assign a variable and then retrieve it using the terminal. Retrieving a value from a variable is
also referred to as "getting the variable", or simply, a "get" operation. Getting a variable before setting it leads to
a error

```C#
string firstName;
firstName = "Bob";
Console.WriteLine(firstName);
```

You can reassign a variable as many times as you want as long as it's the same data type as when the variable was
initialized

```C#
string firstName;
firstName = "Bob";
Console.WriteLine(firstName);
firstName = "Liem";
Console.WriteLine(firstName);
firstName = "Isabella";
Console.WriteLine(firstName);
firstName = "Yasmin";
Console.WriteLine(firstName);
```

It's recommended that you set a variable as you declare one

```C#
string firstName = "Bob";
Console.WriteLine(firstName);
```

An implicitly typed local variable is created by using the var keyword followed by a variable initialization. The var
keyword tells the C# compiler that the data type is implied by the assigned value. After the type is implied, the
variable acts the same as if the actual data type had been used to declare it. The var keyword is used to save on
keystrokes when types are lengthy or when the type is obvious from the context.

```C#
var message = "Hello world!";
```

Declaring the variable this way sets any variable with the name message as a string. Reassigning this variable to a
decimal will cause an error

```C#
var message = "Hello World!";
message = 10.703m;
(2,11): error CS0029: Cannot implicitly convert type 'decimal' to 'string'
```

the var keyword is dependent on the value you use to initialize it. so it's important to give it a value otherwise you
get an error

```C#
var message;
(1,5): error CS0818: Implicitly-typed variables must be initialized
```
