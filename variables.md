## Variables Notes

A Variable is a "named storage" for data. Variables are used to store this information.

```
Syntax:
let message;
message = 'Hello'; // store the string 'Hello' in the variables named message.

**Declaring twice triggers an error**

let message = "This";

// repeated 'let' leads to an error
let message = "That"; // SyntaxError: 'message' has already been declared

```

## Variable naming

There are two limitations on variable names in JavaScript:

- The name must contain only letters,digits,or the symbols **$** and **\_**.

- The first character must not be a digit.

```
let userName;
let test123;
```

When the name contains multiple words, camelCase is commonly used.

```
the dollar **$** and the **_** can also be used in names. They are like regular symbols,just like letters, without any special meaning.

let $ = 1; //declared a variable with the name $
let _ = 2; // and now a variable with the name _

Incorrect variable name

let 1a; // cannot start with digit
let my-name //hyphens '-' aren't allowed in the name
```

While declaring variables we can't use reserved keywords as name convention

## Constants

To declare a constant (unchanging) variable,use **const** instead of **let**:

```
Syntax:
const API = "https://www.dummyjson.com";
```

## Uppercase constants

There is a widespread practice to use constants as aliases for difficult-to-remember values that are known before execution.

Such constants are named using capital letters and underscores.

```
Example:
const COLOR_RED = "#F00";
const COLOR_GREEN = "#0F0";
const COLOR_BLUE = "#00F";
const COLOR_ORANGE = "#FF7F00";
```

## var,let,const

**var**: Variables declared with **var** can have global or local scope.Global scope is for variables declared outside functions, while local scope is for variables declared inside functions.

```
Global Scope Example:

var number = 50;

function print() {
    var square = number * number
    console.log(square)
}

console.log(number) // 50

print() //2500

```

the number variable has a global scope - it's declared outside functions
in the global space - so you can access it everywhere (inside or outside functions).

```
Local scope example:

function print(){
    var number = 50
    var square = number * number
    console.log(square)
}
print() //2500

console.log(number) // ReferenceError: number is not defined

```

## How to redeclare and reassign variables declared with var

Variables declared with var can be redeclared and reassigned.

```
Example:
var number = 50
console.log(number) // 50

number = 100
console.log(number) // 100

number = 200
console.log(number) // 200
```

## Var Hoisting

Variables declared with var are hoisted to the top of their global or local scope,Which make them accessible before the line they are declared.

```
console.log(number) // undefined
var number = 50
console.log(number) // 50
```

Variable is hoisted with a default value of undefined.

## Local Scope Example

```
function print() {
    var square1 = number * number;
    console.log(square1)

    var number = 50

    var square2 = number * number;
    console.log(square2);
}
print()
//Nan
//2500
```

**let**: Variables declared with **let** can be reassigned to other values, but they cannot be redeclared.
