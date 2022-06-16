## Remove Duplicates From Array

Assume we have a list of numbers that looks like this:

```js
[1, 2, 4, 5, 4, 2];
```

## How can we remove the duplicates?
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2z4qrs3lfe2p1uz277lp.gif)
 

In this short tutorial, we are going to learn two methods that we can use to remove duplicates from an array.


## 1. Use a `for-loop`?

```js
let numbers = [1, 2, 4, 5, 4, 2];
let numbersWithoutDuplicates = [];
for (let i = 0; i < numbers.length; i++) {
  if (!numbersWithoutDuplicates.includes(numbers[i])) {
    numbersWithoutDuplicates.push(numbers[i]);
  }
}

console.log(numbersWithoutDuplicates);
// => [ 1, 2, 4, 5 ]
```

### What are we doing here?

1. We have declared a `numbersWithoutDuplicates` and assigned to an empty array. This variable will finally hold our numbers after removing duplicates

1. We are iterating through all the numbers using a for-loop

1. For each iteration, we are checking if the current number is in our `numbersWithoutDuplicates` array.

1. If the current number is in the array, we do nothing, otherwise we add the number

1. Finally, we are printing out our non-duplicate array

The for-loop can be re-written much more succinctly using a `for-of` loop as below:
```js
let numbers = [1, 2, 4, 5, 4, 2];
let numbersWithoutDuplicates = [];
for (let number of numbers) {
  if (!numbersWithoutDuplicates.includes(numbers) {
    numbersWithoutDuplicates.push(number);
  }
}

console.log(numbersWithoutDuplicates);
// => [ 1, 2, 4, 5 ]
```

## 1. Use Set?
We can use a set to automatically exclude duplicates from our array.

> Mathematically, a set is a collection of items where order and repetition is ignored.

In JavaScript we can create a set out of an array object and this will simply eliminate the duplicates.

Let us see how this works:

```js
let numbers = [1, 2, 4, 5, 4, 2];
let setOfNumbers = new Set(numbers); //=> {1, 2, 4, 5}

// populate the numbersWithoutDuplicates with setOfNumbers
// using the spread operator
let numbersWithoutDuplicates = [...setOfNumbers];

console.log(numbersWithoutDuplicates);
// => [ 1, 2, 4, 5 ]
```

## Yaahs! 
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vm9yga2vnq3dy31j82iz.gif)
We just learned two methods on how to remove duplicates from an array. 

Go and try them out!
 
