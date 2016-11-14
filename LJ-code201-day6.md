# Learning Journal Code 201 Day 6

When you get unexpected results, start logging them out. For example, in Lab 5, functions returned arrays and we wanted index values to return, not the whole array. It was commonly overlooked that whole arrays, not separate index:elements were being returned.  

## Code review  
sum(a, b) returns an array [total, string]  
function sumAndMultiply (a, b, c) {  
  var firstSum = sum(a, b)[0]; // gives access to the first[0] index:elemnent after the sum function returns its array  
  var totalSum = sum((sum(a, b)[0], c)[0]); fully evolved way to calculate the sum with correct values   
}  

## Objects
var myFirstObject = {}; // literal declaration. Same if you add 'key: value,' pairs within the brackets  

var stringThatGetsPassedIntoAFunctionProbably = 'favoriteAnimal';

myFirstObject.name = 'kevin'; // dot notation creates properties  
  myFirstObject.name // gets  
  myFirstObject.name = ''; // sets properties, properties can be anything  
myFirstObject['1!favAnimal'] = 'slug'; // bracket notation is better when a number or special character is in the key
myFirstObject[stringThatGetsPassedIntoAFunctionProbably] = ''; // more appropriate use of brackets, keys are always strings  

functions that are a part of an object are called <strong>methods</strong>

'this' works in the functions in the object and you want to access other properties/methods inside that object  
If you need to get to an object inside the object, use 'this', further allowing access to the properties  
var cookieStore = {  
  hours: ['7am', '8am', '9am', '10am'],  
  whatHours: function() {  
    console.log('I am open certain hours: ' + this.hours);  
  }  
}  

## DOM
DOM is a model of the html document in JS so JS can work with it  
var nodeVar = document.getElementById('id')  
<strong>document.getElementById('id')</strong> // get stuff back from the DOM (and give every html element an id)  
- gives back representation of that element  
- what gets stored on the variable is a node  
- <em>CSS note: id's are used by scripts to fetch, classes are better referenced for styling.</em>  
nodeVar.textContent = 'change and hack here lol'  

1. get the thing you want (as a node) (ex: document.getElementById())  
2. use the methods to work on it  
  - ex: var newHeading = document.createElement('h1') // creates new node newHeading of that tag name (h1 in this case)  
  - newHeading.textContent = 'new text' // set what is in the tag/html element  
  - nodeVar.appendChild(newHeading) // how you make a child of a node (parent is nodeVar)  
    - the argument is the content displayed in the node(nodeVar) which is a parent to the newHeading child node?  

In cookieStore{}  
  listHours: function() {  
    var contentArea = document.getElementById('content_area'); // LOCATE. content_area is an id in index.html for a tag  
    var ul = document.createElement('ul'); // USE METHODS. creates ul element only in the function  
    var li = document.createElement('li'); // USE METHODS. creates li element only in the function  

    li.textContent = 'TEST LI'; // USE METHODS. add content for the created tag/element  

    ul.appendChild(li); // USE METHODS. makes ul the parent of li  
    contentArea.appendChild(ul); // USE METHODS. makes contentArea the parent of ul  
  }

<strong>OR</strong>  

  listHours: function() {  
    ""  
    ""  
    var li;  

    // loop to create multiple li's, add content to each one, and append to ul
    for (var i = 0; i < this.storeHours.length; i++) {  
      li = document.createElement('li');  

      li.textContent = this.storeHours[i];  
      ul.appendChild(li);  
    }
    contentArea.appendChild(ul);  
  }  
