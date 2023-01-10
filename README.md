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

## React
