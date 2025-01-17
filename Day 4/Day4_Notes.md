# Objects:

1. Object: - In programming, an object is a collection of properties that represent a real-world entity or concept. It is a data structure that groups related data and functions into a single unit. Objects are used to model complex systems and can be used to represent anything from a person to a car to a company. In JavaScript, objects are created using curly braces {} and consist of key-value pairs.

2. Operations on Objects:

a. Insertion: You can add a new property to an object by using the dot notation or square brackets.
 Here's an example:

```
const person = {
  name: 'Geekster',
  age: 25
};

person.email = 'john@example.com'; // dot notation
person['phone'] = '1234567890'; // square brackets

``` 

b. Reading: You can access the value of a property in an object using the dot notation or square brackets. Here's an example:

```
const person = {
  name: 'John',
  age: 25,
  email: 'john@example.com',
  phone: '1234567890'
};

console.log(person.name); // Output: "John"
console.log(person['age']); // Output: 25

```

c. Updation: You can update the value of a property in an object using the dot notation or square brackets. 
Here's an example:

```
const person = {
  name: 'John',
  age: 25,
  email: 'john@example.com',
  phone: '1234567890'
};

person.age = 26; // dot notation
person['phone'] = '0987654321'; // square brackets

```
d. Deletion: You can remove a property from an object using the delete keyword. Here's an example:

```
const person = {
  name: 'John',
  age: 25,
  email: 'john@example.com',
  phone: '1234567890'
};

delete person.email;
```

3. Creating a Simple Nested Object:
A nested object is an object that contains one or more properties that are also objects. 
Here's an example of a simple nested object:
```
const person = {
  name: 'John',
  age: 25,
  contact: {
    email: 'john@example.com',
    phone: '1234567890'
  }
};
```

4. JSON:
JSON (JavaScript Object Notation) is a lightweight data interchange format that is easy for humans to read and write, and easy for machines to parse and generate. It is a text format that is completely language-independent but uses conventions that are familiar to programmers of the C family of languages, including C, C++, C#, Java, JavaScript, Perl, Python, and many others. JSON is used to transmit data between a server and a web application, as an alternative to XML.

5. Creating a Complex Nested Object:
A complex nested object is an object that contains multiple levels of nesting. Here's an example:

```
const company = {
  name: 'ABC Corp',
  employees: [
    {
      name: 'John',
      age: 25,
      contact: {
        email: 'john@example.com',
        phone: '1234567890'
      }
    },
    {
      name: 'Mary',
      age: 30,
      contact: {
        email: 'mary@example.com',
        phone: '0987654321'
      }
    }
  ],
  location: {
    address: '123 Main St',
    city: 'Anytown',
    state: 'CA',
    zip: '12345'
  }
};
```
