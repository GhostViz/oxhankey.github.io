---
layout: post
title: 100 Days of Code - Day 3
category: 100 Days of Code
permalink: 100DaysofCode/day3
---

Today is Day 3 of  #100DaysofCode and I learned about switch statements, returning boolean values from functions, objects, JSON, nested arrays, iteration with for and while, nesting loops, using parseInt, and using conditional operators.   

I was curious which was more efficient, switch or if/else, so I read an article [switch vs if else](https://www.geeksforgeeks.org/switch-vs-else/), written in the context on the Java programming language, in which the author discussed how if/else statements are great for analyzing booleans and switch statements are great for fixed data values. In terms of speed, when you have more then 5 cases a switch is turned into a hash map so that's when it really starts to shine.

According to [High Performance JavaScript by Nicholas C. Zakas](https://www.oreilly.com/library/view/high-performance-javascript/9781449382308/ch04.html)'s section on if-else Versus switch, switch is almost always faster and when there are more than 2 discrete values switch is the optimal choice.

I also learned about a more modern way to get the number of keys in an object using

```
Object.keys(myObj).length
```

so much simpler than something like:

```
function numAttrs(obj) {
  var count = 0;
  for(var key in obj) {
    if (obj.hasOwnProperty(key)) {
      ++count;
    }
  }
  return count;
}
```
