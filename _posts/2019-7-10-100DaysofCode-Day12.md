---
layout: post
title: 100 Days of Code - Day 12
category: 100 Days of Code
permalink: 100DaysofCode/day12
---

Today is Day 12 of #100DaysofCode. I missed yesterday which was Day 11 but today I've done 3 hours of coding to make up for the missed day. I started and completed the Basic Data Structure Challenges module from [FreeCodeCamp.org](https://freecodecamp.org).

I completed some Array and Object  challenges. The methods and language features I learned about though the challenges are documented below.

## Arrays

To demonstrate each of the concepts below I will be using the following array as an example.

`let myArr = ["Ada", "Jean", "Grace"]`

**pop()** is used to pop the element off the end of an array and return that element.

`let myPop = myArr.pop()` will give us `myArr = ["Ada", "Jean"]` and `myPop = "Grace"`

**push()** is used to add elements to the end of an array.

`myArr.push("Margaret")` will yield `myArr = ["Ada", "Jean", "Grace", "Margaret"]`

**shift()** is used to remove the first element of an array and return that element.  

`let myShift = myArr.shift()` will give us `myArr = ["Jean", "Grace"]` and `myShift = "Ada"`

**unshift()** is used to add elements to the beginning of an array.

`myArr.shift("Barbara")` will yield `myArr = ["Barbara", Ada", "Jean", "Grace"]`.

**splice()** adds or removes elements to an array and returns the removed elements.

`let mySplice = myArr.splice(0, 2)` will remove 2 elements after the 0th index and return those elements so `myArr = ["Grace"]` and `mySplice = ["Ada", "Jean"]`.

Also `let mySplice = myArr.splice(2, 0, "Barbara", "Margaret")` will remove 0 elements at the 2nd index and insert "Barbara" and "Margaret" so `myArr = ["Ada", "Jean", "Barbara", "Margaret", "Grace"]` and `mySplice = []`.

**slice()** takes a start and stop (up to but not including) element and returns a second array containing the elements between the start and stop but leaves the original array untouched.

`let myOtherArr = myArr.slice(0,2)` will yield `myOtherArr = ["Ada", "Jean"]`.

**indexOf()** returns the index of an element in an array. If the element doesn't exist `-1` is returned.

`myArr.indexOf("Lois")` will return `-1` while `myArr.indexOf("Grace")` will `return 2`.

**Spread Operator** can be used to copy entire arrays or combine arrays.

`let myOtherArr = [...myArr]` yields `myOtherArr = ["Ada", "Jean", "Grace"]` and `let myOtherArr = ["Barbara", ...myArr, "Margaret", "Lois"]` gives us `myOtherArr = ["Barbara", "Ada", "Jean", "Grace", "Margaret", "Lois"]`.

W3Schools also has a good page for [JavaScript Array References](https://www.w3schools.com/jsref/jsref_obj_array.asp).

## Objects

To demonstrate each of the concepts below I will be using the following object as an example.
```JavaScript
let womenInTech = {
  Ada: 1815
  Jean: 1924
  Grace: 1906
}
```

**Dot Notation** and **Bracket Notation** are both ways to access properties of an object. Dot Notation is used most frequently, but Bracket Notation should be used when using variables.

`let adaBirth = womenInTech.Ada` will yield `1815`.

`let name = "Ada"` does not work with dot notation if you try `let AdaBirth = womenInTech.name` yields `undefined`. However, `let AdaBirth = womenInTech[name]` yields `1815`.

**delete** deletes the specified property.

`delete womenInTech.Ada` will remove Ada from the object completely.

**hasOwnProperty()** checks if a property exits and returns true or false.

`let check = womenInTech.hasOwnProperty("Ada")` returns `true` while `let check = womenInTech.hasOwnProperty("Barbara")` returns `false`.

**Object.keys()** returns an array of the object's keys.

`let myArr = Object.keys(womenInTech)` returns `["Ada", "Jean", "Grace"]`.

I took a little bit of a different approach to my learning today, but I think for the longer term this will be more beneficial for me and for whoever decides to read what I post.
