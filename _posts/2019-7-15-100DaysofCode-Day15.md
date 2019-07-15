---
layout: post
title: 100 Days of Code - Day 15
category: 100 Days of Code
permalink: 100DaysofCode/day15
---

Today is Day 15 of #100DaysofCode, and I am taking a short break (today only) from the JavScript stuff on FreeCodeCamp so I can work on my blog.

I've been having issues with getting my code blocks to look right when using them so I did some research on what kind of markdown and syntax highlighter is being used with Google Pages.  It turns out the Jekyll engine that runs Google Pages is using [Kramdown Markdown](https://kramdown.gettalong.org/quickref.html) with [Rouge highlighting](https://github.com/rouge-ruby/rouge).

When I looked at the [list of support languages for Rouge](https://github.com/rouge-ruby/rouge/wiki/List-of-supported-languages-and-lexers) the languages I wanted are supported in there with some small tweaks being needed. For instance I was using `bash` instead of `shell`, but I also found that the languages are case sensitive. `Shell` would give me a properly formatted code block but `shell` would not. It was definitely an interesting find.

I was starting out to just do this as a quick fix and then move on to something else today, but it ended up taking me over an hour to figure out and implement. Through this experience I've decided to dedicate 1 day per week of my 100 days to making modifications to my blog.
