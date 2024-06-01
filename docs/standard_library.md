# Standard library

Any feature in the standard library that is used in your program will be directly compiled into your program at compile-time.

To use these features you don't need to import, include, or install anything.

Currently the standard library has these functions:

- [`print`](#print): Outputs something to the standard output
- [`typecheck`](): Check for a type

## print

`start function print takes (T content) gives ()`

Will print out something to the console.

`print` can take any type in its arguement(s).
`print` will not return any value.

\* please note that using any type is only available to functions in the standard library

## typecheck

`start function print takes (T variable) gives (type)`

Used to determine what type something is.

You can use it like this:

```orchid
if (typecheck("bleh") as string) then {
    print("correct!");
} end
```

Note the use of `as`, that is how you compare against a typecheck.

`print` can take any type in its arguement(s).
`print` will not return any value, it can only be checked against.

\* please note that using any type is only available to functions in the standard library
