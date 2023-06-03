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

## Q 2. Write a JavaScript Program to find the **_Factorial_** of given number.

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
for (let number = 1; number <= 10; number++) {
  console.log(number);
}

// Each digit of the given number will be printed on a separate line.

1;
2;
3;
4;
5;
6;
7;
8;
9;
10;
```

<br/>

## Q 9. Write a JavaScript Program to print the **_digits of a Given Number_**.

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
<br/>

## Q 9. Write a JavaScript Program to print all the **_Factors of the Given number_**.

```js
function printFactors(number) {
  console.log("Factors of", number + ":");
  for (let i = 1; i <= number; i++) {
    if (number % i === 0) {
      console.log(i);
    }
  }
}

// Example usage:
printFactors(24);

Factors of 24:
1
2
3
4
6
8
12
24

```

In this program, the printFactors function takes a number as an argument.
It uses a loop to iterate from 1 to the given number.

Inside the loop, it checks if the current number i is a factor of the given number.
This is done by checking if the remainder of dividing the given number by i is 0.
If the remainder is 0, it means i evenly divides the given number and is a factor.

If i is a factor, it is printed to the console using console.log.

By calling the printFactors function with a given number,
it will print all the factors of that number.

<br/>

## Q 10. Write a JavaScript Program to print all the **_Factors of the Given number_**.

```js
function sumOfDigits(number) {
  let sum = 0;
  while (number > 0) {
    sum += number % 10;
    number = Math.floor(number / 10);
  }
  return sum;
}

// Example usage:
console.log(sumOfDigits(12345)); // Output: 15
```

In this program, the sumOfDigits function takes a number as an argument.
It initializes a variable sum to store the sum of the digits, initially set to 0.

A while loop is used to iterate until the number becomes 0. In each iteration,
the remainder of dividing the number by 10 (number % 10) is added to the sum variable.
This extracts the rightmost digit of the number and adds it to the sum.

After adding the digit, the number is divided by 10 (number = Math.floor(number / 10)) to
remove the rightmost digit. This process continues until all the digits have been processed.

<br/>

## Q 11. Write a JavaScript Program to find **_sum of the digits of a given number_**.

```js
function findSmallest(a, b, c) {
  if (a <= b && a <= c) {
    return a;
  } else if (b <= a && b <= c) {
    return b;
  } else {
    return c;
  }
}

// Example usage:
console.log(findSmallest(4, 7, 2)); // Output: 2
console.log(findSmallest(9, 3, 5)); // Output: 3
console.log(findSmallest(1, 6, 8)); // Output: 1

//another Method

function findSmallest(a, b, c) {
  return Math.min(...arguments);
}

// Example usage:
console.log(findSmallest(4, 7, 2)); // Output: 2
console.log(findSmallest(9, 3, 5)); // Output: 3
console.log(findSmallest(1, 6, 8)); // Output: 1
```

In this program, the findSmallest function takes three numbers (a, b, and c) as
arguments. It uses a series of if and else statements to compare the numbers and
determine the smallest one.

The function checks the following conditions:

1. If a is less than or equal to both b and c, then a is the smallest number.
2. If b is less than or equal to both a and c, then b is the smallest number.
   Otherwise, c is the smallest number.

<br/>

In 2nd approach, the findSmallest function takes three numbers (a, b, and c) as
arguments. It uses the spread operator (...) along with the Math.min function to
find the smallest number among the arguments.

The spread operator ...arguments expands the three arguments into separate values,
which are then passed to the Math.min function. The Math.min function returns the
smallest value among the provided arguments.

By calling the findSmallest function with three numbers, it will return the smallest
number among them using the spread operator and the Math.min function.

This approach provides a concise way to find the smallest of three numbers without
the need for explicit comparisons using if or else statements.

<br/>

## Q 12. Write a javaScript program to **_Reverse a given number_**.

```js
function reverseNumber(number) {
  let reversed = 0;
  while (number !== 0) {
    reversed = reversed * 10 + (number % 10);
    number = Math.floor(number / 10);
  }
  return reversed;
}

