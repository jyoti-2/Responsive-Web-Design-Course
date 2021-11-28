Applied Visual Design
Visual design is a combination of typography, color theory, graphics, animation, page layout, and more to help deliver your unique message.

text-align: justify; spaces the text so that each line has equal width.
text-align: center; centers the text
text-align: right; right-aligns the text
text-align: left; (the default) left-aligns the text

You can specify the width of an element using the width property in CSS. Values can be given in relative length units (such as em), absolute length units (such as px), or as a percentage of its containing parent element. 

- Wrapping a <strong>......</strong> makes the text bold.
Try to avoid using the u(underline tag) tag when it could be confused for a link. Anchor tags also have a default underlined formatting.
or text-decoration: underline;

To emphasize text, you can use the em tag. This displays text as italicized, as the browser applies the CSS of font-style: italic; to the element.

To strikethrough text, which is when a horizontal line cuts across the characters, you can use the s tag. It shows that a section of text is no longer valid. With the s tag, the browser applies the CSS of text-decoration: line-through; to the element.

- hr tag used to add a horizontal line across the width of its containing element. This can be used to define a change in topic or to visually separate groups of content.
hr is a self-closing tag, and therefore doesn't need a separate closing tag.

rgba() is great to use it allows to adjust the opacity. it doesn't completely block out the background.

background-color: rgba(45, 45, 45, 0.1) produces a dark gray color that is nearly transparent given the low opacity value of 0.1.

The font size of heading elements (h1 through h6) should generally be larger than the font size of paragraph tags. 

The box-shadow property takes values for

offset-x (how far to push the shadow horizontally from the element),
offset-y (how far to push the shadow vertically from the element),
blur-radius,
spread-radius and
color, in that order.

The opacity property in CSS is used to adjust the opacity, or conversely, the transparency for an item.

A value of 1 is opaque, which isn't transparent at all.
A value of 0.5 is half see-through.
A value of 0 is completely transparent.

text-transformvalues change the example text "Transform me".

Value	Result
lowercase	"transform me"
uppercase	"TRANSFORM ME"
capitalize	"Transform Me"
initial	Use the default value
inherit	Use the text-transform value from the parent element
none	Default: Use the original text

h1 tag to 68px.
h2 tag to 52px.
h3 tag to 40px.
h4 tag to 32px.
h5 tag to 21px.
h6 tag to 14px.

line-height property to change the height of each line in a block of text. As the name suggests, it changes the amount of vertical space that each line of text gets.

 A pseudo-class is a keyword that can be added to selectors, in order to select a specific state of the element.
 a:hover{
     color: red;
 }

 CSS treats each HTML element as its own box, which is usually referred to as the CSS Box Model. Block-level items automatically start on a new line (think headings, paragraphs, and divs) while inline items sit within surrounding content (like images or spans). The default layout of elements in this way is called the normal flow of a document, but CSS offers the position property to override it.

When the position of an element is set to relative, it allows you to specify how CSS should move it relative to its current position in the normal flow of the page. It pairs with the CSS offset properties of left or right, and top or bottom. These say how many pixels, percentages, or ems to move the item away from where it is normally positioned. The following example moves the paragraph 10 pixels away from the bottom:

p {
  position: relative;
  bottom: 10px;
}
Changing an element's position to relative does not remove it from the normal flow - other elements around it still behave as if that item were in its default position.

Note: Positioning gives you a lot of flexibility and power over the visual layout of a page. It's good to remember that no matter the position of elements, the underlying HTML markup should be organized and make sense when read from top to bottom. This is how users with visual impairments (who rely on assistive devices like screen readers) access your content.

You're offsetting an element away from a given spot, which moves the element away from the referenced side (effectively, the opposite direction)

Lock an Element to its Parent with Absolute Positioning
absolute, locks the element in place relative to its parent container. Unlike the relative position, this removes the element from the normal flow of the document, so surrounding items ignore it. The CSS offset properties (top or bottom and left or right) are used to adjust the position.

One nuance with absolute positioning is that it will be locked relative to its closest positioned ancestor. If you forget to add a position rule to the parent item, (this is typically done using position: relative;), the browser will keep looking up the chain and ultimately default to the body tag.

Lock an Element to the Browser Window with Fixed Positioning:
element with a fixed position won't move when the user scrolls.
- can be used to fixed the navbar.
position: fixed;
top: 0px;
left : 0px;

The section element represents a generic section of a document or application. A section, in this context, is a thematic grouping of content. Each section should be identified, typically by including a heading ( h1- h6 element) as a child of the section element.

The aside element represents a section of a page that consists of content that is tangentially related to the content around the aside element, and which could be considered separate from that content. Such sections are often represented as sidebars in printed typography.

Change the Position of Overlapping Elements with the z-index Property
When elements are positioned to overlap (i.e. using position: absolute | relative | fixed | sticky), the element coming later in the HTML markup will, by default, appear on the top of the other elements. However, the z-index property can specify the order of how elements are stacked on top of one another. It must be an integer (i.e. a whole number and not a decimal), and higher values for the z-index property of an element move it higher in the stack than those with lower values.

Center an Element Horizontally Using the margin Property
Another positioning technique is to center a block element horizontally. One way to do this is to set its margin to a value of auto.

This method works for images, too. Images are inline elements by default, but can be changed to block elements when you set the display property to block.

Some examples of complementary colors with their hex codes are:
red (#FF0000) and cyan (#00FFFF)
green (#00FF00) and magenta (#FF00FF)
blue (#0000FF) and yellow (#FFFF00)

Hue is what people generally think of as 'color'. If you picture a spectrum of colors starting with red on the left, moving through green in the middle, and blue on right, the hue is where a color fits along this line. In hsl(), hue uses a color wheel concept instead of the spectrum, where the angle of the color on the circle is given as a value between 0 and 360.

Saturation is the amount of gray in a color. A fully saturated color has no gray in it, and a minimally saturated color is almost completely gray. This is given as a percentage with 100% being fully saturated.

Lightness is the amount of white or black in a color. A percentage is given ranging from 0% (black) to 100% (white), where 50% is the normal color.

background: linear-gradient(90deg, red, yellow, rgb(204, 204, 255));
 background: repeating-linear-gradient(
      45deg,
      yellow 0px,
      yellow 40px,
      black 40px,
      black 80px
    );

One way to add texture and interest to a background and have it stand out more is to add a subtle pattern. The key is balance, as you don't want the background to stand out too much, and take away from the foreground. The background property supports the url() function in order to link to an image of the chosen texture or pattern. The link address is wrapped in quotes inside the parentheses.
background: url("https://cdn-media-1.freecodecamp.org/imgr/MJAkxbh.png");

Use the CSS Transform scale Property to Change the Size of an Element
p {
  transform: scale(2);
}

To scale the paragraph elements to 2.1 times their original size when a user hovers over them:

p:hover {
  transform: scale(2.1);
}
Note: Applying a transform to a div element will also affect any child elements contained in the div.

::before and ::after pseudo-elements are used to add something before or after a selected element.

Use CSS Animation to Change the Hover State of a Button
You can use CSS @keyframes to change the color of a button in its hover state.

Here's an example of changing the width of an image on hover:

<style>
  img {
    width: 30px;
  }
  img:hover {
    animation-name: width;
    animation-duration: 500ms;
    animation-fill-mode: forwards;
  }

  @keyframes width {
    100% {
      width: 40px;
    }
  }
</style>
the animation resets after 500ms has passed, causing the button to revert back to the original color. You want the button to stay highlighted. This can be done by setting the animation-fill-mode property to forwards.