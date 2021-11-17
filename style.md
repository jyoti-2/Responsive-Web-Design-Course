CSS, or Cascading Style Sheets, tell the browser how to display the text and other content that you write in HTML. With CSS, you can control the color, font, size, spacing, and many other aspects of HTML elements.


Styling that individual h2 element with inline CSS
<h2 style="color: blue;">CatPhotoApp</h2> 

Use CSS Selectors to Style Elements
At the top of your code create a style block-
- This will work for all the h2 elements
<style>
  h2 {
    color: red;
  }
</style>

Use CSS Class to style an element
- classes are reusable styles that can be added to Multiple HTML elements.
<style>
  .blue-text { 
    color: blue;
  }
</style>

To use a google font, first we need to import the font.
<link href="https://fonts.googleapis.com/css?family=Lobster" rel="stylesheet" type="text/css">

Now we can use the Lobster font in CSS by using Lobster as the FAMILY_NAME.
font-family: FAMILY_NAME, GENERIC_NAME;

Family names are case-sensitive and need to be wrapped in quotes if there is a space in the name.
The GENERIC_NAME is optional, and is a fallback font in case the other specified font is not available. 

Generic font family names are not case-sensitive. Also, they do not need quotes because they are CSS keywords.

if you wanted an element to use the Helvetica font, but degrade to the sans-serif font when Helvetica isn't available, you will specify it as follows:
p {
  font-family: Helvetica, sans-serif;
}

you can apply multiple classes to an element using its class attribute, by separating each class name with a space.
<img class="class1 class2">
border-radius: 50%, will make the img, text fully circular.

We can use ID also to style a single element or we can use them to select and modify specific elements with javascript.

id attributes should be unique for each element.
One cool thing about id attributes is that, like classes, you can style them using CSS.

An id is not reusable and should only be applied to one element. An id also has a higher specificity (importance) than a class so if both are applied to the same element and have conflicting styles, the styles of the id will be applied.

#cat-photo{
  background-color: green;
}

All HTML elements are essentially little rectangles.
Three important properties control the space that surrounds each HTML element: padding, border, and margin.

An element's padding controls the amount of space between the element's content and its border.
An element's margin controls the amount of space between an element's border and surrounding elements.

If you set an element's margin to a negative value, the element will grow larger.

Use Clockwise Notation to Specify the Padding or margin of an Element => top, right, bottom, left

Use Attribute Selectors to Style Elements
- use to select custom groups of element to style.
[type='radio'] {
  margin: 20px 0px 20px 0px;
}

Understand Absolute versus Relative Units
- Pixels are a type of lenght unit, which is what tells the browser how to size or space an item.
Absolute units - in(inch) mm(millimeters)
Absolute length units approximate the actual measurement on a screen, but there are some differences depending on a screen's resolution.

Relative units, such as em or rem, are relative to another length value. For example, em is based on the size of an element's font.

Every HTML page has a body element, and that its body element can also be styled with CSS. And other elements will inherit the body elements styles.

Prioritize One Style Over Another
classes will override the body element's CSS, if there is conflict.
Order of the class declarations in the <style> section.
Browsers read CSS from top to bottom in order of their declaration.

id declarations override class declarations, regardless of where they are declared in your style element CSS.

inline styles will override all the CSS declarations in your style element.

There's one last way to override CSS. This is the most powerful method of all.
In many situations, you will use CSS libraries. These may accidentally override your own CSS. So when you absolutely need to be sure that an element has specific CSS, you can use !important.

color: red !important;


In CSS, we can use 6 hexadecimal digits to represent colors, two each for the red (R), green (G), and blue (B) components. For example, #000000 is black and is also the lowest possible value.

From these three pure colors (red, green, and blue), we can vary the amounts of each to create over 16 million other colors!
red's hex code #FF0000 can be shortened to #F00. This shortened form gives one digit for red, one digit for green, and one digit for blue.

Another way you can represent colors in CSS is by using RGB values.

The RGB value for black looks like this:
  rgb(0, 0, 0)
The RGB value for white looks like this:
  rgb(255, 255, 255)

CSS Variables are a powerful way to change many CSS style properties at once by changing only one value.

Create a custom CSS Variable
To create a CSS variable, you just need to give it a name with two hyphens in front of it and assign it a value like this:

--penguin-skin: gray;
you can use that variable elsewhere in your CSS to change the value of other elements to gray.

Improve Compatibility with Browser Fallbacks
Providing another more widely supported value immediately before your declaration. That way an older browser will have something to fall back on, while a newer browser will just interpret whatever declaration comes later in the cascade.


To make use of inheritance, CSS variables are often defined in the :root element.

inherit CSS Variables:
:root is a pseudo-class selector that matches the root element of the document, usually the html element. By creating your variables in :root, they will be available globally and can be accessed from any other selector in the style sheet.

Use a media query to change a variable
When your screen is smaller or larger than your media query break point, you can change the value of a variable and it will apply its style whenever it is used.
@media(max-width: 200px)
{
  :root{
    font-size: 10px;
  }
}