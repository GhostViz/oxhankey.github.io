---
layout: post
title: 100 Days of Code - Day 18
category: 100 Days of Code
permalink: 100DaysofCode/day18
---

Today is Day 18 of #100DaysofCode. I completed the Basic Algorithm Scripting module from [FreeCodeCamp.org](https://freecodecamp.org).

I completed the Where Do I Belong, Mutations, and

### Where Do I Belong

Return the lowest index at which a value (second argument) should be inserted into an array (first argument) once it has been sorted. The returned value should be a number.

For example, `getIndexToIns([1,2,3,4], 1.5)` should return 1 because it is greater than 1 (index 0), but less than 2 (index 1).

Likewise, `getIndexToIns([20,3,5], 19)` should return 2 because once the array has been sorted it will look like [3,5,20] and 19 is less than 20 (index 2) and greater than 5 (index 1).


**Solution:**

For this challenge I pushed the integer `num` to the array `arr` and used a bubble sort function `bubbleSort` before returning `indexOf(num)`.


```JavaScript
function getIndexToIns(arr, num) {
  // Find my place in this sorted array.
  arr.push(num);
  return bubbleSort(arr).indexOf(num);
}

function bubbleSort(arr) {
    let swap;
    do {
        swap = false;
        for (let i = 0; i < arr.length; i++) {
          if (arr[i] > arr[i+1]) {
            let temp = arr[i];
            arr[i] = arr[i+1];
            arr[i+1] = temp;
            swap = true;
          }
        }
    }
    while (swap)

  return arr;
}
```

### Mutations

Return true if the string in the first element of the array contains all of the letters of the string in the second element of the array.

For example, ["hello", "Hello"], should return true because all of the letters in the second string are present in the first, ignoring case.

The arguments ["hello", "hey"] should return false because the string "hello" does not contain a "y".

Lastly, ["Alien", "line"], should return true because all of the letters in "line" are present in "Alien".

**Solution:**
For this challenge I converted both strings to lower case then I looped through each element in the second string `str2` and checked if it was in the first string `str1` using `indexOf`.

```JavaScript
function mutation(arr) {
  let str1 = arr[0].toLowerCase();
  let str2 = arr[1].toLowerCase();

  for (let i = 0; i < str2.length; i++) {
    if (str1.indexOf(str2[i]) == -1) {
      return false
    }
  }
  return true;
}
```

### Chunky Monkey

Write a function that splits an array (first argument) into groups the length of size (second argument) and returns them as a two-dimensional array.

**Solution:**
For this challenge I created a new array `newArr` to be my 2d array. Then I looped the length of the array `arr` incrementing each time by `i + size`. Inside the loop I used `slice()` to push a new array to the 2d array `newArr`.

```JavaScript
function chunkArrayInGroups(arr, size) {
  let newArr = [];
  for (let i = 0; i < arr.length; i+=size) {
   	newArr.push(arr.slice(i, i+size));
  }
  return newArr;
}
```

### Final Thoughts

These 3 challenges seemed much harder and took me considerably more time than the previous challenges in this section. The solutions that seemed obvious at first ended up not working out due to technical limitations with things like `sort()` which will sort the array `[0,1,3,20]` to `[0,1,20,3]` so it became necessary to write my own sort function. Overall I am happy with these three challenges because they were challenging and forced me to think outside of the predefined methods.

I did go ahead and upload all of these challenges to [my github](https://github.com/oxhankey/freeCodeCamp/tree/master/jsBasicAlgorithms).
