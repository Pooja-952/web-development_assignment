//**Q.1 Explain Hoisting in JavaScript**

//Solution--->

Hoisting is a concept in JavaScript that refers to the behavior of moving variable and function declarations to the top of their containing scope during the compilation phase, before the code is executed.

In JavaScript, when you declare a variable or a function using the var keyword, the declaration is hoisted to the top of its scope. This means that you can use the variable or call the function before the actual declaration in your code, and it will still work.

Example:-

console.log(message); // Output: undefined
var message = "Hello, world!";
console.log(message); // Output: Hello, world!

Even though the variable message is used before its declaration, it does not result in an error. This is because the variable declaration is hoisted to the top of the scope, and the assignment (message = "Hello, world!") is executed in the order it appears in the code.

Similarly, function declarations are also hoisted to the top of their scope. This means that you can call a function before its actual declaration in the code.

greet(); // Output: Hello!

function greet() {
  console.log("Hello!");
}

In this example, the greet function is called before its declaration, but it still works because the function declaration is hoisted to the top.

However, it's important to note that hoisting only applies to variable and function declarations, not to initializations or assignments. If you declare a variable using let or const, they are hoisted as well but not initialized, so trying to use them before their declaration will result in a ReferenceError.

To avoid confusion and improve code readability, it's generally recommended to declare variables and functions at the beginning of their scope, even though hoisting allows you to use them before their actual declarations.

**//Q.2 Explain Temporal Dead Zone?**

//Solution--->

The Temporal Dead Zone is a concept in JavaScript that refers to a specific behavior related to variables declared with the let and const keywords. When a variable is declared using either of these keywords, it enters a phase called the TDZ until the point of declaration is reached during the program's execution.

During the Temporal Dead Zone , accessing the variable will result in a ReferenceError. This means that although the variable has been declared, it cannot be accessed or assigned any value until after the declaration statement. This behavior is different from variables declared with the var keyword, which are hoisted to the top of their scope and can be accessed before their declaration. (though they have an initial value of undefined).

The purpose of the Temporal Dead Zone  is to prevent the usage of variables before they are explicitly declared. It helps enforce better code quality and prevents issues that can arise from using variables before they have been properly initialized. By throwing a ReferenceError during the TDZ, JavaScript ensures that developers are aware of such mistakes and can fix them accordingly.

Example:-

console.log(x); // ReferenceError: Cannot access 'x' before initialization
let x = 10;

In the above code, the variable x is accessed before it is declared, resulting in a ReferenceError during the Temporal Dead Zone . Moving the console.log statement after the variable declaration would resolve the error:

let x = 10;
console.log(x); // Output: 10

**//Q.3 Difference between var & let?**

//Solution--->

In JavaScript, 'var' and 'let' are both used to declare variables, but they have some differences in terms of scope and behavior:

1. Scope: Variables declared with 'var' have function scope or global scope, meaning they are accessible throughout the entire function or global environment. On the other hand, variables declared with 'let' have block scope, which means they are only accessible within the nearest enclosing block (usually a pair of curly braces {}).

2. Hoisting: Variables declared with 'var' are hoisted to the top of their scope, which means they can be accessed before their declaration (although they have an initial value of 'undefined'). This behavior is known as "hoisting." On the contrary, variables declared with 'let' are not hoisted, and accessing them before their declaration results in a 'ReferenceError' within the Temporal Dead Zone.

3. Re-declaration: Variables declared with 'var' can be re-declared multiple times within the same scope without raising an error. The subsequent declarations override the previous ones. Conversely, variables declared with 'let' cannot be re-declared within the same block scope. Attempting to do so will result in a 'SyntaxError'.

4. Function-scoped vs. block-scoped loops: When using 'var', loop counters declared within a loop (for example, a 'for' loop) are accessible outside the loop, retaining their value after the loop exits. This is because 'var' variables have function scope. In contrast, 'let' variables have block scope, so loop counters declared with 'let' are only accessible within the loop block and do not persist after the loop ends.

'var' has function scope, is hoisted, allows re-declaration, and has different behavior in loops. 'let', on the other hand, has block scope, is not hoisted (leading to the Temporal Dead Zone), does not allow re-declaration, and behaves consistently in loops. It is generally recommended to use 'let' (or 'const' for constants) instead of 'var' for more predictable and localized variable scoping.

**//Q.4 What are the major features introduced in ECMAScript 6?**

//Solution--->

1. Block-scoped variables: The introduction of the 'let' and 'const' keywords allows developers to declare variables with block scope, which improves scoping precision and reduces potential issues.

2. Arrow functions: ES6 introduced arrow functions, offering a concise syntax for writing anonymous functions. Arrow functions have a lexically bound 'this' keyword, avoiding common pitfalls related to function scope and 'this' binding.

3. Classes: ES6 brought a standardized class syntax, simplifying the creation of classes and objects using the 'class', 'constructor', and 'extends' keywords. This addition made object-oriented programming in JavaScript more familiar and concise.

4. Modules: ES6 introduced a standardized module system using the 'import' and 'export' keywords, enabling developers to organize code into reusable and maintainable modules. Modules enhance code encapsulation, facilitate dependency management, and improve performance through static analysis.

