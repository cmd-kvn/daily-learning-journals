# LJ code 201 day 9

Today was almost defeating. I made a stand alone function that needed to be above a function to let the below function render, but it also needed to be below that function because it needed stuff from the above function.  
function 1 // runs to make an array needed by function 2
function 2 // uses arrays to make a table  
function 1 // needs function 2 to run to make objects with data that function 1 needs to use  

I changed the stand alone function to a prototype of the object but still had problems.  

This is the problem I see with dynamic functions. Especially when code is happening/defined at one point in your file that you need to see how it plays with what you're working on.  

I also got a free tshirt. This did not compensate for the troubles I had.

## Code review
In multi-line strings, "wrap" it by concatenating strings on separate lines OR use the escape key (\) at the end of each line break.

When a language can pass in functions as an argument, they are called higher-order functions or first-class functions.

event.target.someTarget.value and  
document.getElementById('some_id').value + an extra id in html  
get the same thing.

### Wireframe practice
http://codepen.io/anon/pen/qqqxoQ?editors=1010#0

## Why use 'use strict'?
'Use strict' helps keep track of the scope of variables. For example, without 'use strict', if a variable wasn't declared in a function, JS would make an assumption and declare it on the global scope, obviously tricky. It also keeps 'this.' in line/within its scope. Otherwise 'this.' would set/give access to the window.

## CSS positioning
Relative position stays in the flow of the document, and is relative (left, right, up, down) to where it would normally be.  
Everything but static is said to be positioned. TRBL doesn't apply to static.  
Static and relative take up 'space', share attributes?  
Fixed and absolute don't take up 'space' on the page.  
Absolute is kinda like fixed, different from if it's ancestor is defaulted to the window or it's ancestor element who is positioned.  
Use absolute to sit on top of something else, especially for pop-ups.  

float gets block elements to sit next to each other  
floats, positioning, box element, display, how to get a good grip on layout  

### Examples
http://codepen.io/anon/pen/VmmyLW
http://codepen.io/anon/pen/VmmyMy?editors=1100