// Example usage:
console.log(reverseNumber(12345)); // Output: 54321
console.log(reverseNumber(9876)); // Output: 6789
console.log(reverseNumber(100)); // Output: 1
```

In this program, the reverseNumber function takes a number as an argument.
It initializes a variable reversed to store the reversed number, initially set
to 0.

A while loop is used to iterate until the number becomes 0. In each iteration,
the rightmost digit of the number (number % 10) is extracted and added to the
reversed variable by multiplying it by 10 and then adding the digit.

After adding the digit, the number is divided by 10
(number = Math.floor(number / 10)) to remove the rightmost digit.
This process continues until all the digits have been processed.

<br/>

# Numbers

## Q1. Write a JavaScript Program to find GCD of two given numbers.

```js
/*
 * Find GCD of two numbers
 * GCD :: Greatest Common Divisor
 * The HCF or GCD of two numbers is the largest number
 * that can divide both numbers without reminder.
 *
 * Number a = 45 = 3 * 3 * 5
 * Number b = 75 = 3 * 5 * 5
 * GCD is = 3 * 5 = 15
 */

function findGCD(a, b) {
  while (b !== 0) {
    let temp = b;
    b = a % b;
    a = temp;
  }
  return a;
}

// Example usage:
console.log(findGCD(12, 18)); // Output: 6
console.log(findGCD(9, 28)); // Output: 1
console.log(findGCD(24, 36)); // Output: 12
```

In this program, the findGCD function takes two numbers (a and b) as arguments.
It uses the Euclidean algorithm to find the GCD of the two numbers.

The algorithm starts by initializing a temporary variable temp to store the value
of b. Then, b is updated with the remainder of dividing a by b using the modulo
operator (%). Finally, a is updated with the value stored in temp.

This process continues until b becomes zero, indicating that the GCD has been
found. At that point, the GCD is stored in a and returned.

<br/>

## Q2. Write a javaScript program to **_LCM of TWO given number_**.

```js
/*
 * 	LCM - Least Common Multiple
 *
 * The LCM of two integers is the smallest
 * positive integer that is perfectly divisible
 * by both the numbers without a reminder.
 * (means reminder should be zero)
 *
 * say n1 = 12 and n2 = 15
 * 12 & 15 can divide 60, 120, 180 ...
 * but the smallest number is 60
 * LCM of 12 & 15 is 60
 *
 * steps
 * 1. get the minimum of n1 & n2
 * 2. assume the maximum is LCM
 * 3. increment the lcm upto both n1 & n2
 * perfectly divides the LCM.
 *
 * n1 = 10 and n2 = 6
 * 10 and 6 can divide 30, 60, 90 ...
 * but the smallest number is 30
 * LCM of 10 & 6 is 30
 *
 */

function findLCM(a, b) {
  let max = Math.max(a, b);
  let lcm = max;

  while (true) {
    if (lcm % a === 0 && lcm % b === 0) {
      break;
    }
    lcm += max;
  }

  return lcm;
}

// Example usage:
console.log(findLCM(12, 18)); // Output: 36
console.log(findLCM(9, 28)); // Output: 252
console.log(findLCM(24, 36)); // Output: 72
```

In this program, the findLCM function takes two numbers (a and b) as arguments.
It starts by finding the maximum of the two numbers using the Math.max function
and assigns it to the variable max.

The initial value of the LCM is set to max. The program enters a while loop that
continues until the LCM is found.

Within each iteration, it checks if the LCM is divisible by both a and b using the
modulo operator (%). If it is, it means that the current LCM is the least common
multiple, and the loop is exited.

If the LCM is not divisible by both a and b, it is incremented by max. This
process continues until the LCM is found.

<br/>

## Q3. Write a javaScript program to **_LCM of TWO given number_** using Prime Factors method.

```js
/*
 * 	LCM - Least Common Multiple
 *
 * The LCM of two integers is the smallest
 * positive integer that is perfectly divisible
 * by both the numbers without a reminder.
 * (means reminder should be zero)
 *
 * say n1 = 12 and n2 = 15
 * 12 & 15 can divide 60, 120, 180 ...
 * but the smallest number is 60
 * LCM of 12 & 15 is 60
 *
 */

