---
layout: post
title: 100 Days of Code - Day 4
category: 100 Days of Code
permalink: 100DaysofCode/day4
---

Today is Day 4 of  #100DaysofCode, and I worked the [Trapping Rain Water](https://leetcode.com/problems/trapping-rain-water/) problem from [leetcode.com](https://leetcode.com).

The solution I found most effective was to use a high and low pointer to track indices in the height array. Based on the value at each index the max height for that side of the array was either set to the value of the index or subtracted from the value of the index the resulting number was added to the total.

I started a [github repository for leetcode problems](https://github.com/oxhankey/leetcode) that I work. Here's [my solution to the Trapping Rain Water problem](https://github.com/oxhankey/leetcode/blob/master/javascript/trapping_rain_water.js).
