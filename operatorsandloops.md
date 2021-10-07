# Operators and Loops

## Author

Jeffrey Smith

## Expressions and operators

This chapter describes JavaScript's expressions and operators, including assignment, comparison, arithmetic, bitwise, logical, string, ternary and more.

A complete and detailed list of operators and expressions is also available in the reference.

## Operators

- Assignment operators
- Comparison operators
- Arithmetic operators
- Bitwise operators
- Logical operators
- String operators
- Conditional (ternary) operator
- Comma operator
- Unary operators
- Relational operators

## Assignment operators

Addition assignment
Subtraction assignment
Multiplication assignment
Division assignment
Remainder assignment
Exponentiation assignment
Left shift assignment
Right shift assignment
Unsigned right shift assignment
Bitwise AND assignment
Bitwise XOR assignment
Bitwise OR assignment
Logical AND assignment
Logical OR assignment
Logical nullish assignment

## Comparison operators

- == compares operands
- <> not equal to
- < less than
- (>) greater than
- <= less than or equal to
- (>=) greater than or equal to
- !~ does not contain
- ~ string comparison
- like
- === Strict equal

## Arithmetic operators


https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators

## Loops

For statement

For loop repeats until a specified condition evaluates to false. The JavaScript for loop is similar to the Java and C for loop.

When a for loop executes, the following occurs:

The initializing expression initialExpression, if any, is executed. This expression usually initializes one or more loop counters, but the syntax allows an expression of any degree of complexity. This expression can also declare variables.
The conditionExpression expression is evaluated. If the value of conditionExpression is true, the loop statements execute. If the value of condition is false, the for loop terminates. (If the condition expression is omitted entirely, the condition is assumed to be true.)
The statement executes. To execute multiple statements, use a block statement ({ ... }) to group those statements.
If present, the update expression incrementExpression is executed.
Control returns to Step 2.

EXAMPLE

for(int x = 10; x < 20; x = x + 1) {
         System.out.print("value of x : " + x );
         System.out.print("\n");
    } 

## do...while statement

do
  statement
while (condition);

Example

let i = 0;
do {
  i += 1;
  console.log(i);
} while (i < 5);

## while statement

This statement executes its statements as long as a specified condition evaluates to true. A while statement looks as follows:

while (condition)
  statement

If the *condition *becomes false, statement within the loop stops executing and control passes to the statement following the loop.

he condition test occurs before statement in the loop is executed. If the condition returns true, statement is executed and the condition is tested again. If the condition returns false, execution stops, and control is passed to the statement following while.

Example 1

let n = 0;
let x = 0;
while (n < 3) {
  n++;
  x += n;
}

With each iteration, the loop increments n and adds that value to x. Therefore, x and n take on the following values:

Example 2

// Infinite loops are bad!
while (true) {
  console.log('Hello, world!');
}

## labeled statement

provides a statement with an identifier that lets you refer to it elsewhere in your program.

Example
markLoop:
while (theMark === true) {
   doSomething();
}

## break statement

statement to terminate a loop

break;
break [label];

Example 1

for (let i = 0; i < a.length; i++) {
  if (a[i] === theValue) {
    break;
  }
}

Example 2

et x = 0;
let z = 0;
labelCancelLoops: while (true) {
  console.log('Outer loops: ' + x);
  x += 1;
  z = 1;
  while (true) {
    console.log('Inner loops: ' + z);
    z += 1;
    if (z === 10 && x === 10) {
      break labelCancelLoops;
    } else if (z === 10) {
      break;
    }
  }
}

## continue statement

statement can be used to restart a while, do-while, for, or label statement.

When you use continue without a label, it terminates the current iteration of the innermost enclosing while, do-while, or for statement and continues execution of the loop with the next iteration

In contrast to the break statement, continue does not terminate the execution of the loop entirely.

In a while loop, it jumps back to the condition. In a for loop, it jumps to the increment-expression

continue [label];

Example 1

The following example shows a while loop with a continue statement that executes when the value of i is 3. Thus, n takes on the values 1, 3, 7, and 12.

let i = 0;
let n = 0;
while (i < 5) {
  i++;
  if (i === 3) {
    continue;
  }
  n += i;
  console.log(n);
}
//1,3,7,12

let i = 0;
let n = 0;
while (i < 5) {
  i++;
  if (i === 3) {
     // continue;
  }
  n += i;
  console.log(n);
}
// 1,3,6,10,15

Example 2

If continue had a label of checkiandj, the program would continue at the top of the checkiandj statement.

let i = 0;
let j = 10;
checkiandj:
  while (i < 4) {
    console.log(i);
    i += 1;
    checkj:
      while (j > 4) {
        console.log(j);
        j -= 1;
        if ((j % 2) === 0) {
          continue checkj;
        }
        console.log(j + ' is odd.');
      }
      console.log('i = ' + i);
      console.log('j = ' + j);

## for...in statement

statement iterates a specified variable over all the enumerable properties of an object. 

Example

The following function takes as its argument an object and the object's name. It then iterates over all the object's properties and returns a string that lists the property names and their values.

function dump_props(obj, obj_name) {
  let result = '';
  for (let i in obj) {
    result += obj_name + '.' + i + ' = ' + obj[i] + '<br>';
  }
  result += '<hr>';
  return result;
}
Copy to Clipboard
For an object car with properties make and model, result would be:

car.make = Ford
car.model = Mustang

## Arrays
Although it may be tempting to use this as a way to iterate over Array elements, the for...in statement will return the name of your user-defined properties in addition to the numeric indexes.

## for...of statement 

for (variable of object)
  statement
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Loops_and_iteration