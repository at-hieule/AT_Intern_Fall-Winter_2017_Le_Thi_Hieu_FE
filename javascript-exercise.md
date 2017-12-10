# HTML + Javascript Exercise

### Knowledge round-up

- **Javascript**

  - What are the differences between a variable that is: `null`, `undefined`?
  + undefined is a variable that has been declared but no value exists and is a type of itself undefined’.
  + null is a value of a variable and is a type of object.
  - What is `use strict`?
  + Allows you to place a program, or a function, in a "strict" operating context. This strict context prevents certain actions from being taken and throws more exceptions.
  Strict mode throws more errors and disables some features in an effort to make your code more robust, readable, and accurate.
  - What are the advantages and disadvantages to using it?
  + It catches some common coding bloopers, throwing exceptions.
  + It prevents, or throws errors, when relatively “unsafe” actions are taken (such as gaining access to the global object).
  + It disables features that are confusing or poorly thought out.
  Disadvantages: Code mixed strict and “normal” modes. If a developer used a library that was in strict mode, but the developer was used to working in normal mode, they might call some actions on the library that wouldn’t work as expected. Worse, since the developer is in normal mode, they don’t have the advantages of extra errors being thrown, so the error might fail silently.

  - What are the differences between `==` and `===`? Write an example for each case (if any)?
  + == only compares values
  + === compares values + type
  ex: var check1 = '10',
      check2 = 10;
      check1 == check2 // true
      check1 === check2 // false
  - What is different between declaration: `var`, `const` and `let`?
  + var: function scope, modify value
  + let: block scope, modify value
  + const: block scope, unmodify value


### Playground
1. Write a JavaScript program to compute the sum of the two given integers. If the two values are same, then returns triple their sum.
```
Input: a = 5, b = 10
Output: 15

Input: a = 5, b = 5
Output: 30

function sum(a, b){
  if(a === b){
    return a * 2 * 3;
  }else{
    return a + b;
  }
}

```


2. Write a JavaScript program to compute the absolute difference between a specified number and 19. Returns triple their absolute difference if the specified number is greater than 19.

```
Input: a = 12
Output: 7

Input: a = 19
Output: 0

Input: a = 22
Output: 9

function abs(num){
  if(num > 19){
    return (num - 19) * 3;
  }else{
    return 19 - num;
  }
}
```

3. A masked number is a string that consists of digits and one asterisk (*) that should be replaced by exactly one digit. Given a masked number find all the possible options to replace the asterisk with a digit to produce an integer divisible by 3.
```
Input: a = '1*9'
Output: ['129', '159', '189']
```
```
Input: a = '1234567890*'
Output: ['12345678900', 
 '12345678903', 
 '12345678906', 
 '12345678909']

function find(x) {
  let output = [];
  let index = 0;
  for(let i =0; i<10; i++){
    let sum = 0;
      let num = x.replace("*", i);
    if(num%3 == 0){
        output[index] = num;
          output++;
      }
  }
  return output;
}

```
4. A masked number is a string that consists of digits and one asterisk (*) that should be replaced by exactly one digit. Given a masked number find all the possible options to replace the asterisk with a digit to produce an integer divisible by 6.
```
Input: a = '1*9'
Output: []
```
```
Input: a = '1234567890*'
Output: ['12345678900', 
 '12345678906']

function find(x) {
  let output = [];
  let index = 0;
  for(let i =0; i<10; i++){
    let sum = 0;
      let num = x.replace("*", i);
    if(num%6 == 0){
        output[index] = num;
          output++;
      }
  }
  return output;
}

```