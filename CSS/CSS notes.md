CSS - Cascading Style Sheets

To comment out text in CSS you use
/* Comment here */

In-line CSS is used within the HTML document to impliment CSS changes:

the <body style=""> tag takes css code as input
There are several methods to specify the colour.
    <body style="background-color: aquamarine;">
    <body style="background-color: rgb(255, 255, 128);">
    <body style="background-color: #E8F9FD;">

Use sites like: https://colorhunt.co/
to find the best hexcodes for matching colour schemes.

Internal CSS is used to affect all style choices with the HTML document but only needs to be specified once:
CSS style is injected via <style> tags:
    <style>
        tagName {CSS-styling}
    </style>

Here you can edit the background-colour, height, width, shading of elements.
CSS stylings should end in ; and be surrounded by curly brackets {}
Pixel dimensions should be specified as 12px
Pixel dimensions can also be specified as a percentage of the screen for better scalability with a range of devices as 12%

You will have to copy the internal CSS settings betwen common functions in different web pages, which is not ideal.
External CSS is used to set the CSS once and have it apply to all of the pages when it is called.
* Put the style code in /CSS/styles.css
* Remove the <stlyle></stlyle> tags containing the styling.
* In the head put a <link> element in the format
    <link rel="stylesheet" href="CSS/styles.css">
* if the website it hosted, href should contain a root /
    <link rel="stylesheet" href="/CSS/styles.css">
You need the style sheet to be referenced in all the document pages that you want it to apply to.

Debugging can be done with the Chrome Developer Tools.
    * 3 dots
    * more tools
    * Developer tools
In the console, you can read any issues there are in loading the files.
In the elements tab, you can see the CSS styles applied to each element.
Here you can see overlapping style applications.

The hierarchy of CSS inheritance if there are several overlapping assignments goes:
    1) In-line CSS
    2) Internal CSS
    3) External CSS 
For best practice, it is recommended to store all style changes in external CSS document.

CSS Syntax - Grammar of the language:
    selector{property:value;}
        selector - who? Who's style do you want to change? H1, Para, img?
        property - what? What do you want to change? Colour, border, etc.
        value - how? How much do you want it to change by?
A ; symbol is needed to close the code in CSS.

By convention, CSS styling is spread with one style for each new line in alphabetical order.
    h1{
        color: red; 
        font-size: 200px;
    }

The MDN reference site has a list of all the proerties that can be changed with CSS.
https://developer.mozilla.org/en-US/docs/Web/CSS/Reference

Inside the <img> tag you can add a class="" selector to differentiate between multiple of the same tag - say 2 titles or 2 images.
Then you can apply the CSS changing code to a specific title/image instead of all of them.
The class selector takes priority over the tag selector.

To apply CSS to a class instead of a tag it uses a .notation.
    .headingTitle{
        color: red; 
        font-size: 200px;
    }

You can do similar things with the heading="" selector within the HTML element <tag>.
To change the CSS of the id in the .css file, type #idName and continue as normal.
Once again, the id specific CSS overrules the <tag> CSS.
    #idName{
        color: red; 
        font-size: 200px;
    }

Each unique ID can only be used once per page.
    - Use to apply a specific style to a unique object.
Classes however can be asigned to multiple tags.
    - Use when you want to apply the same style to a group of related items.

Each HTML element can have more than one class, but it can only have one ID.
To assign multiple classes to a single HTML element, separate them with a space.
    <img class="red circular huge">

Pseudo classes are identified by starting with a :.
They are applied to HTML elements in the CSS sheet in the class section. E.g. img:hover.
HTML elements have different states which can be activated by varying actions, such as hovering over.
The CSS pseudo-class specifies which special state of the selected element to apply to.
https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes
    img:hover{
        background-color: gold;
        blur:(1px);
    }

Favicons are the image shown on the left of the page title.
You use a <link> to tell the page to find the "icon" and the location.

<div> is used to separate groups of HTML elements.
It allows us to structure and divide content.

When specifying a dimension of 0, you do not need to specify the unit (e.g. px or %)

Padding only pads the content, not background image or colours.

CSS Display property:
    in css:
        element{
            display:choice;
        }
* Block
    Take up the whole width of the screen.
    <p>
    <h1>
    <div>
    <list> <ol> <ul>
    <form>
* Inline
    Allow you to style specific parts of block elements.
    You can create multipe inline elements that sit on the same shelf-height.
    However, you lose the ability to change the width of these elements.
    <span>
    <img>
    <anchor> <a>
* Inline-Block
    <img>
    Allows you to group elements inline and have control over their size.
* None
    Gets rid of the element.

To hide things from the site, but maintain the behaviour of other CSS elements around the hidden element, use the visibility parameter:
.class{
    visibility:hidden;
}

The position property:
.class{
    position:choice;
}
    * Static
        Default CSS values without CSS present.
    * Relative
        Relative positioning to Static values.
        Acts as a margin on the applied face - top applies a margin on the top of the static location, moving the image down. right moves left.
        Does not affect any other elements on the page.
            img{
                position:relative
                top:50px;
                right:10px;
            }
    * Absolute
        Relative positioning to the parent - page, div, etc.
        Does affect the other elements on the page.
        Takes the element out of the flow of the document.
    * Fixed
        Maintains the position of the element as the user scrolls through the website.

text-align:center;
Aligns all text that does not have a width set.
If a width is set, you need to use the margin:auto; param.

You can specify font-family fallbacks.
Using multiple parameters, if the browser cannot load the font you specifically want it cascades down the list until one works.
The last option should be a generic font-family to increase effectiveness.
    font-family: verdana, sans-serif;

You can embed fonts into your website if you would rather not take the risk of a different user experience.
In the <head> you can <link> to online-hosted fonts.

You can specify font size in %.
    100% is size 16px.
font can also be specified in terms of em;
    The width of the capital letter M.
    font-size: 2em;
    1em = 16px
Using % and em leads to inheritance.
Body size font size gets used for heading.
if body = 2em and h1 = 5em, then h1 really leads to 10em