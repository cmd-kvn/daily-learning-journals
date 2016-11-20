# LJ code 201 day 10
I'm slowly getting things in CSS to click. Mainly I've focused on my JS for the current salmon cookies project so once I turn to the html/css I think I will see a stronger understanding of how things work. In the meantime, working with codepen in the morning has been helpful to dynamically see what's going on with the html, css, and JS. Likewise pairing knowledge in the afternoon lab was appreciated. Brigette has strong skills. 


## CSS notes
normalize: normalizes html across all browser.  
Meyer reset: is a short, often compressed (minified) set of CSS rules that resets the styling of all HTML elements to a consistent baseline. Include a style sheet to apply it to your project and link it before your style sheet.  

Set the width and 0 auto to center a block element.

## Review
storeObjects [];
totalCookiesPerHr []; // property of a store object

var totalsArray = [];
var hours = storeObjects[0].totalCookiesPerHr.length;
var grandTotal = 0;
var hourTotal = 0;
for(var hour = 0; i < hours; i++) { // The slower moving loop is on the outside (first loop)

  for(var j = 0; j < storeObjects.length; j++) { // The faster moving loop is on the inside (second loop)
    hourTotal = storeObjects[j].totalCookiesPerHr[hour];
    totalsArray.push(hourTotal);
    grandTotal += hourTotal;
  }
}

## Monday
#### Objects  
Few instances to use brackets: setting a property value in literal construction, or  
var key = 'slug'  
objectOne[key] = 'salt' --> {slug: 'salt'}  
objectTwo.key = 'salt' --> {key: salt}  
'this.' : a way to reference properties of that object when you're inside a method of that object.  
'this.' also works in a 'new constructor' to declare new properties in a new object.  

#### DOM manipulation
document.getElementById()  
document.createElement()  
el.textContent  
el.appendChild()  

## Tuesday
#### Constructors
Are used for multiple similar objects.  
One created object is an instance/is instantiated.  
'new', using new to create new objects via constructor.  

## Wednesday
#### Events
node.addEventListener is a method of the node.  
addEventListener('name of event as a string', handler(){}).
- The handler is a function that isn't called in the argument  

Event  
- event.preventDefault();  
- event.target is a reference to the element that fired off the event (node from node.addEventListener, but not always necessarily)  

## Thursday
#### CSS positioning
- Static: the default, appears to be where it appears to be, said to 'not be positioned', no access to TRBL  
- Relative: appearance is positioned to where it's supposed to be but still takes up space where it's supposed to be. Behaves as static if not manipulated.   
- Fixed: anchored relative to the viewport  
- Absolute: relative to closest positioned ancestor(parent)  
- The problem with floats: its parent container will collapse unless you clear it or it has something that's not floated after it, like a block element.  
