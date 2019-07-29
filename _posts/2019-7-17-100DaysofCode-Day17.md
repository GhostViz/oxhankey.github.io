---
layout: post
title: 100 Days of Code - Day 17
category: freeCodeCamp
permalink: 100DaysofCode/day17
---

Today is Day 17 of #100DaysofCode. I am continuing the Basic Algorithm Scripting module from [FreeCodeCamp.org](https://freecodecamp.org).

I completed the Finders Keepers, Boo who, Title Case a Sentence, Slice and Splice, and Falsy Bouncer Challenges.

### Finders Keepers

Create a function that looks through an array `arr` and returns the first element in the array that passes the test `func`. If no elements pass return `undefined`.

**Solution:**

For this challenge I looped through each element in the array while passing that element to the function `func`. If it was true I returned the element. If the entire loop was performed without a true response I returned `undefinded`.

```JavaScript
function findElement(arr, func) {
  for (let element in arr) {
    let num = arr[element];
    if (func(num)) {
      return num;
    }
  }
  return undefined;
}
```

### Boo who

Check if a value is classified as a boolean primitive. Return true or false.

**Solution:**

For this challenge I used typeof to evaluate if `bool` was boolean or not.

```JavaScript
function booWho(bool) {
  return typeof bool === 'boolean';
}
```

### Title Case a Sentence

Return the provided string with the first letter of each word capitalized. Make sure the rest of the word is in lower case.

For the purpose of this exercise, you should also capitalize connecting words like "the" and "of".

**Solution:**

For this challenge I created an array `arr` from the string `str`. Then I looped through `arr` and converted the first character to upper case then added the rest of the of the string back in lower case pushing each new string to a new array `newArr`. Once the loop was completed I returned newArr as a string using `join(" ")`.

```JavaScript
function titleCase(str) {
  let arr = str.split(" ");
  let newArr = [];
  for (let element in arr) {
    newArr.push(arr[element].charAt(0).toUpperCase() + arr[element].slice(1).toLowerCase());  
  }
  return newArr.join(" ");
}
```

### Slice and Splice

You are given two arrays and an index.

Use the array methods slice and splice to copy each element of the first array into the second array, in order.

Begin inserting elements at index n of the second array.

Return the resulting array. The input arrays should remain the same after the function runs.

**Solution:**

For this challenge I created a new array `myArr` from array 2. Then I looped through `arr1` and spliced the the current element into `myArr` at the `n` index before incrementing `n` for the next pass. Once the loop was done I returned `myArr`.

```JavaScript
function frankenSplice(arr1, arr2, n) {
  let myArr = arr2.slice();
  for (let element in arr1) {
    myArr.splice(n, 0, arr1[element]);
    n++;
  }
  return myArr;
}
```

### Falsy Bouncer

Remove all falsy values from an array.

Falsy values in JavaScript are false, null, 0, "", undefined, and NaN.

**Solution:**

For this challenge I used `filter()` to create a new array from array elements in `arr` that pass the `Boolean` test.

```JavaScript
function bouncer(arr) {
  return arr.filter(Boolean);
}
```
