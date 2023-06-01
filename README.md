# JavaScript Programing Questions By Abhishek Goyal

> _Click &#9733; if you like the project. Your contributions are heartily ♡ welcome._

<br/>

<!-- ## Table of Contents

<!--
* [Introduction](#-1-introduction)
* [Variables](#-2-variables)
* [Data types](#-3-data-types)
* [Operators](#-4-operators)
* [Numbers](#-5-numbers)
* [String](#-6-string)
* [Array](#-7-array)
* [Regular Expression](#-8-regular-expression)
* [Functions](#-9-functions)
* [Events](#-10-events)
* [Objects](#-11-objects)
* [Window and Document Object](#-12-window-and-document-object)
* [Classes](#-13-classes)
* [Error Handling](#-14-error-handling)
* [Promises](#-15-promises)
* [Collections](#-16-collections)
* [Modules](#-17-modules)
* [Miscellaneous](#-18-miscellaneous) --> -->

<br/>

# Basic Programs

<br/>

## Q 1. Check the given number is **_EVEN or ODD_**.

```js
function checkEvenOrOdd(number) {
  if (number % 2 === 0) {
    return "Even";
  } else {
    return "Odd";
  }
}
//Example usage:
console.log(checkEvenOrOdd(4)); // Output: Even
console.log(checkEvenOrOdd(7)); // Output: Odd
```

<br/>

## Q 2. Check the given number is **_EVEN or ODD_**.

```js
function calculateFactorial(number) {
  if (number === 0 || number === 1) {
    return 1;
  } else {
    let factorial = 1;
    for (let i = 2; i <= number; i++) {
      factorial *= i;
    }
    return factorial;
  }
}
//Example usage:
console.log(calculateFactorial(5)); // Output: 120
console.log(calculateFactorial(0)); // Output: 1

/* In the above program, the calculateFactorial function takes a number as an argument and calculates its factorial. If the number is 0 or 1, the factorial is 1. Otherwise, a for loop is used to iterate from 2 to the given number, multiplying each number to the factorial variable. The final factorial value is returned.

 You can test the program by calling the calculateFactorial function with different numbers. In the example above, it is called with 5 and 0, and it returns the factorial values of 120 and 1, respectively.
*/
```

<br/>

## Q 3. Find the **_Factorial_** of a number using **_Recursion_** .

```js
function calculateFactorialRecursive(number) {
  if (number === 0 || number === 1) {
    return 1;
  } else {
    return number * calculateFactorialRecursive(number - 1);
  }
}

// Example usage:
console.log(calculateFactorialRecursive(5)); // Output: 120
console.log(calculateFactorialRecursive(0)); // Output: 1

/*
 Factorial Using Recursion

 In mathematics, the factorial of a positive integer n,
 denoted by n!, is the product of all positive integers
 less than or equal to n:

  n! can be written as
  n! = 1 * 2 * 3 * .... * (n-1) * n;

  n! can also be written as
  n! = n * (n-1)!
  This approach helps to calculate using Recursion

  5! = 5 * 4!
  4! = 4 * 3!
  3! = 3 * 2!
  2! = 2 * 1!
  1! = 1

 */
```

<br/>

## Q 4. **_Swap two numbers_** without using third variable approach.

```js
function calculateFactorialRecursive(number) {
  if (number === 0 || number === 1) {
    return 1;
  } else {
    return number * calculateFactorialRecursive(number - 1);
  }
}

// Example usage:
console.log(calculateFactorialRecursive(5)); // Output: 120
console.log(calculateFactorialRecursive(0)); // Output: 1
```
