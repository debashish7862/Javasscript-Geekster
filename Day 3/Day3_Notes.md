﻿# Strings and its properties

1. In programming, a string is a sequence of characters that are used to represent text. In JavaScript and Java, strings are objects that have properties and methods. Some common properties of a string include its length, which represents the number of characters in the string, and its index, which represents the position of a character within the string.


2. Methods: There are a number of methods that can be used to manipulate strings in Java and JavaScript. Some common methods include:

- toUpperCase() and toLowerCase(): These methods convert all characters in a string to upper or lower case, respectively.

- concat(): This method combines two or more strings into a single string.

- charAt(): This method returns the character at a specified index in a string.

- indexOf() and lastIndexOf(): These methods return the index of the first or last occurrence of a specified substring within a string.

- replace(): This method replaces a specified substring with another substring within a string.

- trim(): This method removes whitespace from the beginning and end of a string.


3. String search: In JavaScript, you can use the search() method to search for a specific string within another string. This method returns the index of the first occurrence of the specified string, or -1 if the string is not found.

4. String template: String templates, also known as template literals, are a way to embed expressions inside strings in JavaScript. They are enclosed in backticks (`) instead of single or double quotes, and can contain placeholders that are replaced with values at runtime. For example:

```
const name = 'John';
const age = 30;
const message = `My name is ${name} and I am ${age} years old.`;
console.log(message); // Output: "My name is John and I am 30 years old."

```

5. slice() and substring(): Both slice() and substring() are string methods that can be used to extract a substring from a larger string. The main difference between the two is that slice() can accept negative indices, while substring() cannot. 

Here are some examples:

```
const myString = 'Hello, world!';
const substring1 = myString.slice(7, 12); // Output: "world"
const substring2 = myString.substring(7, 12); // Output: "world"
const substring3 = myString.slice(-6); // Output: "world!"
const substring4 = myString.substring(7); // Output: "world!"

```
