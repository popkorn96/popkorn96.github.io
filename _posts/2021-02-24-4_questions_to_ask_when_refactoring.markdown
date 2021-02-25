---
layout: post
title:      "4 Questions to Ask When Refactoring"
date:       2021-02-25 02:14:43 +0000
permalink:  4_questions_to_ask_when_refactoring
---


There's a moment that all software developers are familiar with. The moment involves writing that last bit of code, getting that last bug fixed, and finally getting the output you were looking for. That moment can make you feel good, almost triumphant, but you know that there is almost always anothers step that comes after, and that is **refactoring**. <br><br>Oxford languages describes refactoring as '*restructure (the source code of an application or piece of software) so as to improve operation without altering functionality.*' To continiously improve as coders, we have to consistently find ways to make our good and working code *better*. <br><br>
To do this, I compiled a list to ask yourself or your companions when refactoring any code. <br>
1. Can you understand it at a glance?
2. Can you derive the result in a different way?
3. Can you improve the performance of your solution?
4. Has anyone else solved this same problem?
<br>
### ONE - Can you understand it at a glance?<br>
Something to always consider when writing your code is the readability. Is someone else able to read your code at first glance? Are your variables appropriately labeled? Is the syntax what you would expect to see on official language resources? Figuring out if an outsider would be able to mark your code as legible is a big part of refactoring.<br>
We all have spurts of writing where we are more focused on result rather than appearance, but it is important to note that *clean code is happy code*. It always makes debugging and updating easier in the future.<br>
### TWO - Can you derive the result in a different way?<br>
This is the first real step to refactoring. Can you use a `for...of` loop instead of a `for` loop? Can you replace your `if...else` with a boolean? Is there a way to export an operation as a function? There can be multiple ways to reduce lines of code for any one function. This question can be misleading if someone is not familiar with time or space complexity implications that each change can affect. It is important to continue to monitor your desired results as you make changes, so you don't accidentally break your code.<br>
### THREE - Can you improve the performance of your solution?<br>
If you haven't covered Big O Analysis yet, I recommend finding a few resources to review before attempting to improve the performance of code you have written. Getting a deeper understanding of time complexity and space complexity might help you decide whether to write code that would cause logarithmic time complexity versus linear.<br> In smaller projects, changing one function to improve on [asymptotic analysis](https://www.geeksforgeeks.org/analysis-of-algorithms-set-1-asymptotic-analysis/) won't cause much change, as opposed to working on larger scaled projects or in a company that deals with larger datasets.<br>
### FOUR - Has anyone else solved this same problem?<br>
In the context of technical interviews, it can be helpful to ask your interviewer how the problem has been solved in the past. This can indicate to your interviewer how you are result driven and capable of self-improvement. Outside the scope of interviews, this question can lead you to find wildly different answers to the same problem you've been presented with. While it may not be what you were looking for, searching for different problems may inspire other ideas and get your gears rolling with other possible ways to approach it.<br><br>
All in all, refactoring is a process that most definitely sharpens your skills and returns great, easy to read, efficient code. As you refactor, it shortens the time you spend in the future with similar code. It can be daunting at first, but your future self will thank you for your efforts.
