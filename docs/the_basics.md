# The basics

## Variables

Variables in Orchid can be defined using `let` or `make`:

- `let`: Defines a variable with an implied type and requires an initial value.
  ```orchid
  let name = "Orchid";
  ```
- `make`: Defines a variable without an initial value but requires specifying the type.
  ```orchid
  make age as int;
  ```


## Functions

Functions in Orchid are defined using the start function syntax. Here is an example:

```orchid
start function sparklify takes (string input) gives (string)
define as {
    return "✨" + input + "✨";
} end
```

In this example we are defining a function called `sparklify`. It takes one string called `input` as parameter. And it can only ever return a string.

## Main function

Your orchid program will be ran from the `main` function. You don't have to write the entire start function syntax every time. The main function can be shortened to something like this:

```orchid
start main
define as {
    let sparked = sparklify("Hello, World!");
    print(sparked);
} end
```

This example combines the concepts of variables and functions and should output `✨Hello, World!✨`.

## If statements

In orchid, if statements run the function that they get (without any parameters).

Normally you would define that with a shorthand lambda function, which is just `then`. Here is an example:

```orchid
if (1 + 1 == 2) then {
    print("Yay!");
} end
```

That example is equivelant to this:

```orchid
if (1 + 1 == 2) start lambda define as {
    print("Yay!");
} end
```

However for example if you had a function called `doSomething`, this is how you could call it in an if statment:

```orchid
if (condition) doSomething;
```
