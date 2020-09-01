## Chapter 1: Into Programming
### Statements
In Javascript a statement looks like this:
```js
a = b  + 3;
```
Keywords to know: 
* Variable Expression
* Literal Value
* Operators
* Arithmetic Expression
* Assignment 
* Expression

### Executing a Program
**The Compiler or Interpreter** translates your code to machine code that the computer can understand.
 
*The Interpreter* will typically translate code top to bottom, line by line everytime the code is run
 
*The Compiler* the translation is done ahead of time, so when the program runs later what's running is actually already
compiled computer instructions.

JavaScript is an interpreted language because the source code is processed each time you run it.
But, the JavaScript engine actually compiles the program on the fly and then immediately runs the compiled code.

```js
a = 21;
b = a * 2;
console.log(b);
```
`log(b)` is referred to the function `console` is the object reference where `log(...)` function is located

#### Generating an Input
```js
age = prompt("Please tell me your age: ");
console.log(age);
```
The input is stored as age, and we use `console.log(age)` to output the variable
### Operators
```js
var a = 20
```
Use `var` to declare a variable

* *Increment* `++` `--` (very similar to a = a + 1)
* *Equality* `==` `===`(strict equal) `!=` `!==` (strict not equal)
* *Logical* `a && b` `a || b` 

### Value, Types, and Converting between Types
```js
var a = "42";
var b = Number(a);
var c = String(b);
```
Using **loose operators** will implicitly coerce values to their matching types.
```js
"99.99" == 99.99
```
The comparison then becomes which is true
```js
99.99 == 99.99 // True
```
### Code Comments
* Code without comments is suboptimal
* Too many Comments are a sign of poorly written code 
* Comments should explain why not what
```js
// Single in Comment

/* This is a
multiline
comment */
```
Program Example:
```js
var amount  = 99.99;
amount *= 2;
console.log(amount); // 199.98
var cash_amount = "$" + String(amount)
console.log(cash_amount) // $199.98
```

### Blocks
Use  curly braces `{...}` for a general box

### Conditionals
```js
const Item_price = 9.99

var bank_account = 117.98

// Can we afford this purchase?
if (Item_price <= bank_account) {
    console.log("Yes I can afford this item");
}
// Otherwise 
else {
    console.log("No I can't afford this item");
}
```
### Loops
A While loop will continue as long as the condition remains true.
```js
num_of_customers = 4

while (num_of_customers > 0) {
    console.log("How many I help you?");
    // help the customer...
    num_of_customers -= 1;
}

// versus:

do {
    console.log("How may I help you?");

    // help the customer...
    num_of_customers -= 1;
} while(num_of_customers > 0);
```
### Functions
`toFixed(2)` Method is Converts a number to a string, and rounds to the nearest two decimals.
By default `toFixed()` will reduce to the nearest whole integer.
```js
function printAmount(amt){
    console.log(amt.toFixed(2));
}

function formatAmount(){
    return "$" + amount.toFixed(2);
}

var amount = 99.99;

printAmount(amount * 2); // 199.98

amount = formatAmount();
console.log(amount);    //$99.99
```
### Scope
functions have their own scope and so a variables from another function can't be accessed 
in a **Nested Loop** the inner loop can access the outer loops variable. **BUT** only the inner loop can.
```js
function outer() {
    var a = 1;

    function  inner() {
        var b = 2;
        console.log(a+b)
        // In here we can access both 'a' and 'b' here
    }
    
    inner();
    // out here we can only access 'a'
    console.log(a);
}
outer();
```