# JS-React

## JS

1. What is DOM?<br/>
   DOM is a programming interface for web documents. it represents the document as node and objects which can be changed by any
   programming language.

2. is DOM part of JS?<br/>
   No DOM is not the part of JS.

3. What is window object in JS?<br/>

   - The Window interface represents a window containing a DOM document; the document property points to the DOM document loaded in that window.
   - A global variable, window, representing the window in which the script is running, is exposed to JavaScript code.

4. What is document?<br/>
   The Document interface represents any web page loaded in the browser and serves as an entry point into the web page's content, which is the DOM tree.

5. What is Execution context?<br/>
   Everything in js happens in Execution context. When js file runs for the first time it creates the execution context. Execution Context is nothing but a environment that handle transformation and execution of code.

   There are 2 types of execution context

   - Global Execution context(it is created when js file run for the first time and refer as global scope)
   - Function Execution context(it is created when function invoked and represent as local scope)

6. What are the 2 phase when js file executed?<br/>

   - variable environment(Memory allocation phase)
     - This is also called memory space where variable initialize to undefined and function body are kept as it is.
   - Thread of execution(code phase)
     - This is also now as code section where line by line execution started and value assign to variables and function invocation are done here.

7. Js is a synchronous single threaded language.<br/>

8. What is call stack?<br/>

   - In Js Call stack maintain the order of execution.
   - It is an mechanism for interpreted language like js in webbrowser, to keep track of functions.
   - when js calls a function it is added to call stack and starts executing that function.
   - Any function calls by that function added to call stack
   - when current function is finished, the interpreter takes it off from call stack.

9. what is Hoisting?

   - Javascript hoisting refers to use variable value in its scope before it's declared.
   - The value is always undefined.
   - variable declare with var can be used before it's declaration.
   - function, function*, async function, and async function* these functions declaration are hoisted with type 1 behavior
   - var declaration hoisted with type 2 behavior.
   - let, const and class declaration are hoisted with type 3 behavior.

10. What is arrow function how it's different from normal function?

- Arrow function is one of the way to writing function using => symbol.
- arrow function behave like a variable in memory allocation phase.
- 3 major differences are

  - arrow function does not support argument binding.

  ```
  let showData = {
        showArg: function(){
        console.log(arguments);
        }
     }
  showData.showArg(1,2,3); // output {0:1,1:2,2:3}

     // Object with Arrow function
     let showData = {
        showArg: ()=>console.log(arguments);
     }
     showData.showArg(1,2,3);
     // Uncaught ReferenceError: arguments is not defined
  ```

  - use of this keyword , in Regular function this depends on how the function is invoked but in arrow function its value remains same, it contains the value of closest non arrow function parent value
  - We can not use new keyword in arrow function, so arrow function can not be used as constructor function.

11. What is window in js?

- The Window interface represents a window containing a DOM document.the document property points to the DOM document loaded in that window.
- A global variable, window, representing the window in which the script is running, is exposed to JavaScript code.
- Window object is created by JS engine.

12. What happened when we run a JS file?

- When we run a Js file in browser it creates
  - Global Object
  - Global Context
  - this

13. What is undefined in JS?

- A variable that has not been assigned a value is of type undefined.
- undefined is primitive type in js.

14. What is scope in JS?

- Scope is current context of execution in which values and expressions are visible or can be referenced.
- if values and expression not in the scope they can not be available to use.
- Scopes can also be layered in a hierarchy, so that child scopes have access to parent scopes, but not vice versa.
- js has following types of scope
  - Global Scope - The default scope for all code running in script mode.
  - Module Scope - The Scope for code running in module mode.
  - Function Scope - The scope created wit function.
  - Block scope: The scope created with a pair of curly braces. (let const variables are belong to this scope)

15. What is lexical environment in js?

- A lexical environment is a data structure that holds identifier-variable mapping.
- identifier refers to the variable name and variable refers to actual object [ like function objet and primitive value]
- Lexical means hierarchy or sequence.
- when new execution context is created a new lexical environment is created and it is referenced in local Execution context in memory space
- Lexical Environment = local memory + lexical environment of its parent

