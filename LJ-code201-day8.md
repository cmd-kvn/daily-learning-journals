# LJ Code 201 day 8

It's the end of what has been called 3 of the most difficult days of the course yet I have not pulled out my hair. This is a good sign. In reality I've feel satisfied with the work I've done since Monday. By taking more time to analyze the problem I noticed I've asked more questions about my algorithm rather than why my code isn't working. It's a change from last week where I tried to jump in, lose scope of the big picture, and then lose my way.

One of the things I'm proud of today is how I cleaned up my code/used the DRY principle. It's almost looking good enough for me to volunteer for code review even if my CSS says otherwise. DRY'ing up helped me see how functions can exist within functions and how object methods can be called within other objects. I could see how it was going to work but today I got more on how to write out the semantics of how to reference these methods.

Lastly, at some point today or yesterday I finally felt comfortable with git/github. It only took the 102 and 1.5 weeks of 201 to finally feel good navigating through it.

## Resources for CSS/HTML
http://scratchpad.io/  
http://codepen.io/

## Code review
If you make an object with a constructor you can still add or edit properties using objectName.someProperty = value.  

## Forms and Events
Major <strong>event</strong> we're focusing on: SUBMIT  
Events capture interaction, anyway you take input from a user.  

<!-- HTML HTML HTML HTML HTML HTML HTML HTML HTML HTML HTML HTML HTML HTML HTML HTML HTML HTML HTML HTML  HTML -->
<!DOCTYPE html>
<html>
  <head>
    <title></title>
  </head>
  <body>
    <h1>Forms and Events</h1>
    <button id="click_me">CLICK ME</button>  
    <form id="name_form">
      <input type="text" placeholder="First Name" name="first_name"> <!-- placeholders are greyed out text that disappears when text is entered -->
      <input type="text" placeholder="Last Name" name="last_name">
      <input type="submit"> <!-- input tags are self closing -->
    </form>
    <section id="form_text"></section>
    <h2>Chat Form</h2>
    <form id="chat_form">
      <input type="text" name="message">
      <input type="text" name="author">
      <input type="submit">
    </form>
    <section id="chat_messages"></section>
    <script type="text/javascript" src="app.js"></script>
  </body>
</html>

<!-- JavaScript JavaScript JavaScript JavaScript JavaScript JavaScript JavaScript JavaScript JavaScript JavaScript -->
'use strict'  

var clickMeButton = document.getElementById('click_me');  

clickMeButton.addEventListener('click', handleClick) //(name of event, what to do when it sees event happen (the function isn't called))  

function handleClick() {  
  alert('CLICKED');  
}  

var nameForm = document.getElementById('name_form'); // Get the element  

nameForm.addEventListener('submit', handleSubmit); //Add the listener  

// Create the handler.  
// SUBMIT will refresh the page and clear the box by default  
// handleSubmit is passed an argument. When the function gets called, 'event' is set as an object to contain info about the event.  
// .preventDefault() keeps the page from refreshing  
function handleSubmit(event) {  
  event.preventDefault();

  var textBox = document.getElementById('form_text');  
  var firstName = event.target.first_name.value; // event.target(node), first_name(input for node on form)  
  var lastName = event.target.last_name.value;  

  textBox.textContent = 'Hi ' + firstName + ' ', + lastName;  

  // Reset the fields
  event.target.first_name.value = '';  
  event.target.last_name.value = '';  
}  

var chatForm = document.getElementById('chat_form');  
var messages = [];  

chatForm.addEventListener('submit', handleChatSubmit);  

function handleChatSubmit(event) {  
  event.preventDefault();  

  // Take in input  
  var message = event.target.message.value;  
  var author = event.target.author.value;  

  // Handle input  
  var newMessage = new ChatMessage(message, author);  
  messages.push(newMessage);  

  // Reset forms  
  event.target.message.value = '';
  event.target.author.value = '';   

  renderChat();   
}  

function ChatMessage(message, author) {  
  this.message = message;  
  this.author = author;  
}  

function renderChat() {  
  var chatSection = document.getElementById('chat_messages'); // Locate  
  var messageParagraph;  
  var author;  
  var message;  

  chatSection.textContent = '';  

  for (var i = 0; i < messages.length; i++) {  
    messageParagraph = document.createElement('p'); // Create   

    message = messages[i].message;  
    author = messages[i].author;  

    messageParagraph.textContent = author + ': ' + message; // Update content  

    chatSection.appendChild(messageParagraph); // Put it somewhere  
  }  
}  
