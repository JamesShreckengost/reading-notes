# Read: 09 - Forms and Events
## Chapter 7: “Forms” (p.144-175)
- Traditionally, the term 'form has reffered to a printed document that contains spaces for you to fill in information.
- Why Forms 
  - The best known form on the web is probably the search box that sits right in the middle of google's homepage.
- Form Controls 
  - There are several types of form controls that you can use to collect information from visitors to your site.
    - Adding Text: Text input, Password input, Text area
    - Making Choices: Radio buttons, Checkboxes, Drop-down boxes
    - Submitting Forms: Submit buttons, Image buttons, Uploading files: File upload.
### How forms work 
- A user fills ina form and then presses a button to submit the information to the server.
- A from may have several controls, each gathering different infomation. The server needs to know which piece of inputted data corresponds with which from element.
### Form Structire
- <form>
  - Form controls live inside a <form> element. This element should always carry the action attribute and will usually have a method and id attribute too.
- action
  - Every <form> element requires an action attribute. Its value is the Url for the page on the server that will recieve the information in the form when it is submitted.
- method
  - Forms can be sent using one of two methods: get or post
### Text Input
- The <input> elements is used to create several different form controls. The value of the type attribute determins what kind of input they will be creating.
- type="text": When the type attribute has a value of text, it creates a single-line text input.
- name: When users enter information into a form, the server needs to know which form control each piece of data was entered too.
- Maxlength: You can use the maxlength attribute to limit the number of characters a user my enter.
- Password input is basically the same as text input but for a password
- <textarea> elements is used to create a multi-line text-input.
- radio button: type="radio", name, value, checked
- Checkbox: type="checkbox", name, value, checked
### Summary 
- Whenever you want to collect information from visitors you will need a form, which lives insides a <form> element.
- Information from a form is sent in name/value pairs
- Each form control is given a name,, and the text the user types in or the values of the options they select are sent to the server.
- HTML5 introduces new form elements which make it easier for visitors to fill in forms.
## Chapter 14: “Lists, Tables & Forms” (pp.330-357)
- There were several CSS properties that were created to work with specific types of HTML elements, such as lists, tables, and forms.
### List style position
- the list-style-type property allows you to control the shape or style of a bullet point.
- You can specify an image to act as abullet point using the list-style-image property
- lists are indented into the page by default and the list-style-position property indicates whether the marker should appear on the inside or the outside of the box containing the main points.
  - outside: The marker sits to the left of the block of text.
  - indside: the marker sits inside the box of text
### Table Properties
- width, padding, text-transform, letter-spacing, font-size, border-top, border-bottom, text align, background-color, :hover
- give cells padding, distinguish headings, shade alternate rows, align numerals, online extra
### Cells
- if you empty cells in your table, then you can use the empty-cell property to specify wither or not their borders would be shown.
- show: shows the borders of any empty cells
- hide: hides the borders of any empty cells
- inherit: if you have one table nested inside another, the inherit value instructs the table cells to obey the rules of the containing table.
- collapse: borders are collapsed into a single border where possible.
- Seperate: borders are detached from each other
### Summary
- In addition to the CSS properties covered in other chapters which work with the contents of all elements, there are several others that are specifically used to control the appearance of lists, tables, and forms.
- List markers can be given differen appearances using the list-style-type and list-style image properties
- Table cells have different borders and spacing in different browsers, but there are properties you can use to control them and make them more consistent
- Forms are easier to use if the form control are vertically aligned using CSS
- Forms benefit from styles that make them feel more interactive.

