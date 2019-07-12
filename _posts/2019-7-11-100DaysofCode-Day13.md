---
layout: post
title: 100 Days of Code - Day 13
category: 100 Days of Code
permalink: 100DaysofCode/day13
---

Today is Day 13 of #100DaysofCode. I started and completed the Basic Algorithm Scripting module from [FreeCodeCamp.org](https://freecodecamp.org).

Today was a busy day so I didn't get in as much coding time as I would have liked, but some time is better than no time at all. I completed the Reverse a String and Celsius to Fahrenheit challenges.

**Reverse a String**

For this challenge I converted the string to an array using `split()`, reversed the array with `reverse()`, and used `join()` to turn the array back into a string.

```JavaScript
function reverseString(str) {
  return str.split("").reverse().join("");
}
```

**Celsius to Fahrenheit**

This challenge was strictly pure math with order of operations.

```JavaScript
function convertToF(celsius) {
  let fahrenheit = (celsius * 9/5) + 32;
  return fahrenheit;
}
```
