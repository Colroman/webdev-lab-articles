this is the code for the html.

```html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <link rel="stylesheet" href="jarvis.css">
  <title>Jarvis Static Bot Solution</title>
</head>
<body>
  <header>
    <h1>Jarvis Static Bot</h1>
  </header>
  <div class="wrapper">
    <h2><b>Jarvis:<b>Hello please type in a command,use<i>help
    </i>to see available commands</h2>
    <div id="chat-area"></div>
    <input type="text" id="user-input">
    <button id="respond">Send</button>
    </div>
  </body>
    <script src="jarvis.js"></script>
    </html>
 ```
	this is the code for the css.
```css	
  body{
  font-family: cursive;
  font-size: 16px;
  padding: 0;
  margin: 0;
  line-height: 1.4;
}
header {
  background-color: #B3A9F4;
  padding: 14px;
  box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
}
h1, h2, h3 {
  font-weight: 300;
}
header > h1 {
  font-weight: 300;
  font-size: 40px;
  color: #ffffff;
  text-align: center;
}
.wrapper {
  max-width: 70%;
  width: 50%;
  margin: auto;
}
input[type=text] {
  width: 100%;
  font-size: 16pt;
  transition: all 0.4s ease-in-out;
  padding: 10px;
  -webkit-appearance: none;
  line-height: 1.42857143;
  color: #555;
  border: 1px solid #ccc;
  margin-top: 3px;
  border-radius: 20px;
  cursor: pointer;
  transition: all 0.4 ease-in-out;
}
button {
  border: none;
  background: orange;
  padding: 12px 12px;
  font-size: 16pt;
  float: right;
  width: 100px;
  color: #fff;
  display: inline;
  align-self: center;
  margin-top: 3px;
  border-radius: 20px;
  cursor: pointer;
  transition: all 0.4s ease-in-out;
}
button:hover {
  background: green;
}

input:focus, button:focus {
  outline: none;
}

#chat-area {
  font-size: 1.5em;
  font-style: italic;
  }
 ```
  this is the Javascript code.var userInput = document.getElementById('user-input');
 
 ```javascript
var btn = document.getElementById('respond');
var chatArea = document.getElementById('chat-area');
function kill() {
   return window.open('http://mystic-investigations.w4lizsrnr.netdna-cdn.com/blog/wp-content/uploads/2015/09/Condition-Red-Alert.gif', '_self');
};
var commands = [
  ['hi', 'hello'],
  ['hello', 'how are you?'],
  ['what\'s up', 'fine and you?'],
  ['who are you', 'i am me ::Jarvis::'],
  ['who created you', 'US!!!!'],
  ["what's your father's name", 'Roman'],
  ['help', 'Yes! what can i do for you'],
  ['self destruct'],
  ['test', 'test']
];
var defaultMsg = "Sorry! I'm still under training i may not have a response to that command";

btn.addEventListener("click", function() {
  chatArea.innerHTML += "<p><b>You: </b>" + userInput.value + "</p><br>";

  for (i = 0; i < commands.length; i++) {
    if (userInput.value == commands[i][0]) {
      var match = true;
      var response = commands[i][1];
  }
  if (userInput.value == 'self destruct' || userInput.value == 'destroy' || userInput.value == 'die') {
    kill();
  }
}
if (userInput.value == 'help') {
  chatArea.innerHTML += "Jarvis: ";
  for (ii = 0; ii < commands.length; ii++) {
      chatArea.innerHTML += commands[ii][0] + "<br>";
}
return;
}
if (!match) {
  setTimeout(function() {
    chatArea.innerHTML += "<p><b>Jarvis: </b>" + defaultMsg + "</p><br>"
  }, 3000);
} else {
  setTimeout(function(){
    chatArea.innerHTML += "<p><b>Jarvis: </b>" + response + "</p><br>"
  }, 2000);
}
});
```
  
  
  


