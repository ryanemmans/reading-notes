# COMPUTER LOGIC - Operators and Loops

Expressions and operators:

- Binary and unary operators, and conditional operator (ternary)
- Operand - the part of a computer instruction which specifies what data is to be manipulated or operated on

## **Expressions** - any valid unit of code that resolves to a value

Assignment Operators:

- Assigns value to left operand based on value of right operand
- Compound assignment operators are shorthand operations. Ex: `x += y` means `x = x + y`
- The *return value* matches expression to right of the `=` sign
- Logical Assignment Ex: `(x &&= y)`, return value is `x && y` - return value is same without assignment/equal sign
- Return values are always based on the operands’ values *before* the operation.

Assignments are evaluated right-to-left when chaining expressions

- Ex: `w = z = x = y` is the same as `w = (z = (x=y))`, or `x = y; z = y; w = y`

Destructuring for complex assignments

- JavaScript expression that makes it possible to extract data from arrays or objects using a syntax that mirrors construction of array and object literals (WHAT?)

Comparison Operators - compare operands and return logical value based on whether comparison is `true`

- Operands can be numerical, string, logical, or object values
- `(==)` Equal
- `(!=)` Not equal
- `(===)` Strict equal
- `(!==)` Strict not equal
- `(>)` Greater than
- `(>=)` Greater than or equal
- `(<)` Less than
- `(<=)` Less than or equal

Arithmetic Operators - take numerical values (either literals or variables) as operands and return a single numeric value (`+`) (`-`) (`*`) (`/`)

- `%` Remainder
- (`++`) Increment
- (`—`) Decrement
- (`-`) Unary negation
- (`+`) Unary plus
- (`**`) Exponentiation

Bitwise Operators - performed on binary representations, treats operands as set of 32 bits (0s and 1s)

Logical Operators - used with Boolean (logical) values

- (`&&`) AND
- (`||`) OR
- (`!`) NOT

Conditional operators - only operators that take three operands - can have one of two values based on a condition.

## **LOOPS - offer a quick and easy way to do something repeatedly**

- Repeat an action x number of times

**For** Statement Loop - repeats until a specified condition evaluates to `false`

- Used when you know how many times you run your loop
- For statement is initilization statement
- If condition is true, the loop statements execute. If false, loop terminates. (If omitted entirely, the condition is assumed to be true.)

**Standard** While Loop and do while loop

- While Loop executes its statement as long as condition evaluates to true.
- If false, loop stops and control passes to following loop
- Make sure condition eventually becomes false, or it will become an infinite loop (Avoid!!)

[back](../README.md)
