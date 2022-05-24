HTML - HyperText Markup Language

Contents are wrapped in <tags> </tags>.

<heading> tags decrease in size with larger numbers </heading>
<h1>Largest</h1>
<h2>Medium</h2>
<h6>smallest</h6>

For searching for help, search "html mdn" with the keywords in the browser.
devdocs.io

Linebreaks are given as <br>. It works like \n in python.
<br> does not need a closing tag. It is a self-closing tag.

The <hr> tag is another self-closing tag.
These provide horizontal-ruled lines to the page.

HTML attributes can be applied to the HTML element.
<hr size="3" noshade>

<center> is used to centre-align the content. </center>

<!-- This is how you comment a line in HTML -->
<!-- They 
    can 
    be 
    multiline -->

UTF-8 is a good pairing for HTML as it includes symbols from many languages across the world. 
It also includes some emoji support.

<h1></h1> Heading
<p></p> Paragraph
<ul></ul> Unordered list
<ol></ol> Ordered list
<li></li> List item within the list

<em></em> Adds emphasis and italics.
<i></i> Adds just italics.
<strong></strong> Strong important and is in bold.
<b></b> Makes it bold.

<img> is a self-closing tag.
<img src="Image/example.png"> The source can be a URL from online or a local copy.
<img src="example.png" alt="Description of the image"> Use alt to provide a text alternative description of the image.

<a></a> anchor tags allow you to insert hyperlinks.
<a href="https://Site to Go to..."> Words to click to be sent to link</a>
<a href="Images/img"> You can even link to images</a>

<table> is used to create tables
    <tr> Creates a table row
        <td> Creates a cell within the row
        </td>
    </tr>
</table>

Using headers and body tags within the table allow you to isolate it for later customisation.
For instance, for long tables, you can fix the header in place as you scroll through the contents of the table.
Styling of the table should be left to CSS.

<table> is used to create tables
    <thead> Creates a row title header in the table.
        <th>ROW 1</th>
        <th>ROW 2</th>
    </thead>
    <tbody> Creates the body of the table.
        <tr>
            <td>
            </td>
        </tr>
    </tbody>
    <tfoot>
    </tfoot>
</table>

Forms can be used to collect data from the user.
<form>
    <label></label> are used to indicate the user response
    <input> are used to generate the method of user response
    <textarea> allows the user to input multiple lines for their text entry
</form>
Inputs can be: checkboxes, empty boxes, poassword boxes, submit boxes etc.
https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input

<form class="" action="mailto:email@address.co.uk" method="post">
The mailto: action opens up the default email browser on the computer with the pre-filled destination address as specified.