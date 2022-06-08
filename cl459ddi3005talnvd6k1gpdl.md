## Swapping Values Using Arithmetic Operations in JavaScript

Assume we have two variables ```a``` and ```b```:
```
let a = 5;
let b = 7;
``` 
Let us swap the values. First we get the sum of the two variables and assign it to ```a```

```
a = a + b; // a = 12
``` 
Now, let us reasign the value of ```b``` with the value of ```a``` by getting the difference

```
b = a - b;  // b = 12 - 7 = 5
``` 

Now, let us reasign the value of ```a``` with the value of ```b``` by getting the difference

```
a = a - b;  // b = 12 - 5 = 7
``` 

Let us see what our variables have by printing them out.

```
console.log(a); // 7
console.log(b); // 5
``` 

This is how the whole code should look like:

```
let a = 5;
let b = 7;
console.log('The value of a and b before swapping.');
console.log('The value of a is, ' a); // The value of a is 5
console.log('The value of b is, ' b); // The value of b is 7
// Get the sum
a = a + b; // a = 12
// Reasign b with the value of a
b = a - b;  // b = 12 - 7 = 5
// Reasign a with the value of b
a = a - b;  // b = 12 - 5 = 7
console.log('The value of a and b after swapping.');
console.log('The value of a is, ' a); // The value of a is 7
console.log('The value of b is, ' b); // The value of b is 5
``` 

That is it! We have swapped our values using arithmetic operations.