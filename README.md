# JavaScript Programing Questions By Abhishek Goyal

> \_Click &#9733; if you like the project. Your contributions are heartily ♡ welcome.

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
* [Miscellaneous](#-18-miscellaneous) -->

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
```

In the above program, the calculateFactorial function takes a number as an
argument and calculates its factorial.
If the number is 0 or 1, the factorial is 1.
Otherwise, a for loop is used to iterate from 2 to the given number, multiplying
each number to the factorial variable.
The final factorial value is returned.

You can test the program by calling the calculateFactorial function with different
numbers.
In the example above, it is called with 5 and 0, and it returns the factorial values
of 120 and 1, respectively.

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

## Q 4. **_Swap two numbers_** without using third variable.

```js
function swapNumbers(a, b) {
  a = a + b;
  b = a - b;
  a = a - b;
  return [a, b];
}

// Example usage:
let x = 10;
let y = 5;
console.log("Before swapping: x =", x, "and y =", y);
[x, y] = swapNumbers(x, y);
console.log("After swapping: x =", x, "and y =", y);
```

In the above function, the swapNumbers function takes two numbers a and b as arguments.
The swapping is done using arithmetic operations without using a third variable.

We first assign a + b to a. This step stores the sum of the two numbers in a.
We then assign a - b to b. This step stores the original value of a in b.
Finally, we assign a - b to a. This step stores the original value of b in a.
After calling the swapNumbers function, the values of x and y will be swapped.
In the example above, the initial values are x = 10 and y = 5. After swapping,
the values become x = 5 and y = 10.

<br/>

## Q 5. How to check the given number is **_Positive or Negative_** in JavaScript?

```js
function checkPositiveNegative(number) {
  if (number > 0) {
    return "Positive";
  } else if (number < 0) {
    return "Negative";
  } else {
    return "Zero";
  }
}

// Example usage:
console.log(checkPositiveNegative(5)); // Output: Positive
console.log(checkPositiveNegative(-7)); // Output: Negative
console.log(checkPositiveNegative(0)); // Output: Zero
```

In the checkPositiveNegative function, the number is compared to 0 using the
greater than (>) and less than (<) operators.
If the number is greater than 0, it is considered positive. If the number is
less than 0, it is considered negative.
If the number is equal to 0, it is considered zero. The corresponding string
is returned based on the comparison result.

You can call the checkPositiveNegative function with different numbers to test
whether they are positive, negative, or zero.
In the example above, it is called with the numbers 5, -7, and 0, and it returns
the corresponding results.

<br/>

## Q 6. Write a JavaScript Program to find whether given number is **_Leap year or NOT_**?

```js
function isLeapYear(year) {
  if ((year % 4 === 0 && year % 100 !== 0) || year % 400 === 0) {
    return "Leap year";
  } else {
    return "Not a leap year";
  }
}

// Example usage:
console.log(isLeapYear(2020)); // Output: Leap year
console.log(isLeapYear(2021)); // Output: Not a leap year
console.log(isLeapYear(2000)); // Output: Leap year
console.log(isLeapYear(1900)); // Output: Not a leap year
```

In the above program, the isLeapYear function takes a year as an argument.

It checks two conditions to determine whether the year is a leap year:

1. If the year is divisible by 4 and not divisible by 100, it is a leap year.
2. If the year is divisible by 400, it is also a leap year.

If either of these conditions is satisfied, the function returns "Leap year".
Otherwise, it returns "Not a leap year".

<br/>

## Q 7. Write a JavaScript Program to find whether given number is **_Leap year or NOT_**?

```js
function isLeapYear(year) = > year % 4 === 0;

// Example usage:
console.log(isLeapYear(2020));  // Output: true
console.log(isLeapYear(2021));  // Output: false
console.log(isLeapYear(2000));  // Output: true
console.log(isLeapYear(1900));  // Output: false

```

<br/>

## Q 8. Write a JavaScript Program to Print 1 To 10 Without Using Loop.

```js
function isLeapYear(year) {
  return new Date(year, 1, 29).getDate() === 29;
}

// Example usage:
console.log(isLeapYear(2020)); // Output: true
console.log(isLeapYear(2021)); // Output: false
console.log(isLeapYear(2000)); // Output: true
console.log(isLeapYear(1900)); // Output: false
```

In this program, the printNumbers function takes a number n as an argument.
It uses a recursive approach to print the current number and then calls
itself with the next number (n + 1) until n reaches 10.

By initially calling the printNumbers function with the starting number 1,
it will recursively print the numbers from 1 to 10 without using a loop.

When you run this program, it will output the numbers 1 to 10 in the
console without explicitly using a loop construct.

<br/>

## Q 9. Write a Java Program to print the **_digits of a Given Number_**.

```js
function printDigits(number) {
  if (number < 10) {
    console.log(number);
  } else {
    printDigits(Math.floor(number / 10));
    console.log(number % 10);
  }
}

// Example usage:
printDigits(12345);

// Each digit of the given number will be printed on a separate line.

1;
2;
3;
4;
5;
```

In this program, the printDigits function takes a number as an argument.
It uses a recursive approach to print the digits of the number.

The function first checks if the number is less than 10. If so, it directly
prints the number as it is a single-digit number.

If the number is greater than or equal to 10, it divides the number by 10 using
Math.floor(number / 10) to remove the rightmost digit. It then calls
printDigits recursively with the truncated number to print the remaining digits.

After the recursive call, it uses number % 10 to extract and print the rightmost
digit.

By calling the printDigits function with a given number, it will print each
digit of the number on separate lines.
