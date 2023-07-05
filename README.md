# JavaScript Programming Questions By Abhishek Goyal

<br/>
Preparing for a JavaScript interview can be a challenging task, as it requires a solid understanding of the language's concepts and techniques. To help you excel in your next interview, we have compiled a set of JavaScript programming questions commonly asked during technical assessments. Whether you're a beginner seeking an entry-level position or an experienced developer aiming for a senior role, these questions will assess your knowledge and problem-solving abilities. Let's dive into the world of JavaScript and equip yourself with the necessary tools to succeed.

</br>





</br>





In this Article, we will cover a range of topics, including **_Basic Programs, Numbers Based Programs, Array Based Programs, String Based Programs, Converters
Print the Series_**. Each question will be explained in a concise and clear manner, ensuring you grasp the core concepts and can confidently discuss them during your interview. Additionally, we'll provide sample code snippets and explanations to enhance your understanding and enable you to apply these concepts in real-world scenarios.

By familiarizing yourself with these JavaScript programming questions, you'll gain the confidence to tackle technical interviews and impress potential employers. Remember, the key to success lies in practice and continuous learning. So, let's embark on this journey together and sharpen your JavaScript skills for your next interview.



<br/>

### Table of Contents

- [Basic Programs](#Basic-Programs)
- [Numbers Based Programs](#Numbers-Based-Programs)
- [Array Based Programs](#Array-Based-Programs)
- [String Based Programs](#String-Based-Programs)
- [Converters](#Converters)
- [Print the Series](#Print-the-Series)
- [Special Function](#Problem-solved-using-special-Function)

<br/>

# Basic Programs

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 3. Find the **_Factorial_** of a number using **_Recursion_** .

```js
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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 10. Write a JavaScript Program to find **_sum of the digits of a given number_**.

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

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 11. Write a JavaScript Program to find the **_smallest of 3 numbers_** (a,b,c) without using < or > symbol?

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

<br/>

# Numbers Based Programs

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

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

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 8 . Write a JavaScript Program to check whether the given number is **Armstrong Number** or NOT.

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

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 9 . Write a JavaScript Program to check whether the given number is **Perfect Number** or NOT.

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

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 10 . Write a JavaScript Program to print **Perfect Numbers** between 1 to 1000.

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

**[⬆ Back to Top](#table-of-contents)**

<br/>

# Array Based Programs

## Q 1 . Write a JavaScript Program to print **Perfect Numbers** between 1 to 1000.

```js
/*
 * Calculate the Average of Given Array
 * -------------------------------------
 *
 * This is one basic program using array.
 * Steps
 * 1. Declare a variable sum with 0
 * 2. Iterate the array and add with sum variable
 * 3. Divide the sum with array length
 *
 * array = {10, 10, 10, 10, 10};
 * sum is 50
 * array length is 5
 * average is 10
 *
 * array = {10, 20, 30, 40, 50, 60, 70, 80, 90, 100};
 * sum is 550
 * array length is 10
 * average is 55
 */

function calculateAverage(arr) {
  if (arr.length === 0) {
    return 0; // To avoid division by zero
  }

  let sum = 0;
  for (let i = 0; i < arr.length; i++) {
    sum += arr[i];
  }

  const average = sum / arr.length;
  return average;
}

// Example usage:
const numbers = [4, 8, 6, 2, 9];
const average = calculateAverage(numbers);
console.log(average); // Output: 5.8
```

We first check if the array is empty (arr.length === 0). If it is, we return
0 to avoid division by zero.

Next, we initialize a variable sum to store the sum of all the elements in
the array.

We then use a for loop to iterate through each element of the array and add
it to the sum variable.

After the loop, we calculate the average by dividing the sum by the length
of the array (arr.length).

Finally, we return the calculated average.

In the example usage, we define an array of numbers numbers and call the
calculateAverage function with this array. The average is stored in the
average variable and printed to the console, which will output 5.8 in this
case.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 2. Find the second largest number in the given array.

```js
function findSecondLargest(arr) {
  if (arr.length < 2) {
    return "Array should have at least two numbers";
  }

  let largest = -Infinity;
  let secondLargest = -Infinity;

  for (let i = 0; i < arr.length; i++) {
    if (arr[i] > largest) {
      secondLargest = largest;
      largest = arr[i];
    } else if (arr[i] > secondLargest && arr[i] < largest) {
      secondLargest = arr[i];
    }
  }

  if (secondLargest === -Infinity) {
    return "There is no second largest number";
  }

  return secondLargest;
}

// Example usage:
const numbers = [4, 8, 6, 2, 9];
const secondLargest = findSecondLargest(numbers);
console.log(secondLargest); // Output: 8
```

First, we perform a check to ensure that the array has at least two numbers.
If the length of the array is less than 2, we return a message indicating
that the array should have at least two numbers.

Next, we initialize two variables, largest and secondLargest, to store the
largest and second largest numbers in the array, respectively. We
initialize them with -Infinity to handle cases where the array contains
negative numbers.

We then loop through each element in the array. If an element is greater
than the current largest, we update secondLargest with the previous value of
largest, and update largest with the new element.

If an element is greater than the current secondLargest but smaller than
largest, we update secondLargest with the new element.

After the loop, we check if secondLargest remains as -Infinity, which means
there is no second largest number in the array. In that case, we return a
message indicating that there is no second largest number.

Otherwise, we return the secondLargest number.

In the example usage, we define an array of numbers numbers and call the
findSecondLargest function with this array. The second largest number is
stored in the secondLargest variable and printed to the console, which will
output 8 in this case.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 3. Find the second minimum number in the given array.

```js
function findSecondMinimum(arr) {
  if (arr.length < 2) {
    return "Array should have at least two numbers";
  }

  let minimum = Infinity;
  let secondMinimum = Infinity;

  for (let i = 0; i < arr.length; i++) {
    if (arr[i] < minimum) {
      secondMinimum = minimum;
      minimum = arr[i];
    } else if (arr[i] < secondMinimum && arr[i] !== minimum) {
      secondMinimum = arr[i];
    }
  }

  if (secondMinimum === Infinity) {
    return "There is no second minimum number";
  }

  return secondMinimum;
}

// Example usage:
const numbers = [4, 8, 6, 2, 9];
const secondMinimum = findSecondMinimum(numbers);
console.log(secondMinimum); // Output: 4
```

First, we perform a check to ensure that the array has at least two numbers.
If the length of the array is less than 2, we return a message indicating
that the array should have at least two numbers.

Next, we initialize two variables, minimum and secondMinimum, to store the
minimum and second minimum numbers in the array, respectively. We initialize
them with Infinity to handle cases where the array contains large positive
numbers.

We then loop through each element in the array. If an element is smaller
than the current minimum, we update secondMinimum with the previous value of
minimum, and update minimum with the new element.

If an element is smaller than the current secondMinimum but not equal to
minimum, we update secondMinimum with the new element.

After the loop, we check if secondMinimum remains as Infinity, which means
there is no second minimum number in the array. In that case, we return a
message indicating that there is no second minimum number.

Otherwise, we return the secondMinimum number.

In the example usage, we define an array of numbers numbers and call the
findSecondMinimum function with this array. The second minimum number is
stored in the secondMinimum variable and printed to the console, which will
output 4 in this case.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 4. Find the missing Number in the given array of 1 to N.

```js
function findMissingNumber(arr) {
  const n = arr.length + 1; // The length of the array is missing one number
  const totalSum = (n * (n + 1)) / 2; // Sum of numbers from 1 to N
  let arraySum = 0;

  for (let i = 0; i < arr.length; i++) {
    arraySum += arr[i];
  }

  const missingNumber = totalSum - arraySum;
  return missingNumber;
}

// Example usage:
const numbers = [1, 2, 4, 5, 6];
const missingNumber = findMissingNumber(numbers);
console.log(missingNumber); // Output: 3
```

We calculate the expected sum of numbers from 1 to N using the formula
(N \* (N + 1)) / 2, where N is the length of the array plus one since it is
missing one number.

Next, we iterate through each element in the array and calculate the sum of
all the numbers in the array.

The missing number can be found by subtracting the sum of the array from the
total expected sum.

Finally, we return the missing number.

In the example usage, we define an array of numbers numbers and call the
findMissingNumber function with this array. The missing number is stored in
the missingNumber variable and printed to the console, which will output 3
in this case.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 5. Write a JavaScript Program to find the **_Intersection of two arrays._**

```js
function findIntersection(arr1, arr2) {
  let i = 0; // Pointer for arr1
  let j = 0; // Pointer for arr2
  const intersection = [];

  while (i < arr1.length && j < arr2.length) {
    if (arr1[i] === arr2[j]) {
      intersection.push(arr1[i]);
      i++;
      j++;
    } else if (arr1[i] < arr2[j]) {
      i++;
    } else {
      j++;
    }
  }

  return intersection;
}

// Example usage:
const array1 = [1, 3, 4, 5, 8];
const array2 = [3, 5, 7, 9];
const result = findIntersection(array1, array2);
console.log(result); // Output: [3, 5]
```

In this program, we use two pointers i and j to iterate through arr1 and
arr2 respectively. We compare the values at these pointers and move the
pointers accordingly.

If the values at arr1[i] and arr2[j] are equal, we found an intersection,
so we add it to the intersection array and move both pointers forward.

If arr1[i] is smaller than arr2[j], we increment i to move to the next
element in arr1.

If arr1[i] is larger than arr2[j], we increment j to move to the next
element in arr2.

We repeat this process until we reach the end of either arr1 or arr2. Finally, we return the intersection array.

In the example usage, we define two sorted arrays array1 and array2 and
call the findIntersection function with these arrays. The result is stored
in the result variable and printed to the console, which will output [3, 5]
in this case.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 6. Write a JavaScript Program to find the **_Intersection of Two Sorted_** arrays.

```js
function findIntersection(arr1, arr2) {
  let i = 0; // Pointer for arr1
  let j = 0; // Pointer for arr2
  const intersection = [];

  while (i < arr1.length && j < arr2.length) {
    if (arr1[i] === arr2[j]) {
      intersection.push(arr1[i]);
      i++;
      j++;
    } else if (arr1[i] < arr2[j]) {
      i++;
    } else {
      j++;
    }
  }

  return intersection;
}

// Example usage:
const array1 = [1, 3, 4, 5, 8];
const array2 = [3, 5, 7, 9];
const result = findIntersection(array1, array2);
console.log(result); // Output: [3, 5]
```

In this program, we use two pointers i and j to iterate through arr1 and arr2 respectively. We compare the values at these pointers and move the pointers accordingly.

If the values at arr1[i] and arr2[j] are equal, we found an intersection, so we add it to the intersection array and move both pointers forward.

If arr1[i] is smaller than arr2[j], we increment i to move to the next element in arr1.

If arr1[i] is larger than arr2[j], we increment j to move to the next element in arr2.

We repeat this process until we reach the end of either arr1 or arr2. Finally, we return the intersection array.

In the example usage, we define two sorted arrays array1 and array2 and call the findIntersection function with these arrays. The result is stored in the result variable and printed to the console, which will output [3, 5] in this case.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 7. Write a JavaScript Program to find the **_Union of Two Arrays (UnSorted Array)_**.

```js
/*
 * Union Of Two Arrays
 * -------------------
 * The Union of Two Arrays Array1, Array2 is the
 * new array which contains all the elements which are
 * either in array1 or in array2, or in both arrays.
 *
 * array1 = {17, 23, 31, 14, 25, 26};
 * array2 = {23, 44, 14, 8, 17};
 *
 * 17, 14 and 23 are present in both arrays
 * UnionArray should contain only one time
 *
 * 31, 25 & 26 are present only in array1
 * all these elements should present in UnionArray
 *
 * 44 & 8 are present only in array2
 * all these elements should present in UnionArray
 *
 * UnionArray = {17, 23, 31, 14, 25, 26, 44, 8};
 *
 */

function findUnion(arr1, arr2) {
  const union = [...arr1]; // Copy arr1 to union array

  // Add elements from arr2 to union if they are not already present
  for (let i = 0; i < arr2.length; i++) {
    if (!union.includes(arr2[i])) {
      union.push(arr2[i]);
    }
  }

  return union;
}

// Example usage:
const array1 = [1, 3, 4, 5, 8];
const array2 = [3, 5, 7, 9];
const result = findUnion(array1, array2);
console.log(result); // Output: [1, 3, 4, 5, 8, 7, 9]
```

In this program, we create a new array union and initially copy all the
elements from arr1 to union using the spread operator ([...arr1]).

Next, we iterate through each element in arr2. If the element is not already
present in union (checked using the includes method), we add it to the
union array using the push method.

After processing all the elements in arr2, we have a new array union
containing all the unique elements from both arr1 and arr2.

Finally, we return the union array.

In the example usage, we define two arrays array1 and array2 and call the
findUnion function with these arrays. The union of the arrays is stored in
the result variable and printed to the console, which will output
[1, 3, 4, 5, 8, 7, 9] in this case.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 8. Write a JavaScript Program to **_Move all Zero to End of the Array_**.

```js
function moveZerosToEnd(arr) {
  let count = 0; // Count of non-zero elements

  // Traverse the array and move non-zero elements to the front
  for (let i = 0; i < arr.length; i++) {
    if (arr[i] !== 0) {
      arr[count] = arr[i];
      count++;
    }
  }

  // Fill the remaining positions with zeros
  while (count < arr.length) {
    arr[count] = 0;
    count++;
  }

  return arr;
}

// Example usage:
const numbers = [0, 5, 0, 3, 8, 0, 9];
const result = moveZerosToEnd(numbers);
console.log(result); // Output: [5, 3, 8, 9, 0, 0, 0]
```

We traverse the array using a loop. If the current element is non-zero,
we move it to the front of the array by assigning it to the position
indicated by the count variable. Then, we increment the count.

After moving all non-zero elements to the front, we fill the remaining
positions of the array with zeros using another loop that starts from the
count variable and goes up to the length of the array.

Finally, we return the modified array with zeros moved to the end.

In the example usage, we define an array of numbers numbers and call the
moveZerosToEnd function with this array. The modified array with zeros
moved to the end is stored in the result variable and printed to the
console, which will output [5, 3, 8, 9, 0, 0, 0] in this case.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 9. Write a JavaScript Program to **_Move all Zeros to Start of the Array_**.

```js
function moveZerosToStart(arr) {
  let count = arr.length - 1; // Count of non-zero elements starting from the end

  // Traverse the array from the end and move non-zero elements to the back
  for (let i = arr.length - 1; i >= 0; i--) {
    if (arr[i] !== 0) {
      arr[count] = arr[i];
      count--;
    }
  }

  // Fill the remaining positions from the start with zeros
  while (count >= 0) {
    arr[count] = 0;
    count--;
  }

  return arr;
}

// Example usage:
const numbers = [0, 5, 0, 3, 8, 0, 9];
const result = moveZerosToStart(numbers);
console.log(result); // Output: [0, 0, 0, 5, 3, 8, 9]
```

We traverse the array using a loop that starts from the end and goes
backwards. If the current element is non-zero, we move it to the back of
the array by assigning it to the position indicated by the count variable.
Then, we decrement the count.

After moving all non-zero elements to the back, we fill the remaining
positions of the array from the start with zeros using another loop
that starts from the count variable and goes down to 0.

Finally, we return the modified array with zeros moved to the start.

In the example usage, we define an array of numbers numbers and call the
moveZerosToStart function with this array. The modified array with
zeros moved to the start is stored in the result variable and printed
to the console, which will output [0, 0, 0, 5, 3, 8, 9] in this case.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 10. Write a JavaScript Program to **_Reverse the given array_**

```js
function reverseArray(arr) {
  const reversed = arr.reverse();
  return reversed;
}

// Example usage:
const numbers = [1, 2, 3, 4, 5];
const result = reverseArray(numbers);
console.log(result); // Output: [5, 4, 3, 2, 1]

// Another approach

function reverseArray(arr) {
  const reversed = [];
  const length = arr.length;

  for (let i = length - 1; i >= 0; i--) {
    reversed.push(arr[i]);
  }

  return reversed;
}

// Example usage:
const numbers = [1, 2, 3, 4, 5];
const result = reverseArray(numbers);
console.log(result); // Output: [5, 4, 3, 2, 1]
```

In this program, we use the reverse() method to reverse the given
array. The reverse() method modifies the original array in place
and returns the reversed array.

We call the reverse() method on the arr array and store the reversed
array in a variable called reversed.

Finally, we return the reversed array.

In the example usage, we define an array of numbers numbers and call
the reverseArray function with this array. The reversed array is
stored in the result variable and printed to the console, which
will output [5, 4, 3, 2, 1] in this case.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 11. Write a program to find the **_Most Frequent Element_** in an given array.

```js
function mostFrequent(arr, n) {
  let maxcount = 0;
  let element_having_max_freq;
  for (let i = 0; i < n; i++) {
    let count = 0;
    for (let j = 0; j < n; j++) {
      if (arr[i] == arr[j]) count++;
    }

    if (count > maxcount) {
      maxcount = count;
      element_having_max_freq = arr[i];
    }
  }

  return element_having_max_freq;
}

// Output

let arr = [40, 50, 30, 40, 50, 30, 30];
let n = arr.length;
console.log(mostFrequent(arr, n)); //30
```

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 12. Write a program to find the **_Most Frequent Element_with occurrence_** in an given array.

```js
function findMostFrequentElement(arr, n) {
  let maxCount = 0;
  let elementWithMaxFreq;

  for (let i = 0; i < n; i++) {
    let count = 0;

    for (let j = 0; j < n; j++) {
      if (arr[i] == arr[j]) count++;
    }

    if (count > maxCount) {
      maxCount = count;
      elementWithMaxFreq = arr[i];
    }
  }

  return { element: elementWithMaxFreq, frequency: maxCount };
}

// Example usage:
const arr = [40, 50, 30, 40, 50, 30, 30];
const n = arr.length;
const result = findMostFrequentElement(arr, n);
console.log(result); // Output: { element: 30, frequency: 3 }
```

In this code, we have modified the mostFrequent function to calculate
the frequency count of each element in the array.

We introduced two variables: maxCount to keep track of the maximum
count and elementWithMaxFreq to store the element with the highest
frequency.

We used two nested loops to compare each element with every other
element in the array and count the occurrences.

If the count is greater than the current maxCount, we update both
maxCount and elementWithMaxFreq accordingly.

Finally, we return an object containing the most frequent element
and its occurrence count.

In the example usage, we defined an array arr and its length n.
We called the findMostFrequentElement function with these parameters.
The most frequent element and its occurrence count are stored in
the result variable and printed to the console, which will output
{ element: 30, frequency: 3 } in this case.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 13. Write a javaScript program to **_Rotate the Given Array_** d times.

```js
function Rotate_and_Print(arr, d, n) {
  //Initializing array temp with size n
  var temp = new Array(n);

  let k = 0;

  // Storing the n - d elements of
  // array arr[] to the front of temp[]
  for (let i = d; i < n; i++) {
    temp[k] = arr[i];
    k++;
  }

  // Storing the first d elements of array arr[]
  //  into temp
  for (let i = 0; i < d; i++) {
    temp[k] = arr[i];
    k++;
  }
  //Printing the temp array which stores the result
  for (let i = 0; i < n; i++) {
    console.log(temp[i] + " ");
  }
}

let arr = [1, 2, 3, 4, 5, 6, 7];
let n = arr.length;
let d = 2; //number of times rotating the array
Rotate_and_Print(arr, d, n); // 3 4 5 6 7 1 2
```

1. initialize a temporary array(temp[n]) of length same as the original array
2. Initialize an integer(k) to keep a track of the current index
3. Store the elements from the position d to n-1 in the temporary array
4. Now, store 0 to d-1 elements of the original array in the temporary array 5. Lastly, copy back the temporary array to the original array

**[⬆ Back to Top](#table-of-contents)**

<br/>

# String Based Programs

## Q 1. Write a javaScript program to **_Reverse the String_** d times.

```js
function reverseString(str) {
  // Split the string into an array of characters, reverse the array, and join the characters back into a string
  return str.split("").reverse().join("");
}

// Example usage
const originalString = "Abhishek";
const reversedString = reverseString(originalString);

console.log("Reversed string:", reversedString); // "Reversed string:", "kehsihbA"

//Another Approach

function reverseString(str) {
  let reversedStr = "";
  for (let i = str.length - 1; i >= 0; i--) {
    reversedStr += str[i];
  }
  return reversedStr;
}

// Example usage
const originalString = "Abhishek";
const reversedString = reverseString(originalString);

console.log("Reversed string:", reversedString); // "Reversed string:", "kehsihbA"
```

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 2. Write a javaScript program to **_Sort the String_** d times.

```js
function sortString(str) {
  // Convert the string into an array of characters
  let arr = str.split("");

  // Sort the array in alphabetical order
  arr.sort();

  // Convert the sorted array back into a string
  let sortedStr = arr.join("");

  return sortedStr;
}

// Test the function
let stringToSort = "Abhishek";
let sortedString = sortString(stringToSort);
console.log(sortedString); //Abehhiks
```

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 3. Write a javaScript program to **_Count the Number of Words_** in a given String.

```js
function countWords(str) {
  // Remove leading and trailing white spaces
  str = str.trim();

  // If the string is empty, return 0
  if (str === "") {
    return 0;
  }

  // Split the string into an array of words
  const words = str.split(/\s+/);

  // Return the number of words in the array
  return words.length;
}

// Example usage:
const inputString = "Hello, my name is abhishek and i love javascript";
const wordCount = countWords(inputString);
console.log("Number of words:", wordCount); // "Number of words:", 9
```

1. It trims the string to remove any leading or trailing white spaces.
2. If the trimmed string is empty, it returns 0 as there are no words.
3. Otherwise, it splits the string into an array of words using the regular expression /\s+/, which matches one or more consecutive white spaces.
4. Finally, it returns the length of the array, which represents the number of words in the string.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 4. Write a javaScript program to **_Count the Number of Vowels_** in the given string.

```js
function countVowels(str) {
  // Convert the string to lowercase
  str = str.toLowerCase();

  // Define an array of vowels
  const vowels = ["a", "e", "i", "o", "u"];

  // Initialize a count variable for vowels
  let vowelCount = 0;

  // Iterate over each character in the string
  for (let i = 0; i < str.length; i++) {
    // Check if the current character is a vowel
    if (vowels.includes(str[i])) {
      // If it is, increment the vowel count
      vowelCount++;
    }
  }

  // Return the total count of vowels
  return vowelCount;
}

// Example usage:
const inputString = "Hello, my name is abhishek and i love javascript";
const vowelCount = countVowels(inputString);
console.log("Number of vowels:", vowelCount); // "Number of vowels:", 15
```

1. It converts the string to lowercase using the toLowerCase() method. This ensures that both uppercase and lowercase vowels are counted.
2. It defines an array called vowels which contains all the vowel characters.
3. It initializes a variable vowelCount to keep track of the count of vowels.
4. It iterates over each character in the string using a for loop.
5. For each character, it checks if it is included in the vowels array using the includes() method.
6. If the character is a vowel, it increments the vowelCount.
7. Finally, it returns the total count of vowels.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 5. Write a JavaScript program to find the **_Most Repeated Character_** in the Given String.

```js
const maxChar = (str) => {
  const strObj = {};
  let maxCount = 0;
  let maxChar = "";
  for (let char of str) {
    strObj[char] = strObj[char] + 1 || 1;
  }
  for (let key in strObj) {
    if (strObj[key] > maxCount) {
      maxCount = strObj[key];
      maxChar = key;
    }
  }
  return maxChar;
};

// a
console.log(maxChar("abhishek"));

// another approach

const maxChar = (str) => {
  const strObj = {};
  for (let char of str) {
    strObj[char] = strObj[char] + 1 || 1;
  }
  return strObj;
};
console.log(maxChar("abhishek")); //{  a: 1,  b: 1,  e: 1,  h: 2,  i: 1,  k: 1,  s: 1}
```

We will keep track of two variables: maxCount & maxChar.
Then, we will loop through the object and compare the value of
each key to maxCount. If the value is greater than the value of
maxCount, then, we will assign that value to maxCount and the
key to maxChar. At the end of the loop, maxChar will be the
most common character in the input string.

**[⬆ Back to Top](#table-of-contents)**

<br/>

## Q 6. Write a JavaScript Program to **_Print All Combinations_** of a given String.

```js
function printCombinations(str) {
  // Create an array to store the combinations
  const combinations = [];

  // Recursive function to generate combinations
  function generateCombinations(prefix, remaining) {
    if (remaining.length === 0) {
      combinations.push(prefix);
      return;
    }

    for (let i = 0; i < remaining.length; i++) {
      const newPrefix = prefix + remaining[i];
      const newRemaining = remaining.slice(0, i) + remaining.slice(i + 1);
      generateCombinations(newPrefix, newRemaining);
    }
  }

  // Start the recursion with an empty prefix and the original string
  generateCombinations("", str);

  // Print the combinations
  for (let combination of combinations) {
    console.log(combination);
  }
}

// Example usage:
const inputString = "abc";
printCombinations(inputString);

// "abc"
// "acb"
// "bac"
// "bca"
// "cab"
// "cba"
```

1. It creates an empty array (combinations) to store the generated
   combinations.
2. It defines a recursive function (generateCombinations) that takes
   a prefix and the remaining characters as input.
3. If there are no remaining characters (remaining.length === 0),
   it means a combination has been formed, so the prefix is added to
   the combinations array.
4. Otherwise, it iterates over each character in the remaining string
   and performs the following steps:
   4.1 It creates a new prefix by appending the current character to
   the existing prefix.
   4.2 It creates a new remaining string by removing the current
   character from the remaining string.
   4.3 It recursively calls the generateCombinations function with
   the new prefix and new remaining string.
5. The recursion starts with an empty prefix and the original string
   (generateCombinations("", str)).
6. After generating all the combinations, it prints each combination
   by iterating over the combinations array.

**[⬆ Back to Top](#table-of-contents)**

</br>

# Converters

## Q 1. Convert Decimal Number to Binary Number.

```js
function decimalToBinary(decimalNumber) {
  // Use toString() with radix 2 to convert decimal to binary
  const binaryNumber = decimalNumber.toString(2);
  return binaryNumber;
}

// Example usage:
const decimal = 10;
const binary = decimalToBinary(decimal);
console.log("Binary representation:", binary);
```

1. It uses the toString() method on the decimalNumber to convert it to a string representation.
2. The toString() method accepts an optional radix parameter, which specifies the base of the number system. In this case, we pass the radix value of 2 to indicate binary representation.
3. The function then returns the binary representation of the decimal number.

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 2. Convert Binary Number to Decimal Number.

```js
function binaryToDecimal(binaryNumber) {
  // Use parseInt() with radix 2 to convert binary to decimal
  const decimalNumber = parseInt(binaryNumber, 2);
  return decimalNumber;
}

// Example usage:
const binary = "1010";
const decimal = binaryToDecimal(binary);
console.log("Decimal representation:", decimal);
```

1. It uses the parseInt() function to parse the binaryNumber as an integer.
2. The parseInt() function accepts an optional radix parameter, which specifies the base of the number system. In this case, we pass the radix value of 2 to indicate binary representation.
3. The function then returns the decimal representation of the binary number.

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 3. Convert Decimal Number to Octal Number.

```js
function decimalToOctal(decimalNumber) {
  // Use toString() with radix 8 to convert decimal to octal
  const octalNumber = decimalNumber.toString(8);
  return octalNumber;
}

// Example usage:
const decimal = 25;
const octal = decimalToOctal(decimal);
console.log("Octal representation:", octal);
```

1. It uses the toString() method on the decimalNumber to convert it to a string representation.
2. The toString() method accepts an optional radix parameter, which specifies the base of the number system. In this case, we pass the radix value of 8 to indicate octal representation.
3. The function then returns the octal representation of the decimal number.

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 4. Convert Octal Number to Decimal Number.

```js
function octalToDecimal(octalNumber) {
  // Use parseInt() with radix 8 to convert octal to decimal
  const decimalNumber = parseInt(octalNumber, 8);
  return decimalNumber;
}

// Example usage:
const octal = "37";
const decimal = octalToDecimal(octal);
console.log("Decimal representation:", decimal);
```

1. It uses the parseInt() function to parse the octalNumber as an integer.
2. The parseInt() function accepts an optional radix parameter, which specifies the base of the number system. In this case, we pass the radix value of 8 to indicate octal representation.
3. The function then returns the decimal representation of the octal number.

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 5. Convert Decimal to Hexadecimal.

```js
function decimalToHexadecimal(decimalNumber) {
  // Use toString() with radix 16 to convert decimal to hexadecimal
  const hexadecimalNumber = decimalNumber.toString(16);
  return hexadecimalNumber;
}

// Example usage:
const decimal = 255;
const hexadecimal = decimalToHexadecimal(decimal);
console.log("Hexadecimal representation:", hexadecimal);
```

1. It uses the toString() method on the decimalNumber to convert it to a string representation.
2. The toString() method accepts an optional radix parameter, which specifies the base of the number system. In this case, we pass the radix value of 16 to indicate hexadecimal representation.
3. The function then returns the hexadecimal representation of the decimal number.

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 6. Convert Hexadecimal to Decimal.

```js
function hexadecimalToDecimal(hexadecimalNumber) {
  // Use parseInt() with radix 16 to convert hexadecimal to decimal
  const decimalNumber = parseInt(hexadecimalNumber, 16);
  return decimalNumber;
}

// Example usage:
const hexadecimal = "FF";
const decimal = hexadecimalToDecimal(hexadecimal);
console.log("Decimal representation:", decimal);
```

1. It uses the parseInt() function to parse the hexadecimalNumber as an integer.
2. The parseInt() function accepts an optional radix parameter, which specifies the base of the number system. In this case, we pass the radix value of 16 to indicate hexadecimal representation.
3. The function then returns the decimal representation of the hexadecimal number.

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 7. Convert Hexadecimal to Decimal.

```js
function hexadecimalToDecimal(hexadecimalNumber) {
  // Use parseInt() with radix 16 to convert hexadecimal to decimal
  const decimalNumber = parseInt(hexadecimalNumber, 16);
  return decimalNumber;
}

// Example usage:
const hexadecimal = "FF";
const decimal = hexadecimalToDecimal(hexadecimal);
console.log("Decimal representation:", decimal);
```

1. It uses the parseInt() function to parse the hexadecimalNumber as an integer.
2. The parseInt() function accepts an optional radix parameter, which specifies the base of the number system. In this case, we pass the radix value of 16 to indicate hexadecimal representation.
3. The function then returns the decimal representation of the hexadecimal number.

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 8. Convert Octal to Binary Number.

```js
function octalToBinary(octalNumber) {
  let binaryNumber = "";

  // Iterate over each octal digit
  for (let i = 0; i < octalNumber.length; i++) {
    const octalDigit = parseInt(octalNumber[i], 8);

    // Convert octal digit to 3-digit binary representation
    const binaryDigit = octalDigit.toString(2).padStart(3, "0");

    // Concatenate binary digit to the binary number
    binaryNumber += binaryDigit;
  }

  return binaryNumber;
}

// Example usage:
const octal = "73";
const binary = octalToBinary(octal);
console.log("Binary representation:", binary);
```

1. It initializes an empty string (binaryNumber) to store the binary representation.
2. It iterates over each octal digit in the octalNumber.
3. For each octal digit, it parses it as an integer using parseInt() with a radix of 8 to get the decimal value of the digit.
4. It converts the decimal value of the octal digit to its 3-digit binary representation using toString() with a radix of 2.
5. If the binary representation is less than 3 digits, it pads it with leading zeros using padStart() to ensure it has exactly 3 digits.
6. It concatenates the binary representation of each octal digit to the binaryNumber string.
7. Finally, it returns the resulting binary number.

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 8. Convert Binary Number to Octal.

```js
// 1. Group the binary digits in sets of three digits starting from the rightmost side.
// 2. Convert each set of three binary digits to their equivalent octal digit.
// 3. Concatenate the octal digits to form the octal number.

function binaryToOctal(binaryNumber) {
  let octalNumber = "";

  // Pad the binary number with leading zeros to make it divisible by 3
  const paddingLength =
    binaryNumber.length % 3 === 0 ? 0 : 3 - (binaryNumber.length % 3);
  const paddedBinaryNumber = "0".repeat(paddingLength) + binaryNumber;

  // Group the binary digits in sets of three from right to left
  for (let i = paddedBinaryNumber.length - 1; i >= 0; i -= 3) {
    const binaryDigits = paddedBinaryNumber.substring(
      Math.max(i - 2, 0),
      i + 1
    );
    const octalDigit = parseInt(binaryDigits, 2).toString(8);
    octalNumber = octalDigit + octalNumber;
  }

  return octalNumber;
}

// Example usage:
const binary = "101010";
const octal = binaryToOctal(binary);
console.log("Octal representation:", octal);
```

1. It initializes an empty string (octalNumber) to store the octal representation.
2. It pads the binaryNumber with leading zeros to make it divisible by 3 using the paddingLength variable.
3. It iterates over the padded binary number in sets of three digits from right to left.
4. For each set of three binary digits, it converts them to their equivalent decimal value using parseInt() with a radix of 2.
5. It converts the decimal value to its octal representation using toString() with a radix of 8.
6. It concatenates the octal digit to the octalNumber string.
7. Finally, it returns the resulting octal number.

**[⬆ Back to Top](#table-of-contents)**

</br>

# Print the Series

## Q 1. Write the JavaScript Program to print the following series **_EVEN number Series_**

```js
function printEvenSeries(limit) {
  for (let i = 2; i <= limit; i += 2) {
    console.log(i);
  }
}

// Example usage:
const limit = 10;
console.log("Even number series:");
printEvenSeries(limit);

// "Even number series:"
// 2
// 4
// 6
// 8
// 10
```

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 2. Write the JavaScript Program to print the following series **_ODD number Series_**

```js
function printOddSeries(limit) {
  console.log("Odd number series:");
  for (let i = 1; i <= limit; i += 2) {
    console.log(i);
  }
}

// Example usage:
const limit = 10;
printOddSeries(limit);

// Odd number series:
// 1
// 3
// 5
// 7
// 9
```

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 3. Write the JavaScript Program to print the following series **_Pattern Series_** 3, 33, 333, 3333, 33333, 333333 ....

```js
function printPatternSeries(n) {
  let pattern = "";

  for (let i = 1; i <= n; i++) {
    pattern += "3";
    console.log(pattern);
  }
}

// Example usage:
const n = 5;
printPatternSeries(n);

// 3
// 33
// 333
// 3333
// 33333
```

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 4. Write the JavaScript Program to print the following series **_Geometric Progression_**

```js
function printGeometricProgression(a, r, n) {
  console.log("Geometric progression series:");
  let term = a;

  for (let i = 0; i < n; i++) {
    console.log(term);
    term *= r;
  }
}

// Example usage:
const initialTerm = 1;
const commonRatio = 2;
const numberOfTerms = 10;

printGeometricProgression(initialTerm, commonRatio, numberOfTerms);

// "Geometric progression series:"
// 1
// 2
// 4
// 8
// 16
// 32
// 64
// 128
// 256
// 512
```

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 5. Write the JavaScript Program to print the following series **_Fibonacci Series_**

```js
function printFibonacciSeries(n) {
  let series = [];

  // First two terms of the series
  series[0] = 0;
  series[1] = 1;

  // Generate the Fibonacci series
  for (let i = 2; i < n; i++) {
    series[i] = series[i - 1] + series[i - 2];
  }

  // Print the series
  console.log("Fibonacci series:");
  for (let i = 0; i < n; i++) {
    console.log(series[i]);
  }
}

// Example usage:
const numberOfTerms = 10;
printFibonacciSeries(numberOfTerms);

// Fibonacci series:
// 0
// 1
// 1
// 2
// 3
// 5
// 8
// 13
// 21
// 34
```

In this program, the printFibonacciSeries function takes a parameter n
that specifies the number of terms in the Fibonacci series to print.
It initializes an array series to store the Fibonacci series.

The program starts with the first two terms of the series, 0 and 1.
Then, using a for loop, it generates the Fibonacci series by adding
the previous two terms. Each new term is the sum of the two preceding
terms.

Finally, it prints the Fibonacci series using another for loop.

In the example usage, the program prints the Fibonacci series with 10
terms. You can modify the value of numberOfTerms to generate a
different number of terms in the series.

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 6. Write the JavaScript Program to print the following series **_Prime Number Series_**

```js
function isPrime(num) {
  if (num <= 1) {
    return false;
  }

  for (let i = 2; i <= Math.sqrt(num); i++) {
    if (num % i === 0) {
      return false;
    }
  }

  return true;
}

function printPrimeSeries(n) {
  console.log("Prime number series:");
  let count = 0;
  let number = 2;

  while (count < n) {
    if (isPrime(number)) {
      console.log(number);
      count++;
    }
    number++;
  }
}

// Example usage:
const numberOfPrimes = 10;
printPrimeSeries(numberOfPrimes);

// Prime number series:
// 2
// 3
// 5
// 7
// 11
// 13
// 17
// 19
// 23
// 29
```

In this program, we define a helper function isPrime to check if a number
is prime or not. It takes a number num as an argument and checks if it
is divisible by any number from 2 to the square root of the number.
If it is divisible by any number, it returns false; otherwise, it
returns true.

The printPrimeSeries function takes a parameter n that specifies the
number of prime numbers to print. It uses a while loop to iterate until
the desired count of prime numbers is reached. It checks if each number
is prime using the isPrime function and prints it if it is.

In the example usage, the program prints the prime number series with 10
prime numbers. You can modify the value of numberOfPrimes to generate a
different number of prime numbers in the series.

**[⬆ Back to Top](#table-of-contents)**
</br>

# Problem solved using special Function

## Q 1. Write the JavaScript Program using **_Concat_**

```js
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const result = arr1.concat(arr2);
console.log(result); //Output: [1, 2, 3, 4, 5, 6];
```

Concatenates two or more arrays

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 2. Write the JavaScript Program using **_Entries()_**

```js
const arr = ["a", "b", "c"];
const iterator = arr.entries();
console.log(iterator.next().value); //Output: [0 ,'a'];
console.log(iterator.next().value); //Output: [1 ,'b'];
console.log(iterator.next().value); //Output: [2 ,'c'];
```

Returns an iterator object that contains the key value pairs
for each index in the array

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 3. Write the JavaScript Program using **_every()_**

```js
const arr = [1, 2, 3, 4, 5];
const allEven = arr.every((num) => num % 2 === 0);
console.log(hasEvenNumber); //Output: false
```

Tests whether all elements in the array pass the provided function.

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 4. Write the JavaScript Program using **fill()**

```js
const arr = [1, 2, 3, 4, 5];
const allEven = arr.every((num) => num % 2 === 0);
console.log(hasEvenNumber); //Output: false
```

Fills all elements in the array with a static value.

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 5. Write the JavaScript Program using **filter()**

```js
const arr = [1, 2, 3, 4, 5];
const evenNumbers = arr.filter((num) => num % 2 === 0);
console.log(hasEvenNumber); //Output: [2,4]
```

Creates a new array with all elements that pass the provided function's test

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 6. Write the JavaScript Program using **find()**

```js
const arr = [1, 2, 3, 4, 5];
const foundNumber = arr.find((num) => num > 3);
console.log(foundNumber); //Output: [4]
```

Returns the first element in the array that satisfies the provided testing function.

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 7. Write the JavaScript Program using **findIndex()**

```js
const arr = [1, 2, 3, 4, 5];
const foundNumber = arr.findIndex((num) => num > 3);
console.log(foundNumber); //Output: [3]
```

Returns the index of the first element in the array that satisfies
the provided testing function.

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 8. Write the JavaScript Program using **indexOf()**

```js
const arr = [1, 2, 3, 4, 5];
const index = arr.indexOf(3);
console.log(index); //Output: 2
```

Returns the first index at which a specified element is found in an array

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 9. Write the JavaScript Program using **lastIndexOf()**

```js
const arr = [1, 2, 3, 4, 5];
const index = arr.lastIndexOf(2);
console.log(index); //Output: 4
```

Returns the last index at which a specified element is found in an array

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 10. Write the JavaScript Program using **flat()**

```js
const arr = [1, 2, [3, 4, [5, 6]]];
const flattened = arr.flat(2);
console.log(flattened); //Output: [1,2,3,4,5,6]
```

Creates a new array with all sub array elements concatenated
into it recursively up to the specified depth

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 11. Write the JavaScript Program using **flatMap()**

```js
const arr = [1, 2, 3, 4, 5];
const doubledAndFlattened = arr.flatMap((num) => [num * 2]);
console.log(doubledAndFlattened); //Output: [2, 4, 6, 8, 10]
```

Maps each element using a mapping function, then flattens the result
into a new array

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 12. Write the JavaScript Program using **includes()**

```js
const arr = [1, 2, 3, 4, 5];
const includesThree = arr.includes(3);
console.log(includesThree); //Output: true
```

Checks if an array contains a specific element

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 13. Write the JavaScript Program using **forEach()**

```js
const arr = [1, 2, 3, 4, 5];
arr.forEach((num) => {
  console.log(num);
});
// Output:
// 1
// 2
// 3
// 4
// 5
```

Executes a provided function once for each array element.

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 14. Write the JavaScript Program using **from()**

```js
const arr = Array.from("JavaScript");
console.log(arr); //Output ["J", "a", "v", "a", "S", "c", "r", "i", "p", "t"]
```

Allows you to convert an iterable object (such as a string, Set,
Map, etc or an array like object (such as the
arguments object) into a new array

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 15. Write the JavaScript Program using **join()**

```js
const arr = [1, 2, 3, 4, 5];
const joined = arr.join("-");
console.log(joined); //Output: "1-2-3-4-5"
```

Joins all elements of an array into a string

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 16. Write the JavaScript Program using **key()**

```js
const arr = ["a", "b", "c"];
const iterator = arr.keys();
console.log(iterator.next().value); //Output:0;
console.log(iterator.next().value); //Output:1;
console.log(iterator.next().value); //Output:2;
```

Returns a new Array Iterator object that contains
the keys for each index in the array.

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 17. Write the JavaScript Program using **map()**

```js
const arr = [1, 2, 3, 4, 5];
const doubled = arr.map((num) => num * 2);
console.log(doubled); //Output: [2, 4, 6, 8, 10]
```

Creates a new array with the results of calling a provided
function on every element in the array.

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 18. Write the JavaScript Program using **pop()**

```js
const arr = [1, 2, 3, 4, 5];
const lastElement = arr.pop();
console.log(doubled); //Output: 5
console.log(arr); //Output: [1,2,3,4]
```

Removes the last element from an array and
returns that element

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 19. Write the JavaScript Program using **push()**

```js
const arr = [1, 2, 3, 4, 5];
arr.push(6);
console.log(arr); //Output: [1,2,3,4,5,6]
```

Adds one or more elements to the end of an array and
returns the new length of the array

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 20. Write the JavaScript Program using **shift()**

```js
const arr = [1, 2, 3, 4, 5];
const firstElement = arr.shigt();
console.log(firstElement); //Output: 1
console.log(arr); //Output: [2,3,4,5]
```

Removes the first element from an array and returns
that element

**[⬆ Back to Top](#table-of-contents)**
</br>


## Q 21. Write the JavaScript Program using **unshift()**

```js
const arr = [1, 2, 3, 4, 5];
arr.unshift(0);
console.log(arr); //Output: [0,1,2,3,4,5]
```

Adds one or more elements to the beginning of an array
and returns the new length of the array

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 22. Write the JavaScript Program using **reduce()**

```js
const arr = [1, 2, 3, 4, 5];
const sum = arr.reduce((acc, num) => acc + num, 0);
console.log(sum); //Output: 15
```

Applies a function against an accumulator and each element in
the array (from left to right) to reduce it to a single value

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 23. Write the JavaScript Program using **reduceRight()**

```js
const arr = [1, 2, 3, 4, 5];
const sum = arr.reduceRight((acc, num) => acc + num, 0);
console.log(sum); //Output: 15
```

Applies a function against an accumulator and each element in
the array (from right to left) to reduce it to a single value

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 24. Write the JavaScript Program using **reverse()**

```js
const arr = [1, 2, 3, 4, 5];
arr.reverse();
console.log(arr); //Output: [5, 4, 3, 2, 1]
```

Reverses the order of the elements in an array

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 25. Write the JavaScript Program using **slice()**

```js
const arr = [1, 2, 3, 4, 5];
const sliced = arr.slice(1, 4);
console.log(sliced); //Output: [2,3,4]
```

Extracts a section of an array and returns a new array

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 26. Write the JavaScript Program using **splice()**

```js
const arr = [1, 2, 3, 4, 5];
const removed = arr.slice(2, 2);
console.log(removed); //Output: [3,4]
console.log(arr); //Output: [1,2,5]
```

Changes the contents of an array by removing, replacing,or adding elements

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 27. Write the JavaScript Program using **sort()**

```js
const arr = [3, 1, 5, 2, 4];
arr.sort();
console.log(arr); //Output: [1,2,3,4,5]
```

Sorts the elements of an array in place and returns the sorted array
**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 28. Write the JavaScript Program using **toString()**

```js
const arr = [1, 2, 3, 4, 5];
const str = arr.toString();
console.log(arr); //Output: '1,2,3,4,5'
```

Returns a string representing the specified array and its elements

**[⬆ Back to Top](#table-of-contents)**

</br>

## Q 29. Write the JavaScript Program using **values()**

```js
const arr = ["a", "b", "c"];
const iterator = arr.values();
console.log(iterator.nect().value); //Output: 'a'
console.log(iterator.nect().value); //Output: 'b'
console.log(iterator.nect().value); //Output: 'c'
```

Returns a new Array Iterator object that contains the values for
each index in the array

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 30. Write the JavaScript Program using **copyWithin()**

```js
const arr = [1, 2, 3, 4, 5];
arr.copyWithin(0, 3, 5);
console.log(arr); //Output:[4,5,3,4,5]
```

Copies a portion of an array to another location within the same array

**[⬆ Back to Top](#table-of-contents)**
</br>

## Q 31. Write the JavaScript Program using **Array.of()**

```js
const array = Array.of(1, 2, 3, 4, 5);
console.log(array); //Output:[1,2,3,4,5]

const singleElementArray = Array.of(10);
console.log(singleElementArray); //Output:[10]
```

is a built in method in JavaScript that is used to convert the elements of an
array into localized strings based on the current locale settings

**[⬆ Back to Top](#table-of-contents)**
</br>
