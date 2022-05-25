CSS - Cascading Style Sheets

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
    tagName {CSS styling}
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