# Learning Journal - code 201 - day 7

I experienced part of the self-hazing process today. I had some beautifully written code but I couldn't run it in the browser. Curse you, machine! Turns out I was looking for it in the wrong .html window. You live and you learn. More of that to come I'm sure.

This is supposed to be day 2 of a hard series of 3 days yet I'm still maintaining my sanity. I believe what's really helping is focusing and understanding the problem before hacking at the keyboard. This allows me to ask better questions and recognize where or why my code might not be working. I'm still finishing late but having an algorithm keeps me calm and away from panicking.

Another thing I learned about that will be useful some point down the line is having multiple .js files to organize my code. Right now I noticed I'm writing a whole bunch of definitions for functions, variables, and objects, then executing the actual code on the last lines of the file. It seems like a pain to scroll all the way down. This is multiple .js files come in. One can have the definitions while the other can show the code to run. If they're both tagged in the html document they will run. 

refactor: taking code that we have and making it cleaner and more efficient  
## Functions
function declaration  
- available everywhere in the script  
- function functionName () {}  

function expression  
- only available after the fact of where you declare it  
- var functionName = function() {}  

## Tables
### Static table
<table>  
  <thead> <!-- table head -->  
    <tr> <!-- table row -->  
      <th></th> <!-- table header -->  
      <th>9am</th>  
      <th>10am</th>  
      <th>11am</th>  
      <th>Total</th>  
    </tr>  
  </thead>  
  <tbody> <!-- table body -->  
    <tr>  
      <th>Pike</th>  
      <td>37</td> <!-- table data cell -->  
      <td>50</td>  
      <td>22</td>  
      <td>109</td>  
    </tr>  
  </tbody>  
</table>  

### Dynamic table
var hours = ['9am', '10am', '11am'];  

function renderHeaderRow() {
    <!-- create your container then every unique cell -->
    var storeTable = document.getElementById('store_table'); // Locate  
    var tableRow = document.createElement('tr'); // Create  
    var blankTableHeader = document.createElement('th'); // Create  
    var totalTableHeader = document.createElement('th'); // Create  
    var hourlyTableHeader;  

    tableRow.appendChild(blankTableHeader);

    for (var i= 0; i < hours.length; i++) {  
      hourlyTableHeader = document.createElement('th');  
      hourlyTableHeader.textContent = hours[i]; // Update content  
      tableRow.appendChild(hourlyTableHeader);  // Put it somewhere
    }   

  totalTableHeader.textContent = 'Total';  
  tableRow.appendChild(totalTableHeader);  

  storeTable.appendc(tableRow);  
}
renderHeaderRow(); //call the function to show in html

### Constructors
METHODS ON THE PROTOTYPE, PROPERTIES IN THE Constructors  

function CookieStore(storeName, minCust, maxCust, avgCookies) {  
  // var this = {} //'this' assigned brand new object  
  this.name = storeName; //'this' is referring to the new object (key?) it's creating for you  
  this.minCust = minCust;  
  this.maxCust = maxCust;  
  this.avgCookies = avgCookies;  
  this.hours = ['9am', '10am', '11am'];

  // Take care of this function with a prototype  
  this.logStoreName = function() {  
    console.log(this.name);  
  }  
  //return this; //the properties  
}  

// Make a prototype (for memory optimization) for methods in constructors  
CookieStore.prototype.logStoreName = function() {  
  console.log(this.name);  
}  

CookieStore.prototype.toHtml = function() {  
  var storeTable = document.getElementById('store_table');  
  var tableRow = document.createElement('tr');  
  var nameTableHeader = document.createElement('th');  
  var totalTableData = document.createElement('td');  
  var hourlyTableData;

  nameTableHeader.textContent = this.name;  
  tableRow.appendChild(nameTableHeader);  

  for (var i = 0; i < this.hours.length; i++) {  
    hourlyTableData = document.createElement('td');  
    hourlyTableData.textContent = 5; // use different data here in lab  
    tableRow.appendChild(hourlyTableData);  
  }

  totalTableData.textCon = 15; // use instead calc total from other methods  
  tableRow.appendChild(totalTableData);  

  storeTable.appendChild(tableRow);  
}

// Run the constructor, use keyword 'new'  
var pike = new CookieStore('pike', 2, 15, 6);  

## Code review
Potentially change in cookie store app.js, storeName Hours property:  
- create list item for store name  
- create list item for total  
- return the node after you make it in the function
on top of the list item for hours and cookies  

If your console logs out "object object" it's trying to concatenate an object with a string.  

Create node, update (add content) node, put (append) it where it needs to go.  
