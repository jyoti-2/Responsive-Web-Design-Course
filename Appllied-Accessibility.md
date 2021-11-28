In web development, accessibility refers to web content and a UI (user interface) that can be understood, navigated, and interacted with by a broad audience. This includes people with visual, auditory, mobility, or cognitive disabilities.

Add a Text Alternative to Images for Visually Impaired Accessibility.
alt text describes the image's content and provides a text-alternative for it. An alt attribute helps in cases where the image fails to load or can't be seen by a user. Search engines also use it to understand what an image contains to include it in search results. 
<img src="importantLogo.jpeg" alt="Company logo">
People with visual impairments rely on screen readers to convert web content to an audio interface. They won't get information if it's only presented visually. For images, screen readers can access the alt attribute and read its contents to deliver key information.

alt can be a empty string. If the image is self described.

Use Headings to Show Hierarchical Relationships of Content - 
Semantic meaning means that the tag you use around content indicates the type of information it contains.

The main element is used to wrap the main content, and there should be only one per page. It's meant to surround the information related to your page's central topic. It's not meant to include items that repeat across pages, like navigation links or banners.

The main tag also has an embedded landmark feature that assistive technology can us to navigate to the main content quickly. If you have ever seen a jump to Main content link at the top of a page, using the main tag automatically gives assistive devices that functionality.

article is a sectioning element and is used to wrap independent, self-contained content. The tag works well with blog entries, forum posts, or news articles.

<div> - groups content <section> - groups related content <article> - groups independent, self-contained content

Make Screen Reader Navigation Easier with the header Landmark.

Make Screen Reader Navigation Easier with the nav Landmark
<nav>
      <ul>
        <li><a href="#combat">Combat</a></li>
        <li><a href="#weapons">Weapons</a></li>
      </ul>
</nav>

Make Screen Reader Navigation Easier with the footer Landmark.
Similar to header and nav, the footer element has a built-in landmark feature that allows assistive devices to quickly navigate to it. It's primarily used to contain copyright information or links to related documents that usually sit at the bottom of a page.
(footer element).

Improving the accessibility of the audio content.
An audio element represents a sound or audio stream.
The source element allows authors to specify multiple alternative media resources for media elements. It does not represent anything on its own.

If this attribute is present, the browser will offer controls to allow the user to control audio playback, including volume, seeking, and pause/resume playback.

<audio controls>
<source src="https://amazonaws.com/screen-reader.mp3" type="audio/mpeg">
</audio>

Improve Chart Accessibility with the figure Element.

figure element and the related figcaption. Used together, these items wrap a visual representation (like an image, diagram, or chart) along with its caption. Wrapping these elements together gives a two-fold accessibility boost by semantically grouping related content and providing a text alternative explaining the figure.

For data visualizations like charts, the caption can be used to briefly note the trends or conclusions for users with visual impairments. Another challenge covers how to move a table version of the chart's data off-screen (using CSS) for screen reader users.

Here's an example - note that the figcaption goes inside the figure tags and can be combined with other elements:

<figure>
  <img src="roundhouseDestruction.jpeg" alt="Photo of Camper Cat executing a roundhouse kick">
  <br>
  <figcaption>
    Master Camper Cat demonstrates proper form of a roundhouse kick.
  </figcaption>
</figure>

Improve Form Field Accessibility with the label Element.

Improving accessibility with semantic HTML markup applies to using both appropriate tag names and attributes.

The label tag wraps the text for a specific form control item, usually the name or label for a choice. This ties meaning to the item and makes the form more readable. The for attribute on a label tag explicitly associates that label with the form control and is used by screen readers.

The value of the for attribute must be the same as the value of the id attribute of the form control. Here's an example:

<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name">
</form>


Wrap Radio Buttons in a fieldset Element for Better Accessibility

The fieldset tag surrounds the entire grouping of radio buttons to achieve this. It often uses a legend tag to provide a description for the grouping, which screen readers read for each choice in the fieldset element.

The fieldset wrapper and legend tag are not necessary when the choices are self-explanatory, like a gender selection. Using a label with the for attribute for each radio button is sufficient.

Here's an example:

<form>
  <fieldset>
    <legend>Choose one of these three items:</legend>
    <input id="one" type="radio" name="items" value="one">
    <label for="one">Choice One</label><br>
    <input id="two" type="radio" name="items" value="two">
    <label for="two">Choice Two</label><br>
    <input id="three" type="radio" name="items" value="three">
    <label for="three">Choice Three</label>
  </fieldset>
</form>

Add an Accessible Date Picker
Forms often include the input field, which can be used to create several different form controls. The type attribute on this element indicates what kind of input element will be created.
Depending on browser support, a date picker shows up in the input field when it's in focus, which makes filling in a form easier for all users.

<label for="date-picker">Enter a date:</label>
<input type="date" id="date-picker" name="date">

Standardize Times with the HTML5 datetime Attribute.

time element along with a datetime attribute to standardize times. The time element is an inline element that can wrap a date or time on a page. A datetime attribute holds a valid format of that date. 

<p>Master Camper<time datetime="2013-02-13">last Wednesday</time>, which ended in a draw.</p>

15th => 15<sup>th</sup>

display: none; or visibility: hidden; hides content for everyone, including screen reader users
Zero values for pixel sizes, such as width: 0px; height: 0px; removes that element from the flow of your document, meaning screen readers will ignore it

Improve Readability with High Contrast Text.

Low contrast between the foreground and background colors can make text difficult to read. Sufficient contrast improves your content's readability, but what exactly does "sufficient" mean?

The Web Content Accessibility Guidelines (WCAG) recommend at least a 4.5 to 1 contrast ratio for normal text. The ratio is calculated by comparing the relative luminance values of two colors. This ranges from 1:1 for the same color, or no contrast, to 21:1 for white against black, the most substantial contrast. There are many contrast checking tools available online that calculate this ratio for you.

Note: Some online color picking tools include visual simulations of how colors appear for different types of colorblindness. These are great resources in addition to online contrast checking calculators.

Give Links Meaning by Using Descriptive Link Text
<a href="">information about batteries</a>

Make Links Navigable with HTML Access Keys
HTML offers the accesskey attribute to specify a shortcut key to activate or bring focus to an element. Adding an accesskey attribute can make navigation more efficient for keyboard-only users.
<button accesskey="b">Important Button</button>

