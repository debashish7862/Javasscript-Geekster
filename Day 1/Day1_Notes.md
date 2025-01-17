# What is Javascript

1.  What is JavaScript? JavaScript is a high-level, interpreted programming language that is commonly used for web development. It was created in 1995 by Brendan Eich while he was working at Netscape Communications Corporation. JavaScript is often abbreviated as JS, and it is one of the most popular programming languages in the world.

2.  Purpose of JavaScript The purpose of JavaScript is to add interactivity and dynamic functionality to web pages. With JavaScript, you can add animations, respond to user actions, validate user input, and manipulate the HTML and CSS of a web page. It is also commonly used on the server-side with Node.js to build scalable web applications.

3.  JavaScript Features JavaScript has several key features that make it a popular choice for web development:

- Interactivity: JavaScript allows you to add interactive elements to web pages, such as dropdown menus, pop-ups, and animations.
- Lightweight: JavaScript is a lightweight programming language that can be easily embedded in web pages.
- Flexibility: JavaScript can be used on the client-side (in web browsers) and the server-side (with Node.js).
- Rich library support: There are numerous JavaScript libraries and frameworks that make it easier to develop web applications.
- High performance: Modern JavaScript engines are highly optimized, making JavaScript code run very quickly in web browsers.

1.  What is Node? Node.js is an open-source, cross-platform JavaScript runtime environment that allows developers to run JavaScript code outside of a web browser. It is built on the V8 JavaScript engine (which is used by Google Chrome) and provides a way to write server-side applications using JavaScript.