function findLCM(a, b) {
  // Find prime factors of both numbers
  const primeFactorsA = findPrimeFactors(a);
  const primeFactorsB = findPrimeFactors(b);

  // Merge prime factors from both numbers
  const allPrimeFactors = mergePrimeFactors(primeFactorsA, primeFactorsB);

  // Calculate LCM using prime factors
  let lcm = 1;
  for (const prime in allPrimeFactors) {
    lcm *= Math.pow(prime, allPrimeFactors[prime]);
  }

  return lcm;
}

function findPrimeFactors(num) {
  const primeFactors = {};

  for (let i = 2; i <= num; i++) {
    while (num % i === 0) {
      if (primeFactors[i]) {
        primeFactors[i]++;
      } else {
        primeFactors[i] = 1;
      }
      num /= i;
    }
  }

  return primeFactors;
}

function mergePrimeFactors(factorsA, factorsB) {
  const mergedFactors = { ...factorsA };

  for (const prime in factorsB) {
    if (mergedFactors[prime]) {
      mergedFactors[prime] = Math.max(mergedFactors[prime], factorsB[prime]);
    } else {
      mergedFactors[prime] = factorsB[prime];
    }
  }

  return mergedFactors;
}

// Example usage:
console.log(findLCM(12, 18)); // Output: 36
console.log(findLCM(9, 28)); // Output: 252
console.log(findLCM(24, 36)); // Output: 72
```

In this program, we have three functions:

1. The findLCM function takes two numbers (a and b) as arguments. It first finds the prime
   factors of both numbers using the findPrimeFactors function. Then it merges the prime
   factors using the mergePrimeFactors function.

2. The findPrimeFactors function takes a number (num) as an argument and returns an object
   containing the prime factors and their frequencies. It iterates from 2 up to the given
   number and checks if the number is divisible by the current iteration. If it is, it
   adds the prime factor to the object and reduces the number by dividing it. This process
   repeats until the number becomes 1.

3. The mergePrimeFactors function takes two prime factor objects (factorsA and factorsB)
   and merges them into a single object. It starts by creating a copy of factorsA. Then it
   iterates over the prime factors in factorsB and checks if they exist in the merged
   object. If they do, it updates the frequency to the maximum of the two. If they don't,
   it adds the prime factor to the merged object.

Finally, the findLCM function calculates the LCM by iterating over the merged prime
factors. It multiplies each prime factor raised to its corresponding frequency to
calculate the LCM.

<br/>

## Q 4. Check whether the **_Given Number_** is a **_Palindrome or NOT_**.

```js
/*
 * Palindrome Check
 *
 * Check the given number is Palinndrome Number or NOT
 *
 * A palindrome number is a number that remains the same when
 * its digits are reversed.
 *
 * Say N = 16461
 * reverse of N = 16461
 * N and reverse of N are same
 * So 16461 is Palindrome number
 *
 * Other examples are
 * 12321, 1001, 10101
 *
 * NOT a Palindrome
 * 100, 123, 2020
 *
 */

function isPalindrome(number) {
  const originalNumber = number;
  let reversedNumber = 0;

  while (number > 0) {
    const digit = number % 10;
    reversedNumber = reversedNumber * 10 + digit;
    number = Math.floor(number / 10);
  }

  if (originalNumber === reversedNumber) {
    return true;
  } else {
    return false;
  }
}

//Another method

function isPalindrome(number) {
  const str = number.toString();
  const reversedStr = str.split("").reverse().join("");

  return str === reversedStr;
}

// Example usage:
console.log(isPalindrome(12321)); // Output: true
console.log(isPalindrome(12345)); // Output: false
console.log(isPalindrome(1221)); // Output: true
console.log(isPalindrome(123)); // Output: false
console.log(isPalindrome("abccba")); // Output: true
console.log(isPalindrome("abc")); // Output: false
```

In this program, the isPalindrome function takes a number as an argument
and checks whether it is a palindrome.

First, we store the original number in a variable originalNumber for
comparison later. Then, we initialize reversedNumber to 0.

We use a while loop to reverse the number. In each iteration, we extract the
last digit of the number using the modulo operator (%) and add it to
reversedNumber after multiplying it by 10. Then, we update the number by
removing the last digit using integer division (Math.floor(number / 10)).

After the loop finishes, we compare originalNumber with reversedNumber. If
they are equal, it means the number is a palindrome, and the function returns
true. Otherwise, it returns false.

<br/>

## Q 5. Write a JavaScript Program to print all the **Prime Factors** of the Given Number.

```js
function printPrimeFactors(number) {
  let factor = 2;

  while (number > 1) {
    if (number % factor === 0) {
      console.log(factor);
      number /= factor;
    } else {
      factor++;
    }
  }
}

