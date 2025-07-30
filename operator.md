# Operators

## unary,binary,operand

- `An operand` - is what operators are applied to. For instance `5*2` there are two operands: the left operand is `5` and the right operand is `2`.

- An Operator is unary if it has a single operand. the unary negation `-` reverses the sign of a number:

```
let x = 1;
x = -x;
console.log(x) // -1, unary negation was applied
```

- An Operator is binary if it has two operands. The same minus exists in binary form as well:

```
let x = `, y=3;
console.log(y - x); // 2, binary minus subtracts values
```

## Types of JavaScript Operators

There are different types of JavaScript Operators:

1. Arithmetic Operators
2. Assignment Operators
3. Comparison Operators
4. String Operators
5. Logical Operators
6. Bitwise Operators
7. Ternary Operators
8. Type Operators

### JavaScript Arithmetic Operators

Arithmetic Operators are used to perform arithmetic on numbers:

```
Arithmetic Operators Example
let a = 3;
let x = (100 + 50 ) * a;
```

**Maths Operations that can be performed**

1. Addition +
2. Subtraction -
3. Multiplication \*
4. Division /
5. Remainder %
6. Exponentiation \*\*

## String concatenation with binary +

If the binary + is applied to strings, it merges(concatenates)them:

```
let s = "my" + "string";
console.log(s) // my string
```

If any of the operand is a string, then the other one is converted to a string too.

```
console.log('1' + 2) //12
console.log(2 + 2 + '1'); // "41" and not "221"
```

## Numeric Conversion, Unary +

The unary plus or, in other words, the plus operator + applied to a single value, doesn't do anything to numbers. But if the operand is not a number, the unary plus converts it into a number.

```
let x = 1;
console.log(+x); //1

let y = -2;
console.log(+y); // -2

//Converts non-numbers
console.log(+true); //1
console.log(+ ""); //0
```

## Assignment

Let's note that an assignment = is also an operator. It is listed in the precedence table with the very low priority of 2.

That's why, when we assign a variable, like x = 2 \* 2 + 1, the calculations are done first and then the = is evaluated, storing the result in `x`.

```
let x = 2 * 2 + 1;
console.log(x);
```

## Increment/decrement

Increasing or decreasing a number by one is among the most common numerical operations.

- Increment ++ increase a variable by 1;
- Decrement -- decrease a variable by 1;

```
let counter = 2;
counter--;           // works the same as counter = counter - 1, but is shorter
console.log(counter); // 1
```

## Bitwise Operators

- AND (&)
- OR (|)
- XOR (^)
- NOT (~)
- LEFT SHIFT (<<)
- RIGHT SHIFT (>>)
- ZERO-FILL RIGHT SHIFT(>>>)


