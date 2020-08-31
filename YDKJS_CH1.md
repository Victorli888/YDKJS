## Chapter 1: Into Programming
###Statements
In Javascript a statement looks like this:
```js
a = b  + 3;
```
Keywords to know: *Variable Expression, Literal Value, 
Operators, Arithmetic Expression, Assignment Expression,*

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
