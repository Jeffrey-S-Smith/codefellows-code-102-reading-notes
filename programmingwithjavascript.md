# Programming with JavaScript

## Author

Jeffrey Smith

## Programming JavaScript

## Function

What is a function is a block of code designed to perform a particular task you want it to do.

functions excutes when something invokes it (call it).  

EXAMPLE

function myFunction(p1, p2) {
  return p1 * p2;   // The function returns the product of p1 and p2
}

## Function Syntax

Function is defined with a keyword followed ba a name followed by parentheses ().

The names can contain letters, digits, underscores, and dollar signs (same rules as variables).

The parentheses may include parameter names separated by commas:
(parameter1, parameter2, ...)

The code to be executed, by the function, is placed inside curly brackets: {}

function name(param1, param 2, parm3) { code to be excuted }

Function parameters are listed inside the parentheses () in the function definition.

Function arguments are the values received by the function when it is invoked.

Inside the function, the arguments (the parameters) behave as local variables.

## Function Invocation

Inside the code the function will execute when "something" invokes (calls) the function:

- When an event occurs (when a user clicks a button)
- When it is invoked (called) from JavaScript code
- Automatically (self invoked)

## Function Return

When JavaScript reaches a return statement, the function will stop executing.

Function often compute a return value and return it back to the caller.

EXAMPLE

let x = myFunction(4, 3);   // Function is called, return value will end up in x

function myFunction(a, b) {
  return a * b;             // Function returns the product of a and b
}

The result in X will come back as 12

## Why Functions?

Because we can reuse code: Define the code once and use it may times.

Because you can use the same code manytimes with many arguments, to produce different results.

EXAMPLE

Convert Fahrenheit to Celsius:

function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius(77);

## The () Operator Invokes the Function

Using the example above toCelsius refers to the function object, and toCelsius() refers to the function result.

Accessing a function without () will return the function object instead of the function result.

EXAMPLE

function toCelsius(fahrenheit) {
  return (5/9) * (fahrenheit-32);
}
document.getElementById("demo").innerHTML = toCelsius;

## Functions Used as Variable Values

Functions can be used the same way you can use variables in all types of formulas, assignments, and calculations.

EXAMPLE

Instead of using a variable to store the return value of a function:

let x = toCelsius(77);
let text = "The temperature is " + x + " Celsius";

You can use the function directly, as a variable value:

let text = "The temperature is " + toCelsius(77) + " Celsius";

## Local Variables

Variables declared in JavaScript functions, become LOCAL to the function.

Local variables can only be accessed from within the function.

EXAMPLE

// code here can NOT use carName

function myFunction() {
  let carName = "Volvo";
  // code here CAN use carName
}

// code here can NOT use carName

https://www.w3schools.com/js/js_functions.asp

## Operation

## JavaScript Operators

EXAMPLE

Assign values to variables and add them together:

let x = 5;         // assign the value 5 to x
let y = 2;         // assign the value 2 to y
let z = x + y;     // assign the value 7 to z (5 + 2)

The assignment operator (=) assigns a value to a variable.

The addition operator (+) adds numbers:

let x = 5;
let y = 2;
let z = x + y;

The multiplication operator (*) multiplies numbers.

let x = 5;
let y = 2;
let z = x * y;

## JavaScript Arithmetic Operators

- Addition +
- Subtraction -
- Multiplication
- Exponentiation (ES2016) **
- Division /
- Modulus (Division Remainder) %
- Increment ++
- Decrement --

https://www.w3schools.com/js/js_operators.asp