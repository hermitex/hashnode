## What are th Types of Functions in JavaScript?

## What is a Function
A function is a block of reusable code that performs a specific task.

There are 3 types of functions in JavaScript:
<ul>
<li>Anonymous functions</li>
<li>Named functions</li>
<li>Immediately Invoked Function Expression</li>
</ul>

## Anonymous Functions
These are functions are functions without names attached to them. Typically, these functions will be declared with the ```function``` keyword but without a name.

The syntax of an anonymous function looks like:
```
// declaring an anonymous function
function(){
 // function body
}
```
Here is an example of an anonymous function:
```
// declaring an anonymous function
function(){
  console.log('I am anonymous!'); // I am anonymous!
}
```
In the above example, we have defined an anonymous function that prints out the string *'I am anonymous!'* to the console.

It is important to note that we cannot access the anonymous fuction after its creation.  However, if we want to access it, we can assign the function to a variable.
```
// declaring an anonymous function
let anonymousFun = function(){
  console.log('I am anonymous!'); 
}
anonymousFun(); // I am anonymous!
```

## Named Functions
These are functions which on declaration, they are assigned a name. This allows us to access the function later on just by referencing the name of the function.
The general syntax looks like:

```
function functionName(/*parameters*/){
  // function body
}
``` 

Here is an example of a named function:
```
function myNamedFun(){
   console.log('I am a named function'); 
}

// accessing the function
myNamedFun(); // I am a named function

``` 


## Immediately Invoked Function Expression
Immediately Invoked Function Execution(IIFE) is a function that executes immediately after its declaration.
The general syntax for IIFEs looks like:

```
(
  function(){
    // function body
}
)()
``` 

Here is an example of a IIFE function:
```
(function immediatelyInvoked(){
   console.log('I will execute imediately!');  // I will execute imediately!
})();

``` 

I like thinking about IIFEs as code blocks that live in their 'own environment' such that they are not affected by any other code that will execute thereafter.

You can find the IIFE helpful when you want to quickly initialize variables or objects in a larger function.

If you are keen, you must have noticed that the IIFE is more of an anonymous function. Therefore, we can assign them a variable and later on use the variable as shown below:

```
let myFun = (function immediatelyInvoked(){
   return 'I will execute imediately!';  
})();

console.log(myFun) // I will execute imediately!
``` 

## Key Takeaways

<ol>
<li>A function is a block of reusable code that perfoms a specific task</li>
<li>There are 3 types of functions in JavaScript:</li>
  <ul>
<li>Anonymous functions</li>
<li>Named functions</li>
<li>Immediately Invoked Function Expression</li>
</ul>
</ol>








