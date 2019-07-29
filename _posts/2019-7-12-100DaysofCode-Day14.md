---
layout: post
title: 100 Days of Code - Day 14
category: freeCodeCamp
permalink: 100DaysofCode/day14
---

Today is Day 14 of #100DaysofCode. I am continuing the Basic Algorithm Scripting module from [FreeCodeCamp.org](https://freecodecamp.org).

I completed the Factorialize a Number and Find Longest Word Length challenges.

**Factorialize a Number**
To factorialize a number you multiply all positive integers less than or equal to a number. The result is called n-Factorial with n being the number. For example 5 Factorial is 120.

For this challenge I started out by defining my total as 1. After that I created a for loop which incremented from 2 (remember 0 and 1 are both covered by total = 1 already) to the number we wished to factorialize. Finally I returned the total. 

```JavaScript
function factorialize(num) {
  let total = 1;
  for (let i = 2; i <= num; i++) {
    total *= i;
  }
  return total;
}
```

**Find Longest Word Length**
For the Find Longest Word Length challenge I actually solved it two different ways. Both solutions used a largestStr variabe and split the given string into an array of strings.

The first way I solved it was by using a for loop with `in` and looped through each element in the array checking the length against value of `largestStr` and adjusting the value if necessary.

```JavaScript
function findLongestWordLength(str) {
  let strArray = str.split(" ");
  let largestStr = 0;
  for (let strs in strArray){
    if (largestStr < strArray[strs].length) {
      largestStr = strArray[strs].length;
    }
  }
  return largestStr;
}
```

The second way I solved it was by using a for loop and incrementing through each
index until I reached the end. The process I used inside the loop for each solution is the same.

```JavaScript
function findLongestWordLength(str) {
  let strArray = str.split(" ");
  let largestStr = 0;
  for (let i = 0; i < strArray.length; i++){
    if (largestStr < strArray[i].length) {
      largestStr = strArray[i].length;
    }
  }
  return largestStr;
}
```
