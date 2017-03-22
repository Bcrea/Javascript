# Basic Javascript

## Primitive types

* `strings` `numbers` `booleans` `null` and `undefined` everything else is an `object`.

## Boolean values

Boolean values are either `true` or `false`.

* Types of boolean values:

1. Falsy
  * null
  * undefined
  * 0
  * ""
  * false
2. Truthy
  * Anything else is truthy

Difference between `undefined` and `null`, `null` is intended to represent a value that is not there yet, while `undefined` is a value that hasn't been initialized, so we can set a variable to `null` if we intend to assign an object to it later on.

## Statements

Any expression, followed by a semicolon, is a statement.

```javascript
a;
var a = b;
console.log(a);
```

## expressions

An expression is an evaluation and is expected to give a value back.

```javascript
var a = 5;
var b = 5;
var sum = a + b;

if (a > b) {
	/*
	conditional statements here
	*/
}
```
There are different Operator expressions to perform actions on javascript:

* Arithmetic operators `+` `-` `*` `/`
* Assignment operator `=` 
* Logical operators `&&` for AND `||` for OR.
* comparison operators `==` (equality), `!=` (not equal), `<`(less than)
  `>` (greater than), `===` strict equality, `!==` (strict not equal).
* preincrement operator `++a` postincrement operator `a--`
* predecrement operator `--a` postdecrement operator `a--`

* preincrement operator: increments the value of the variable before using it `var ans = ++a;`if the value of a was 5, now it will be incremented to 6 before being assigned to ans.

## How to use operators

* The binary operator `+` can be used in arithmetic to add numbers together or to concatenate strings.

```javascript

var a = 5 + 5; // a stores the value 10
var myString = "Hello " + "World!"; // myString holds the string "Hello World!"
```
* when you sum a number with a string the number will be converted to a string because `+` is also a concatenation operator. `18 + "1500"` will be `"181500"`.

* when comparing a number string to a literal number using comparison operators the number string is treated as a literal number, or rather converted. `"20" > 18` this will be `true`.

* when comparing strings using `<` or `>` JS will look at each letter in the string to compare, so `"banana" < "mango"` banana is less than mango so the result is `true`, but javascript uses unicode characters to do the comparisons if the first letter is the same, javascript will look at the second letter.

* the binary operator `+` reads left-to-right, so the result of `1 + 2 + " hola"` will be `"3 hola"`.

* the unary operator `-` when used in a boolean value will turn `-true` into `-1`.

## Comparing different types

* When comparing different types, one will be converted to the other one so the comparison can be done.

```javascript

"1" == 1;
true // the string "1" is converted to a number and then compared to the other number.

"1" == true;
true // true will be converted to 1 (1 means true, 0 means false) and then compared.

"Hello" == 1;
false // The string gets converted into a number but the comparison can't be done because
    // Hello is not a number.
"true" == true;
false // this was hard for me at first, but it makes sense, true is converted to 1, and "true" is compared to 1, but it can't be compared so "true" is converted 
     //to a number and javascript tries to compare again but fails and the result is false.
```

`NaN`: stands for Not a Number, but it is actually a number that just can't be represented by the javascript interpreter, just like `null` is an object that is not there yet.

