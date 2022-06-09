## Pass Functions as Arguments in JavaScript?

Having looked at [types of functions in JavaScript](https://tiberiusmairura.hashnode.dev/what-are-the-types-of-functions-in-javascript) it is high time we delve a bit deeper. We know that, in programming, we can populate our function's parameter with arguments. But did you know that in JavaScript you can pass a function as an argument to another function? 

Well, in this short article, we are going to see how this can be done using a few examples. To do that, we are going to define two functions `returnSomething` and `something`. Let's do it!

```
function returnSomething(something){
return something;
}

function something(){
let myThings = ['Trousers', 'Cat', 'Pen'];
myThings.push('Laptop');
console.log(mythings);
}

returnSomething(something) 
```

If you run the code snippet above in your browser console, you will see the following output:

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/oshiyjkvxeazvrofsioh.png)

If you look closely, you will notice that the function was returned without being executed. This function will have access to all, well, "things" defined inside the returnSomething function and this includes local variables, other parameters, etc.

## How can we Invoke this Function?
Well, if we want to execute this function, we can append the () at the end of the function like this:
```
function returnSomething(something){
return something();
}

function something(){
let myThings = ['Trousers', 'Cat', 'Pen'];
myThings.push('Laptop');
console.log(mythings);
}

returnSomething(something); 
```
Running this code on the console will show the following result:

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/diq9rx3flf3kutobjw9n.png)

This is all possible because in JavaScript functions are first class objects. This means that functions can be passed around like any other value, and this includes being passed to another function just as we have demonstrated above. This might seem to be a simple concept, but it builds up on a more useful concept called callback functions. 

## Callback Functions

When a function is passed to another function, like we've done above, whereby it may or may not be invoked immediately, we call it a callback function.

A good example of how a callback function is used is when you attach event listeners to HTML elements and then perform some action when the event is triggered.

Building on the knowledge above, let us see how a callback function works using `makeCoffeeFor` and `orderCoffee` functions as examples.

```
function makeCoffeeFor(name, order){
return order(name);
}

makeCoffeeFor('Tiberius', function(name){console.log(`${name}, your coffee is being prepared!`)});
```
The result of executing the above snippet is as shown below:

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/x6x0cimaw5r828g5j1ab.png)

In practice, callback functions become extremely helpful especially when when the parent(the function in which they are passed to) is performing some expensive operations for instance scraping data from a website. The data scraped can then be passed back to the callback.
```
function expensiveOperation(callback){
// find the right website
// scrape the right data
// clean the data
return callback(data); // pass the cleaned data back to the callback
}

expensiveOperation(function(data){console.log(data)});
```
Great! We've come a long way and we've learn't a couple of concepts.

## Key Takeaways

- Functions are _**first class objects**_ in JavaScript

- Therefore, they can be passed around as values and this includes passing them to other functions

- A function passed to another function to be executed later is called a **_callback function_**