// Example usage:
printPrimeFactors(24); // Output: 2 2 2 3
printPrimeFactors(56); // Output: 2 2 2 7
printPrimeFactors(100); // Output: 2 2 5 5
printPrimeFactors(97); // Output: 97
```

1. The printPrimeFactors function takes a number as its parameter.
2. Inside the function, we initialize a variable factor to 2. This will be the
   first number we check for divisibility.
3. The while loop runs as long as number is greater than 1. The loop will continue
   until the number becomes 1, meaning we have divided out all the prime
   factors.
4. Inside the loop, we check if number is divisible evenly by the current factor
   using the modulo operator (%). If the remainder is 0, it means that factor is a
   prime factor of number.
5. If factor is a prime factor, we print it using console.log(factor). We also
   divide number by factor to reduce its value.
6. If factor is not a prime factor, we increment it by 1 and continue the loop to
   check the next number.
7. The loop continues until number becomes 1, at which point all the prime factors
   have been found and printed.

<br/>

## Q 6. Write a JavaScript Program to check whether the Given Number is **_Prime Number or NOT_**.

```js
function isPrime(number) {
  // Check if the number is less than 2
  if (number < 2) {
    return false;
  }

  // Check for divisibility from 2 to the square root of the number
  for (let i = 2; i <= Math.sqrt(number); i++) {
    if (number % i === 0) {
      return false;
    }
  }

  return true;
}

console.log(isPrime(17)); // Output: true
console.log(isPrime(28)); // Output: false
```

1. Check if the number is less than 2. If it is, then it is not a prime number,
   so we return false.
2. Iterate from 2 to the square root of the number. For each number i in this
   range, check if the number is divisible by i. If it is, then it is not a prime
   number, so we return false.
3. If the number is not divisible by any number in the range, it is a prime
   number, so we return true.

<br/>

## Q 7 . Write a JavaScript Program to print **_Prime Numbers from 1 to N_**.

```js
function isPrime(number) {
  if (number < 2) {
    return false;
  }

  for (let i = 2; i <= Math.sqrt(number); i++) {
    if (number % i === 0) {
      return false;
    }
  }

  return true;
}

function printPrimeNumbers(N) {
  for (let number = 2; number <= N; number++) {
    if (isPrime(number)) {
      console.log(number);
    }
  }
}

console.log(printPrimeNumbers(20));

// output
// 2
// 3
// 5
// 7
// 11
// 13
// 17
// 19
```

In this program, we have two functions. The first function, isPrime,
checks whether a given number is prime or not. It follows the same
logic as explained in the previous response about checking prime
numbers.

The second function, printPrimeNumbers, takes a number N as input and
prints all the prime numbers from 1 to N. It uses a for loop to
iterate from 2 to N. For each number in this range, it calls the
isPrime function to check if the number is prime. If it is, it is
printed using console.log().

In the example, the number N is set to 20 to test the function. You
can replace it with any other positive integer to print the prime
numbers from 1 to that number. The program will print the prime
numbers in the given range.

<br/>

## Q 8 . Write a Java Program to check whether the given number is **Armstrong Number** or NOT.

```js
/*
 * 	Armstrong Number
 *
 * A positive number is called Armstrong number
 * if it is equal to the
 * sum of cubes of its digits
 * for example 0, 1, 153, 370, 371, 407 etc.
 *
 * 153 = 1^3 + 5^3 + 3^3 = 1 + 125 + 27 = 153
 * 370 = 3^3 + 7^3 + 0^3 = 27 + 343 + 0 = 370
 * 371 = 3^3 + 7^3 + 1^3 = 27 + 343 + 1 = 371
 */

