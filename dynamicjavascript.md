# Dynamic web pages with JavaScript

## Author

Jeffrey Smith

## Javascript

JavaScript (JS) an object-oriented computer programming language commonly used to create interactive effects within web browsers.

Do not confuse JavaScript with the Java programming language. Both "Java" and "JavaScript" are trademarks or registered trademarks of Oracle in the U.S. and other countries. However, the two programming languages have very different syntax, semantics, and use.

[Webpage](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

We are going to see how to input from a user and combine that the other two create simple page that will great you.

Examples 

<html>
<head>
  <title>Hello World</title>
</head>
<body>
 
First name: <input id="first_name">
Last name: <input id="last_name">
<button id="say">Say hi!</button>
 
<hr>
<div id="result"></div>
 
<script>
function say_hi() {
    var fname = document.getElementById('first_name').value;
    var lname = document.getElementById('last_name').value;
 
    var html = 'Hello <b>' + fname + '</b> ' + lname;
 
    document.getElementById('result').innerHTML = html;
}
 
document.getElementById('say').addEventListener('click', say_hi);
</script>
 
</body>
</html>

We have a bit more HTML than earlier with addition to having a button, and a div element where we show our results

Also we have two input elements. Each one with its own ID.

If you click on the Try link, you'll see two input boxes and a button:

Input form

First name _________  Last name________   Say Hi!  which is a button.

In JavaScript we have a function called say_hi. It usees the getElementById we have already seen to locate the DOM element representing the input element with the id first_name. The object returned has a method value that will return the text the user has typed in that field.

Use this technique to retrieve the content of both input fields and assign their content to two variables: fname and lname.

Then, using these variable we create an HTML snippet and assign it to a new variable called html.

Then we set the innerHTML attribute as earlier to show the HTML we generated. The result might look like this:

First name_______   last name __________   Say hi! which is a button

you click and Hello the name appears on the screen.

[Webpage](https://code-maven.com/input-output-in-plain-javascript)