- So in short, a lexical environment is a place where variables and functions live or physically present during the program execution.
- Global execution context's lexical environment parent is null

16. What is Scope chain?

- Scope chain is the chain of lexical environment.for example the inner function can access the variables of outer function.

17. What is let keyword in js?

- The let declaration declares a block-scoped local variable, optionally initializing it to a value.
- let allows you to declare variables that are limited to the scope of a block statement, or expression on which it is used.
- let and const does not create property in window object when declare globally.
- ```
      if (true) let a = 1; // SyntaxError: Lexical declaration cannot appear in a single-statement
  ```
- ##### Scope Rules

  - Variables declared by let have their scope in the block for which they are declared, as well as in any contained sub-blocks.

- Redeclaring the same variable within the same function or block scope raises a SyntaxError.

18. What is temporal dead zone?

- A let or const variable is said to be in a "temporal dead zone" (TDZ) from the start of the block until code execution reaches the line where the variable is declared and initialized.
- While inside the TDZ, the variable has not been initialized with a value, and any attempt to access it will result in a ReferenceError.
- This differs from var variables, which will return a value of undefined if they are accessed before they are declared.

19. What is lexical scope?

- Lexical scope is the definition area of expression.
- Lexical scope is the place in which the item got created.

20. What is const?

- The const declaration creates block-scoped constants, much like variables declared using the let keyword.
- The value of a constant can't be changed through reassignment (i.e. by using the assignment operator), and it can't be redeclared (i.e. through a variable declaration).

21. Functions in JS?

- JS functions are called first class objects, because they can be passed to other functions, returned from functions and assigned to variables and properties.

22. Types of functions in JS?

- Regular function: can return anything; always runs to completion after invocation
- Generator function: returns a Generator object; can be paused and resumed with the yield operator
- Async function: returns a Promise; can be paused and resumed with the await operator
- Async generator function: returns an AsyncGenerator object; both the await and yield operators can be used

23. what is function statement?

- Function definition is the function statement.

24. What is function expression?

- Hoisting makes the difference between function expression and function statement.
- The function declaration creates functions that are hoisted. Other syntaxes do not hoist the function and the function value is only visible after the definition.

25. What is function declaration?

- Function declaration is same as function statement.

26. What is anonymous function?

- It is a function that does not have any name associated with it. Normally we use the function keyword before the function name to define a function in JavaScript, however, in anonymous functions in JavaScript, we use only the function keyword without the function name.
- An anonymous function is not accessible after its initial creation, it can only be accessed by a variable it is stored in as a function as a value. An anonymous function can also have multiple arguments, but only one expression.

27. Different between parameters and arguments?

- Parameters are in function declaration, when we pass value in function call is called function arguments.

28. What is callback?

- A callback function is a function passed into another function as an argument, which is then invoked inside the outer function to complete some kind of routine or action.

29. What is closure?

- A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function's scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

30. What is event loop?

- Js is a synchronous single threaded programming language.
- Question is how Js manage to do concurrent, non blocking and async operation? These things are handled by concurrency model provided by JS.
- ###### Call stack ###### :

  - Js maintain a stack to track the function calls, When we call any function in js,then execution context is created for tat function and pushed into the stack.
  - When function execution finished it's popped out from stack, this process is happened in all function calls in JS.

- ###### callback queue ####### :
  - Js maintain a queue to manage events or callback;
  - When a async function is called in js, it will create a execution context and pushed into the call stack, but immediately it pops and gives to the WEB API(for example setTimeOut() is stored in the timer API provide by browser, here are many other API like WEB API, LOCAL STORAGE API etc ).
  - In the Web API the callback waits until finish processing of this task, for example if setTimeOut((){}, 1000), i will be in web api for 1000 sec then it will added to call back queue.
- ###### event queue ###### :
  - Event loop sits in between call stack and callback queue, there is only one task of queue, it will constantly check the call stack and when the stack is empty it will pull callback from callback queue and pushed into the call stack.

31. What is micro task queue?

- Micro task queue is similar to callback queue but it has more priority than callback queue. All the callback coming through Promises and Mutation Observer will go inside micro task queue. For example fetch() callback queue will gets to the micro task queue.