function isArmstrongNumber(number) {
  const digits = [];
  let temp = number;
  const numLength = number.toString().length;

  while (temp > 0) {
    const digit = temp % 10;
    digits.push(digit);
    temp = Math.floor(temp / 10);
  }

  const sum = digits.reduce((acc, curr) => acc + Math.pow(curr, numLength), 0);

  return sum === number;
}

// Test the function
const number = 153;
if (isArmstrongNumber(number)) {
  console.log(`${number} is an Armstrong number.`);
} else {
  console.log(`${number} is not an Armstrong number.`);
}

//Output
// 153 is an Armstrong number.
```

1. Convert the number to a string and determine the number of digits in
   the number by using the length property.
2. Initialize an empty array called digits to store the individual digits
   of the number.
3. Extract each digit from the number using the modulo operator (%) and
   divide the number by 10 in each iteration until the number becomes 0.
   Store the digits in the digits array.
4. Calculate the sum of each digit raised to the power of the number of
   digits using the reduce method.
5. Finally, check if the sum is equal to the original number. If it is,
   then the number is an Armstrong number.

<br/>

## Q 9 . Write a Java Program to check whether the given number is **Perfect Number** or NOT.

```js
/*
 * Perfect Number
 * ---------------
 * Perfect number is a positive integer that is
 * equal to the sum of its proper positive divisors,
 * that is, the sum of its positive divisors excluding
 * the number itself.
 *
 * Following are the examples of perfect number.
 * 6 = 1+2+3
 * 28= 1+2+4+7+14
 * 496= 1+2+4+8+16+31+62+124+248
 *
 */

function isPerfectNumber(number) {
  if (number <= 0) {
    return false;
  }

  let sum = 0;

  for (let i = 1; i < number; i++) {
    if (number % i === 0) {
      sum += i;
    }
  }

  return sum === number;
}

// Example usage
const number = 28;
if (isPerfectNumber(number)) {
  console.log(number + " is a perfect number.");
} else {
  console.log(number + " is not a perfect number.");
}
```

In this program, the isPerfectNumber function takes a number as input and
checks whether it is a perfect number or not. A perfect number is a
positive integer that is equal to the sum of its proper divisors
(excluding the number itself).

The function first checks if the number is less than or equal to 0, in
which case it immediately returns false. Then, it initializes a variable
sum to 0, which will be used to store the sum of the proper divisors.

The program uses a for loop to iterate through all the numbers from 1 to
number - 1. For each iteration, it checks if number is divisible by the
current number i. If it is, then i is a proper divisor, so it adds it to
the sum variable.

Finally, the function checks if the sum is equal to the number. If they
are equal, it means that the number is a perfect number, and the function
returns true. Otherwise, it returns false.

In the example usage, we check whether the number 28 is a perfect number
using the isPerfectNumber function and log the result to the console.

<br/>

## Q 10 . Write a Java Program to print **Perfect Numbers** between 1 to 1000.

```js
function isPerfectNumber(number) {
  if (number <= 0) {
    return false;
  }

  let sum = 0;

  for (let i = 1; i < number; i++) {
    if (number % i === 0) {
      sum += i;
    }
  }

  return sum === number;
}

function printPerfectNumbers(start, end) {
  console.log(`Perfect numbers between ${start} and ${end}:`);

  for (let i = start; i <= end; i++) {
    if (isPerfectNumber(i)) {
      console.log(i);
    }
  }
}

// Example usage
printPerfectNumbers(1, 1000);
```

In this program, we have the isPerfectNumber function, which we used in the previous
solution. It checks whether a given number is a perfect number or not.

The printPerfectNumbers function takes two arguments, start and end, which represent the
range of numbers to check for perfect numbers. It iterates through the numbers from start
to end and calls the isPerfectNumber function for each number. If the number is a perfect
number, it is printed to the console.

In the example usage, we call the printPerfectNumbers function with the arguments 1 and
1000 to print all the perfect numbers between 1 and 1000. The program outputs the perfect
numbers to the console.

# Array Based Programs