5. Template literals: Template literals provide a more expressive way to create strings, allowing embedded expressions and multiline strings using backticks (`) instead of single or double quotes. They enhance string manipulation and readability.

6. Enhanced object literals: ES6 enhanced object literals by introducing computed property names, shorthand property and method syntax, and the ability to define object methods without using the 'function' keyword.

7. Destructuring assignment: ES6 introduced destructuring assignment, offering a concise syntax to extract values from arrays or objects and assign them to variables. This simplifies code by eliminating the need for manual value extraction and enables more flexible data manipulation.

8. Promises: Promises became a built-in mechanism for handling asynchronous operations in a structured and intuitive manner. They enable developers to write asynchronous code that is easier to understand, avoiding callback hell and improving error handling.

9. Iterators and generators: ES6 introduced iterators and generators, which provide more flexible and controlled iteration over data structures. Iterators define a standardized way to traverse data, while generators offer a concise syntax for creating iterators.

These are just a few of the significant features introduced in ECMAScript 6. The improvements in ES6 made JavaScript more powerful, expressive, and easier to develop complex applications. Subsequent versions of ECMAScript have continued to build upon these foundations, introducing further enhancements and features to the language.

**//Q.5 What is the difference between let and const in ES6?**

//Solution--->

1. Mutability: Variables declared with 'let' are mutable, meaning their values can be changed or reassigned. In contrast, variables declared with 'const' are immutable, and their values cannot be modified once assigned.

2. Initialization: Variables declared with 'let' can be declared without an initial value and assigned later in the code. On the other hand, variables declared with 'const' must be initialized with a value at the time of declaration and cannot be left uninitialized.

3. Scope: Both 'let' and 'const' have block scope, which means they are limited to the nearest enclosing block, such as a function, loop, or conditional statement. They are not accessible outside that block.

4. Hoisting: Variables declared with 'let' and 'const' are hoisted to the top of their block scope, but unlike 'var', they are not initialized until the declaration statement is encountered. Accessing variables before their declaration within the same block leads to the Temporal Dead Zone and results in a 'ReferenceError'.

5. Reassignment: Variables declared with 'let' can be reassigned multiple times within their block scope. However, variables declared with 'const' cannot be reassigned after they are assigned a value. It's important to note that for complex types like objects and arrays assigned to 'const', their properties or elements can still be modified.

6. Best Practices: It is generally recommended to use 'const' for variables that are not intended to be reassigned, as it promotes immutability and makes the code's intent clearer. Use 'let' for variables that need to be reassigned or whose values may change over time.

To summarize, 'let' allows variable reassignment and is suitable for mutable variables, while 'const' enforces immutability and is appropriate for variables that should not be modified. Both 'let' and 'const' have block scope, are hoisted within their scope, and differ in terms of reassignment and initialization requirements.

**//Q.6  What is template literals in ES6 and how do you use them?**

//Solution--->

1. Basic string interpolation: Template literals enable you to embed variables or expressions within the string using ${}. The expressions inside ${} are evaluated and their values are inserted into the resulting string.

const name = 'Alice';
const greeting = `Hello, ${name}!`;
console.log(greeting); // Output: Hello, Alice!

2. Multiline strings: With template literals, creating multiline strings becomes effortless, as line breaks and indentation are preserved without the need for escape characters.

const multiline = 
` This is a
  multiline
  string.
`;
console.log(multiline);
/* Output:
   This is a
   multiline
   string.
*/

3. Expression evaluation: Template literals allow for the evaluation of expressions within ${}. This enables calculations or function calls directly within the template literal.

const a = 5;
const b = 10;
const sum = `The sum of ${a} and ${b} is ${a + b}.`;
console.log(sum); // Output: The sum of 5 and 10 is 15.

4. Tagged templates: Template literals can be used with a function, known as a "tag," to customize the evaluation and manipulation of the template. The tag function receives the template literal as separate arguments and can perform custom operations on the strings and values.

function customTag(strings, ...values) {
  // Manipulate the strings and values as needed
  return 'Customized result';
}

const result = customTag`This is a ${variable} template`;
console.log(result); // Output: Customized result

**//Q.7 What’s difference between map & forEach?**

//Solution--->

The map() and forEach() methods are both array iteration methods in JavaScript, but they differ in their behavior and the values they return. Here are the main differences between map() and forEach():

1. Return value:

map(): The map() method returns a new array by applying a provided function to each element of the original array. It creates a new array of the same length, with each element being the result of the callback function applied to the corresponding element of the original array.
forEach(): The forEach() method does not return anything. It iterates over each element of the array and executes a provided callback function on each element.

2. Purpose:

map(): map() is typically used when you need to transform each element of an array and collect the transformed values into a new array. It is useful for creating a new array based on the original array.
forEach(): forEach() is commonly used when you want to perform an action or execute a function for each element of the array without creating a new array. It is suitable for operations that do not require the creation of a new array.

3. Modification of the original array:

map(): The map() method does not modify the original array. Instead, it returns a new array containing the transformed values, leaving the original array unchanged.
forEach(): The forEach() method does not create a new array. However, it allows you to modify the elements of the original array directly within the callback function. It is not intended for transforming array elements like map().

4. Handling the result:

map(): Since map() returns a new array, you can assign its result to a variable or use it directly in further operations.

const numbers = [1, 2, 3];
const doubledNumbers = numbers.map(num => num * 2);
console.log(doubledNumbers); // Output: [2, 4, 6]

forEach(): As forEach() does not return anything, you cannot directly capture its result. It is primarily used for its side effects, such as logging or modifying array elements.

const numbers = [1, 2, 3];
numbers.forEach(num => console.log(num)); // Output: 1, 2, 3

**//Q.8 How can you destructure objects and arrays in ES6?**

//Solution--->

Destructuring, which allows you to extract values from arrays and properties from objects in a concise manner. Destructuring is a powerful technique that improves code readability and simplifies working with complex data structures. Let's explore how to destructure objects and arrays:

1. Destructuring Objects:
To destructure an object, you enclose the desired property names in curly braces ({}) on the left side of the assignment operator (=). The variable names on the left side should match the property names of the object you want to destructure.

const person = { name: 'Alice', age: 30 };
const { name, age } = person;

console.log(name); // Output: Alice
console.log(age);  // Output: 30

2. Destructuring Arrays:
To destructure an array, you enclose the desired element positions in square brackets ([]) on the left side of the assignment operator (=). The variables on the left side will receive the values from the corresponding positions in the array.

const numbers = [1, 2, 3];
const [a, b, c] = numbers;

console.log(a); // Output: 1
console.log(b); // Output: 2
console.log(c); // Output: 3

We can also skip elements in the array by leaving an empty slot (using commas) without assigning it to a variable:

const numbers = [1, 2, 3, 4, 5];
const [a, , c] = numbers;

console.log(a); // Output: 1
console.log(c); // Output: 3

Additionally, the rest syntax (...) can be used to assign the remaining elements of an array to a new array:

const numbers = [1, 2, 3, 4, 5];
const [a, ...rest] = numbers;

console.log(a);    // Output: 1
console.log(rest); // Output: [2, 3, 4, 5]

**//Q.9 How can you define default parameter values in ES6 functions?**

//Solution--->

In ECMAScript 2015 (ES6) and subsequent versions of JavaScript, you can define default parameter values for function parameters. Default parameters allow you to set a default value that will be used if no argument or an undefined argument is passed for that parameter. Here's how you can define default parameter values in ES6 functions:
function myFunction(param1, param2 = defaultValue) {
  // function body
}
In the above syntax:

param1 is a required parameter that must be provided when calling the function.
param2 is an optional parameter with a default value of defaultValue. If no argument is passed for param2 or if undefined is explicitly provided, the default value will be used.
Let's look at some examples to understand how default parameter values work:
function greet(name = 'Guest') {
  console.log(`Hello, ${name}!`);
}

greet();           // Output: Hello, Guest!
greet('Alice');    // Output: Hello, Alice!
greet(undefined);  // Output: Hello, Guest! (default value)

function addNumbers(a, b = 0) {
  console.log(a + b);
}

addNumbers(5, 10);    // Output: 15
addNumbers(5);        // Output: 5 (default value of 0 is used)
In the first example, the greet() function has a default parameter name set to 'Guest'. If no argument is provided, the default value is used. In the second example, the addNumbers() function has a default parameter b set to 0. If the second argument is not provided, the default value is used.

**//Q.10 What is the purpose of the spread operator (...) in ES6?**

//Solution--->

The spread operator (...) introduced in ECMAScript 2015 (ES6) and later versions of JavaScript serves various purposes and offers useful functionalities. Let's explore the purpose of the spread operator:

1. Array Spreading:
The spread operator allows you to unpack elements from an array or an iterable object. It expands an array into individual elements, which can be useful in scenarios where multiple arguments or elements are expected.

const numbers = [1, 2, 3];
console.log(...numbers); // Output: 1 2 3

const str = 'Hello';
console.log(...str);     // Output: H e l l o

2. Object Spreading:
The spread operator is also applicable to objects. It enables the spreading of properties from one object into another, allowing you to create a shallow copy or merge multiple objects together.

const obj1 = { x: 1, y: 2 };
const obj2 = { z: 3 };

const mergedObj = { ...obj1, ...obj2 };
console.log(mergedObj); // Output: { x: 1, y: 2, z: 3 }

3. Function Argument Spreading:
Within function calls, the spread operator can be used to spread out the elements of an array as individual arguments to the function.

function addNumbers(a, b, c) {
  console.log(a + b + c);
}

const numbers = [1, 2, 3];
addNumbers(...numbers); // Output: 6

4. Array and Object Literal Spreading:
The spread operator can be used within array and object literals to clone or create new arrays/objects by spreading the elements/properties of existing ones.

const originalArray = [1, 2, 3];
const clonedArray = [...originalArray];

const originalObject = { x: 1, y: 2 };
const clonedObject = { ...originalObject };

By using the spread operator in array and object literals, we can easily clone arrays or objects and create new ones by spreading the elements or properties of existing ones.


