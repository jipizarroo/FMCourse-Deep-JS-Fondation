---
description: >-
  One of the 3 core pilars.
  https://frontendmasters.com/courses/deep-javascript-v3/scope/
---

# Scope

Scope => Is where we look at things.

* What is it that we are looking for? => We are looking for identifiers.

```javascript
x = 42; // x that's been assigned to.
console.log(y); // y that's being a value retrieved from.
```

All variables are in one of those two roles in your program. When we are processing our code, when the scope is being processed by the JS engine, its essentially asking the question =>

When I see this variable, first of all, what position is it in? and secondly, what scope does it belong to?

It's extremely common for people to think about JS as a running top-down, line-by-line, execution, BUT JS is not an interpreted language, it's a compiled language. There is some processing step that has to happen before execution has occurred.

Example: \
If you have ever written a JS syntax error, left off a comma, had an extra parenthesis, or curly brace somewhere, and then you try to run the program, and you immediately get a syntax error =>

How can JS know there is an error on line 10, before executing lines 1 through 9? JS went through a process step first as opposed to simply executing top-down.

So what does that processing step look like?

The way the processing first happens before we execute =>

There is a stage where it goes through all of that compilation, through all of that parsing and it produces this abstract syntax tree BUT it also produces, essentially, a plan for the lexical environment, meaning, where all the lexical scopes are, and what marbles are gonna be in them ( Marbel coz is referring to the bucket coloring sorting of marbles ), what identifiers.&#x20;

It prepares this plan, and that is the executable code that is handed off to be executed by the other part of the JS engine.





