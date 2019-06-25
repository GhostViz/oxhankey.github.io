---
layout: post
title: 100 Days of Code - Day 2
category: 100 Days of Code
permalink: 100DaysofCode/day2
---

Today was Day 2 of #100DaysOfCode, and I learned about arrays and multi-dimensional arrays. I learned that while items in an array can be accessed like characters in a string, a string is not an array of characters because it is immutable. That means it's characters can not be freely changed. An array is mutable, mean items in an array can be freely changed.

I also learned about the queue data structure in which items are kept in order, and I wrote a function taking advantage of push and shift to implement a queue.

```
function nextInLine(arr, item) {
  arr.push(item);
  var next = arr.shift();
  return next;
}

var testArr = [1,2,3,4,5];

console.log("Before: " + JSON.stringify(testArr));
console.log(nextInLine(testArr, 6)); // Modify this line to test
console.log("After: " + JSON.stringify(testArr));
```
> .push - append to the end of an Array <br />
> .pop - removed from end of array<br />
> .shift - removed from beginning of array<br />
> .unshift - append to the beginning of array<br />

In addition to these things I learned about global and local scope. In javascript variables that are declared without var are [hoisted](https://www.w3schools.com/js/js_hoisting.asp) into the global scope and interpreted as being declared at the top of the code. While hoisting is the default behavior for JavaScript it is still best practice to declare all variables at the top to avoid confusion for other programmers. This also ensures the code reads as it is interpreted.

More to come tomorrow!