2.  Installation of Node To install Node.js, you can download the installer from the official Node.js website (<https://nodejs.org/en/>). Once the installer is downloaded, run it and follow the on-screen instructions to complete the installation.

3.  Executing JS File With Node To execute a JavaScript file with Node.js, you can use the command-line interface (CLI). Open a terminal or command prompt and navigate to the directory that contains the JavaScript file. Then, run the following command:

```
node file.js
```

4. This will execute the JavaScript file and output any results to the console.

console.log()
console.log() is a JavaScript function that is used to output data to the console (in web browsers or with Node.js). It takes one or more arguments and prints them to the console. For example:

```
console.log('Hello, world!');

```

5. This would output the string "Hello, world!" to the console.

JS variables
A variable in JavaScript is a container for storing data values. You can declare a variable using the var, let, or const keywords. For example:

```
var name = 'John';
let age = 30;
const PI = 3.14;
```

In this example, name is a variable that stores a string, age is a variable that stores a number, and PI is a variable that stores a constant value.

6. JS Data types
   JavaScript has several data types, including:
   String: A sequence of characters, such as "Hello, world!"
   Number: A numeric value, such as 42 or 3.14
   Boolean: A value that is either true or false
   Undefined: A value that indicates a variable has not been assigned a value
   Null: A value that represents nothing or no value
   Object: A collection of properties and values
   Symbol: A unique identifier (added in ES6)

7. Operators
   JavaScript has several operators for performing operations on data values, including:
   Arithmetic operators

Arithmetic operators include `+` (addition), `-` (subtraction), `*` (multiplication), `/` (division), and `%` (modulus).

- Comparison operators Comparison operators are used to compare two values and return a Boolean value. They include `==` (equal to), `!=` (not equal to), `>` (greater than), `<` (less than), `>=` (greater than or equal to), and `<=` (less than or equal to).

- Logical operators Logical operators are used to combine Boolean values and return a Boolean value. They include `&&` (and), `||` (or), and `!` (not).

- Assignment operators Assignment operators are used to assign values to variables. They include `=` (simple assignment), `+=` (addition assignment), `-=` (subtraction assignment), `*=` (multiplication assignment), `/=` (division assignment), and `%=` (modulus assignment).

# Conditionals

Conditional statements are used for  make decisions based on different conditions.
By default , statements in JavaScript script executed sequentially from top to bottom. If the processing logic require so, the sequential flow of execution can be altered in two ways:

- Conditional execution: a block of one or more statements will be executed if a certain expression is true
- Repetitive execution: a block of one or more statements will be repetitively executed as long as a certain expression is true. In this section, we will cover _if_, _else_ , _else if_ statements. The comparison and logical operators we learned in the previous sections will be useful in here.

Conditions can be implementing using the following ways:

- if
- if else
- if else if else
- switch
- ternary operator

## If

In JavaScript and other programming languages the key word _if_ is to used check if a condition is true and to execute the block code. To create an if condition, we need _if_ keyword, condition inside a parenthesis and block of code inside a curly bracket({}).

```js
// syntax
if (condition) {
  //this part of code runs for truthy condition
}
```

**Example:**

```js
let num = 3
if (num > 0) {
  console.log(`${num} is a positive number`)
}
//  3 is a positive number
```

As you can see in the  condition example above, 3 is greater than 0, so it is a positive number. The condition was true and the block of code was executed. However, if the condition is false, we won't  see any results.

```js
let isRaining = true
if (isRaining) {
  console.log('Remember to take your rain coat.')
}
```

 The same goes for the second condition, if isRaining is false the if block will not be executed and we do not see any output. In order to see the result of a falsy condition, we should have another block, which is going to be _else_.

## If Else

If condition is true the first block will be executed, if not the else condition will be executed.

```js
// syntax
if (condition) {
  // this part of code runs for truthy condition
} else {
  // this part of code runs for false condition
}
```

```js
let num = 3
if (num > 0) {
  console.log(`${num} is a positive number`)
} else {
  console.log(`${num} is a negative number`)
}
//  3 is a positive number

num = -3
if (num > 0) {
  console.log(`${num} is a positive number`)
} else {
  console.log(`${num} is a negative number`)
}
//  -3 is a negative number
```

The last condition is false, therefore the else block was executed. What if we have more than two conditions? In that case,  we would use *else if* conditions.

## If  Else if Else

On our daily life, we make decisions on daily basis. We make decisions not by checking  one or two conditions instead we make decisions based on multiple conditions. As similar to our daily life, programming is also full of conditions. We use *else if* when we have multiple conditions.

```js
// syntax
if (condition) {
     // code
} else if (condition) {
   // code
} else {
    //  code

}
```

**Example:**

```js
let a = 0
if (a > 0) {
  console.log(`${a} is a positive number`)
} else if (a < 0) {
  console.log(`${a} is a negative number`)
} else if (a == 0) {
  console.log(`${a} is zero`)
} else {
  console.log(`${a} is not a number`)
}
```

## Switch

Switch  is an alternative for **if else if else else**.
The switch statement starts with a *switch* keyword followed by a parenthesis and code block. Inside the code block we will have different cases. Case block runs if the value in the switch statement parenthesis matches with the case value. The break statement is to terminate execution so the code execution  does not go down after the condition is satisfied.  The default block runs if all the cases don't satisfy the condition.

```js
switch(caseValue){
  case 1:
    // code
    break
  case 2:
   // code
   break
  case 3:
   // code
   break
  default:
   // code
}
```

```js
let weather = 'cloudy'
switch (weather) {
  case 'rainy':
    console.log('You need a rain coat.')
    break
  case 'cloudy':
    console.log('It might be cold, you need a jacket.')
    break
  case 'sunny':
    console.log('Go out freely.')
    break
  default:
    console.log(' No need for rain coat.')
}
```
// Examples to use conditions in the cases

```js
let num = prompt('Enter number');
switch (true) {
  case num > 0:
    console.log('Number is positive');
    break;
  case num == 0:
    console.log('Numbers is zero');
    break;
  case num < 0:
    console.log('Number is negative');
    break;
  default:
    console.log('Entered value was not a number');
}
```

## Ternary Operators

Another way to write conditionals is using ternary operators. We have covered this in other sections, but we should also mention it here.

```js
let isRaining = true
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.')
```

More Examples - https://www.programiz.com/javascript/ternary-operator