# LJ Code 201 - Day 5  

The first week of 201 has finished. It was a good time to find a rhythm and refine my approach to the remaining time. The Wednesday lab with loops was particularly challenging and mentally exhausting but 1/5 for the week isn't too bad. Because a lot of the material this week was familiar to me on some level, my concern is how I will handle everything once new concepts and material are presented down the line. I anticipate more challenges and a few more frustrated journal entries.  

A good skill I want to improve on is taking a problem or instruction and turning it into detailed/lengthy pseudocode. My brain can understand the problem but it will execute multiple lines in one action whereas my code needs to be broken down with more steps to achieve the same outcome. It's reassuring to think I'm still smarter than my computer. It will always do what I tell it but right now I'm telling it to do things I didn't quite translate well.  

The check yo'self moments of the day were:  
- Examining the test.js on top of app.js to work through problem 3. Problems won't always be isolated in one file.  
- Variable datatypes are just var. You overlook that when you think you pass a single value but instead pass a whole array. C++ has an advantage here with all their silly datatypes.

## Things I learned today  
- In a .html file, type "html" + tab to get a template  

- reference error happens (in the console of web window) when something hasn't been declared  

- Function template:  
function functionName (var1, var2) {  
  return [var1, var2]  
}  
- Anything after the return statement of a function is not ran  
- Return an array to get multiple values out of a function  

## Overview of week 1  
<strong>Monday:</strong>  
HTML
- Provides structure for the page  
- Not how things look (for CSS), or logic/interaction (for JS)

Git  
- ACP
  - git branch  
  - git status  
  - add (stages files)  
  - git status  
  - commit (changes become part of project history)  
  - push (moves changes from local to remote)  
  - git status  

Terminal  
- navigation  
  - cd  
  - ls  
  - pwd  
  - whoami
- create/edit  
  - mv (changes the path, can change the name)  
  - touch  
  - mkdir  
  - cp  
- delete  
  - rm  

<strong>Tuesday:</strong>  
Project structure  
  - app.js, <script> tag at bottom of the body  
  - index.html, <link> tag in the <head>  
  - style.css  

Git branching  
  - git checkout -b <branchName>, creates a new branch  

<strong>Wednesday:</strong>  
Control flow  
  - falsey values: false, 0, undefined, null, '', NaN  
  - truthy values: everything else  

Arrays  
  - if you aren't accessing or creating something in/for the array, don't use brackets.  
  - common to use a for loop to iterate over  

Type coercion  
  == checks for equality, converts type first  
  === checks for type and equality  

<strong>Thursday:</strong>  
CSS display  
  - block: own line, expands to the width of its parent container. ex - div, p, h, ul, ol, li  
  - inline-block: like inline with extra positioning properties  
  - inline: sit in with text, width by default wraps the content. ex - span, a  

Position  
  - static: default (it's not positioned), out of the flow of the page-yes  
  - relative: access to top, right, left, bottom, relative to its default/static position, out of the flow of the page-no  
  - absolute: access to top, right, left, bottom, relative to its closest positioned ancestor (with help from relative. Relative can act like static.), out of the flow of the page-yes  
  - fixed: access to top, right, left, bottom, relative to the window, out of the flow of the page-yes. Really good for sticky header/footer or pop-up window   
