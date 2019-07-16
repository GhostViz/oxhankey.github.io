---
layout: post
title: 100 Days of Code - Day 16
category: 100 Days of Code
permalink: 100DaysofCode/day16
---

Today is Day 16 of #100DaysofCode. I am continuing the Basic Algorithm Scripting module from [FreeCodeCamp.org](https://freecodecamp.org).

I completed the Factorialize a Number and Find Longest Word Length challenges.

### Return Largest Numbers in Arrays

For this challenge I was given an array containing four arrays of four integers and was told to return an array with the maximum integer from each array.

**Solution:**

I used a loop to loop through each element in the array `arr` and pushed the maximum integer to `newArr`. To do this I utilized `Math.max`.

> A note about this solution: The instructions said one could always assume 4 integers and 4 arrays of integers. Using `for (arrs in arr)` will loop through an infinite number of integers and Math.max will find the max no matter the number of integers in the array so it will work for the problem at any size.

```JavaScript
function largestOfFour(arr) {
  let newArr = [];
  for (let arrs in arr) {
    newArr.push(Math.max.apply(null,arr[arrs]))
  }
  return newArr;
}
```

### Confirm Ending
For this challenge I was supposed to check the ending of a string `str` to see if it matches a target `target`.

**Solution:**

I simply used `str.slice()` to check the last `target.length` number of characters against `target`. The return of this comparison was already boolean.

```JavaScript
function confirmEnding(str, target) {
  return target === str.slice(-target.length);
}
```

### Repeat a String
For this challenge I was supposed to repeat a string `num` times without using `string.repeat()`. If the number was 0 or under it should return `""`.

**Solution:**

The first thing I did is check if the number was 0 or less. If it was I returned `""`. If the number was greater than 0 I looped through adding `str` to a new string `newStr` `num` times and returned `newStr`.

```JavaScript
function repeatStringNumTimes(str, num) {
  if (num <= 0) {
    return ""
  } else {
    let newStr = str;
    for (let i = 1; i < num; i++) {
      newStr += str;
    }
    return newStr;
  }
}
```

### Truncate a String
For this challenge I was given a string `str` and a number `num` and told to truncate `str` to `num` characters.

**Solution:**

I checked that the length of `str` was greater than `num` and if it was I used `str.slice()` to return `num` of strings with "..." concatenated to the end.  If `num` was equal to or greater than `str.length` I returned `str`.

```JavaScript
function truncateString(str, num) {
  if (str.length > num) {
    return str.slice(0,num) + "...";
  } else {
    return str;
  }
}
```
