# Functions

## Function Declaration

To create a function we can use a function declaration.

```
Syntax:
function showMessage() {
    console.log('Hello World!');
}

function name(parameter1,parameter2,...parameterN) {
    //body
}

showMessage() // Calling a function
```

## Local variables

A variable declared inside a function is only visible inside that function.

```
function showMessage() {
    let message = "Hello, World" // local variable;

    console.log(message)
}

showMessage(); // Hello, World

console.log(message); // <--- Error! The variable is local to the function
```

## Outer variable

A function can access an outer variables as well, for example

```
let userName = "John";

function showMessage() {
    let message = 'Hello, ' + userName;
    console.log(message);
}

showMessage(); // Hello, John
```

The function has full access to the outer variable, It can modify as well.

```
let userName = 'John';

function showMessage() {
  userName = "Bob"; // (1) changed the outer variable

  let message = 'Hello, ' + userName;
  alert(message);
}

alert( userName ); // John before the function call

showMessage();

alert( userName ); // Bob, the value was modified by the function
```

The Outer variable is only used if there's no local one.

if a same-name variable is declared inside the function then it shadows the outer one. For instance, in the code below the functions uses the local `userName`. The outer one is ignored.

```
let userName = 'John';

function showMessage() {
  let userName = "Bob"; // declare a local variable

  let message = 'Hello, ' + userName; // Bob
  alert(message);
}

// the function will create and use its own userName
showMessage();

alert( userName ); // John, unchanged, the function did not access the outer variable
```

## Parameters

We can pass arbitrary data to functions using parameters.
In the example below, the functions has two parameter `from` and `text`.

```
function showMessage(from,text) { // parameters: from,text

console.log(from + ': ' + text);
}

showMessage('Ann', 'Hello!'); // Ann: Hello! (*)
showMessage('Ann', "What's up?"); // Ann: What's up? (**)
```

When a value is passed as a function parameter, it's also called argument.

- A parameter is the variable listed inside the parentheses in the function declaration (it's a declaration time term).
- An argument is the value that is passed to the function when it is called (it's a call time term).

## Default values

If a function is called, but an argument is not provided, then the corresponding value become `undefined`.

```
function showMessage(from, text = "no text given") {
  alert( from + ": " + text );
}

showMessage("Ann"); // Ann: no text given
```

## Returning a value

A function can return a value back into the calling code as the result.
The simplest example would be a function that sum two values

```
function sum(a,b) {
    return a + b;
}

let result = sum(1,2);
console.log(result); // 3
```

` A function with an empty return or without it returns undefined`

if a function does not return a value, it is the same as if it returns undefined:

```
function doNothing() { /* empty */}

console.log(doNothing() === undefined); // true
```

## Functions == Comments

Functions should be short and do exactly one thing. If that thing is big,maybe it's worth it to split the function into a few smaller functions. Sometimes following this rule may not be that easy, but it's definitely a good thing.
A separate function is not only easier to test and debug - its very existence is a great comment!

```
function showPrimes(n) {

  for (let i = 2; i < n; i++) {
    if (!isPrime(i)) continue;

    alert(i);  // a prime
  }
}

function isPrime(n) {
  for (let i = 2; i < n; i++) {
    if ( n % i == 0) return false;
  }
  return true;
}
```
