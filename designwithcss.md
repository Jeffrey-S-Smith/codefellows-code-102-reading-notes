# Design web pages with CSS

## CSS Style

## Author

Jeffrey Smith

What is CSS? (Cascading Style Sheets
allows you to create good looking web pages. it works under the hood. 

What is CSS for
CSS is a language for specifying how documents are presented to users 
css is very basic document text style exampe  turning single column to text into a layout
with a main content area and sidebar. 

CSS syntax

h1 {
    color: red;
    font-size: 5em;
}

h1 {
    color: red;
    font-size: 5em;
}



p {
    color: black;
}

### CSS Modules

many things that you could style using CSS, 
the language is broken down into modules.
you can explore MDN and many of the documentation pages for CSS Specification

## How To Add CSS

Three ways

- External CSS
- Internal CSS
- Inline CSS

## Example
 
 External CSS

<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="mystyle.css">
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>

An external style sheet can be written in any text editor, 
and must be saved with a .css extension.

The external .css file should not contain any HTML tags.

how the "mystyle.css" file looks:

"mystyle.css"

body {
  background-color: lightblue;
}

h1 {
  color: navy;
  margin-left: 20px;
}

## Internal CSS

internal style sheet may be used if one single HTML page has a unique style.

internal style is defined inside the <style> element, inside the head section.

Example

<!DOCTYPE html>
<html>
<head>
<style>
body {
  background-color: linen;
}

h1 {
  color: maroon;
  margin-left: 40px;
}
</style>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html>

### Inline CSS

inline style may be used to apply a unique style for a single element.

inline styles, add the style attribute to the relevant element.
The style attribute can contain any CSS property.

Example

<!DOCTYPE html>
<html>
<body>

<h1 style="color:blue;text-align:center;">This is a heading</h1>
<p style="color:red;">This is a paragraph.</p>

</body>
</html>

### Multiple Style Sheets

some properties have been defined for the same selector (element) in different style sheets, 
the value from the last read style sheet will be used.

 Assume that an external style sheet has the following style for the <h1> element:
 
 h1 {
  color: navy;
}

Then, assume that an internal style sheet also has the following style for the <h1> element:
h1 {
  color: orange;   
}

Example

internal style is defined after the link to the external style sheet, 
the <h1> elements will be "orange":

<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
<style>
h1 {
  color: orange;
}
</style>
</head>

f the internal style is defined before the link to the external style sheet, 
the <h1> elements will be "navy": 

<head>
<style>
h1 {
  color: orange;
}
</style>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>

[Webpage](https://www.w3schools.com/css/css_howto.asp)

## CSS color Property

Example

text-color for different elements:

body {
  color: red;
}

h1 {
  color: #00ff00;
}

p.ex {
  color: rgb(0,0,255);
}

Definition and Usage

Color property specifies the color of text.

CSS Syntax
color: color|initial|inherit;

Example

- HEX body {color: #92a8d1;}
- RGB body {color: rgb(201, 76, 76);}
- RGBA  body {color: rgba(201, 76, 76, 0.6);}
- HSL body {color: hsl(89, 43%, 51%);}
- HSLA body {color: hsla(89, 43%, 51%, 0.6);}

uuu

[Webpage](https://www.w3schools.com/cssref/pr_text_color.asp)
