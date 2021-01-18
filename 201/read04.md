# Read 04 Notes: HTML Links, CSS Layout, JS Functions
## (HTML) Chapter 4: Ch.4 “Links” (pp.74-93)
  - Links are the defining feature of the web because they allow you to move from one web page to antother -- enabling the very idea of browsing or surfing.
### Writing Links
  - Links are created using the <a> element. Users can click on anything between the opening <a> tag and the closing </a> tag. You specify which page you want to link to using the href attribute.
### Linking to Other Sites
   - Links are created using the <a> element which has an attribute element which has an attribute called href. The vlaue of the href attribute is the page that you want people to go to when they click on the link.
   - When you link to a different website, the value of the href attribute will be the full web addres for the site which is known as an absolute URL
### Linking to Other Pages On the Same Website
  - When you are linking to other pages within the same site, you do not need to specify the domain name in the URL. You can use a shorthand known as a relative URL.
  - If all the pages of the site are in the same folder, then the value of the href attribute is just the name of the file.
### Directory Structure
  - On larger websites its a good idea to organize your code by placing the pages for each different section of the site into a new folder. Folders on a website are sometimes reffered to as directories.
    - Structure
      - The top level folder is known as the root folder.
      - The root folder contains all of the other files and folders for a website.
      - Each section of the site is placed in a seperate folder; This helps organize the files.
    - Relationships
      - The relationship between files and folders on a website is described sing the smae terminology as family tree.
    - Home Pages
      - The main homepage of a site written in HTML (and the homepages of each section in a child folder) is called index.html
      - Webservers are usually set up to return the inde.html file if no file name is specified.
    - Every page and every image on a website has a URL. The URL is made up of the domain name followed by the path to that page or image.
### Relative Urls
- Relative Urls can be used when linking to pages within your own website. They provide a shorthand way of telling the browser where to find your files.
  - Same Folder
    - To link a file in the same folder, just use the file name.(Nothing else is needed.)
  - Child Folder
    - For a child folder, use the name of the child folder, followed by a forward slash, then the name.
  - Grandchild Folder
    - Use the name of the child folder, followed by a forward slash, then the name of the grandchild folder, followed by another forward slash, then the file name.
  - Parent folder
    - Use ../ to indicate the folder above the current one, then follow it with the file name.
  - Granparent folder
    - Repeat ../ to indicate that you want to go up two folders (rather than one), then follow it with the file name.
### Email Links
  - Mailto:
    - To create a link that starts up the user's email program and addresses an email to a specified email address, you use the <a> element. However, this time the value of the href attribute starts with mailto: aand is followed by the email address you want the amil to be went to
### Opening Links in a New Window 
  - Target
    - If you want a link to open in a new window, you can use the target, attribute on the opening<a>tag. You value of this attribute should be _blank.
### Linking to a specific part of the same page
  - To link an element that uses an id attribute you use the <a> element again, but the value of the href attribute strta with ehe # symbol, followed by the value of the id attribute you want to link to. 
### Summary 
  - Links are created using the <a> element
  - The <a> element uses the href attribute to indicate the page you are linking to.
  - If you are linking to a page within your own site, it is best to use relative links rather than qualified URLS.
  - You can create links to open email programs with an email address in the "to" field.
  - You can use if attribute to target elements within a page that cna be linked to.
## (HTML) Chapter 15: “Layout” (pp.358-404)
- In this chapter we are going to look at how to control where each element sits on a page and hwo to create attractive page layouts.
### Key concepts in positioning elements
  - Building Blocks
    - CSS treats each HTMl element as if it is in its own its own boc. This box will will either be a block-level box or an inline block.
  - Containig Elements
    - If one block-level element sits inside another block-level element then the outer box is kown as the containing or parent elements.
  - Controlling the position of the elements
    - Css has the following positioning schemes that allow you to control the layout of a page: normal flow, relative postitioning, and abosulte positioning. You can specify the positioning scheme using the position property in CSS. You can also float elements using the float property.
    - To indicate where a box should be positioned, you may also need to use box offest properties to tell the browser how far from the top or bottom and left or right it should be placed.
      - Normal flow
        - Every block-level element appeats on a new line, causing each item to appear lower down the page than the previous one. 
        - Even if you specify the width of the boxed and there is space for two elements to sit side by side, they will not appear nect to each other.
        - This is the default behavior
      - Relative Postioning
        - The moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left where it would have been placed.
        - This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.
      - Absolute Positioning
        - This positions the element in relation to its containing element. 
        - It is taken out of normal flow m meaning that it does not affect the position of any surrounding elements.
        - Absolute positioned elemtnts move as users scroll up and down the page.
      - Fixed Positioning
        - This is a form of absolute positioning that postions the elemnt in relation to the browser window, as opposed to the containing element.
        - Elements with fixed positioning do not affect the position of surrounding elements and they do not move when the user scrools up or down the page
      - Floating elements
        - Floating an element allows you to take that element out of normal flow and position it to the far left or right of a containing box.
        - The floated element becomes a block-level element around which other content can flow.
  - When you move any element from normal flowm boxes can overlap. The z-index property allows you to control which box appears on top.
### Normal Flow
- Position:static
  - In normal flow, each block-level elements sits on top of the nect one.
  - Since this is the default way in which browsers treat HTML elements, you do not need a CSS property to indicate that elemtns should appear in normal flow, but the syntax would be - postion: static;
- Position:relative
  - Relative positioning moves an element in relation to where it would have beeb in normal flow
- Position:absolute
  - When the position property is given a value of absolute, the box is taken out of nromal flow and no longer affects the position of other elements on the page.
- postiion:fixed
  - Fixed postioning is a type of absolute positioning that requires the position property to have a value of fixed.
### Overlapping Elements
- z-index
  - When you use relative, fixed, or absolute positioning, boxes can overlap. if boxed so overlap, the elements that appear later in the HTML code sit on top those that earlier in the page. 
### Floating Elements
- float
  - The float property allows you to take an element in normal flow and place it as far to the left or right of the containing element as possible.
  - a lot of layouts place boxes next to each other. The float property is commonly used to achieve this. 
  - When elements are floated, the height of the boxes can affec whwre the following elements sit.
### Clearing Floats 
- clear
  - The clear property allows you to say that no element should touch the left or right hand sides of a box. it can take the following values:
    - left, right, both, none
### Parents of Floated Elements
- Problem
  - If a contianing element only contains floated elements, some browsers will treat is as if it is zero pixels tall
- Solution
  - Traditionally, developers got around this problem by adding an extra element the last floated box. 
  - A CSS rule would be applied to this additonal element setting the clear property to have a value of both. But this meant that an extra element was aded to the HTML just to fix the height of the containing element.
  - More recently, developers have opted for a purely CSS-based solution because it menas that there is no need to added to the HTML just to fix the height of the containg elements.
  - The pure CSS solution adds two CSS rules to the containing element.
### Creating Multi-Column Layouts With Floats
- Many web pages use multiple columns in their design. This is achieved by using a <div> element to represent each column. 
- The following three CSS properties are used to postion the columns next to each other:
  - Width: This sets the width of the columns
  - Float: This potions the columns next to each other
  - Margin: This creates a gap between the columns
### Screen Sizes 
- Different visitors to your site will have different sized screens that show different amounts of information, so your design needs to be able to work on a range differnt sized screens.
- Resolution refers to the number of dots a screene shows per inch. Some devices have a higher resolution than desktop computers and most operating systems allows users to adjust the resolution of their screens.
### Page Sizes
- Because scren sizes and display resolutions vary so much, web deisgners often try to create pages of around 960-1000 pixels wide.
### Fixed Width Layouts
- Fixed width layout designs do not change size as the user increases or decreases the size of their browser window. Measurements tend to be given in pixels.
- To create a fixed width layout, the width of the main boxes on a page will usually be specified in pixels.
### Liqiud Layouts
- Liquid layouts designs stretch and contract as the user increases or decreases the size of their browser window. They tend user percentages.
### Layout Grids
- Composition in any visual art is the placement or arrangement of visual elements -- how they are organized on page. Many designers use a grid structure to help them position items on apge, and the same is true for web designers.
### CSS Framewprk
- CSS frameworks aim to make your life easier by providing the code for common tasks, such as creating layout grids, styling forms, creating printer-friendly versions of pages and so on. You can include the CSS framework code in your projects rather than writing the CSS from scratch.
### Summary
- <div> elements are often used as containing elements to group together sections of a page.
- Browsers display pages in normal fflow unless you specify relative, absolute, or fixed postioning.
- The float property moves content to the left or right of the page and can be used to creat multi-column layouts.
- Pages can be fixed width or liqiud (stretchy) layouts
- Designers keep pages within 960-1000 pixels wide, and indicate what the site is about within the top 600 pixels.
- Grids help create professional and flexible designs
- CSS Frameworks provide rules for cmmon tasks
- You can include multiple CSS files in one page.
## (JavaScript) Chapter 3: “Functions, Methods, and Objects” (pp.86-99 ONLY)
- Browsers require very detailed instructions about what we want them to do. Therefore, complex scripts can run to hundreds of lines. Programmers use functions, methods, and objects to organize their code. 
### What is a function
- Functions let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function
- When you ask it to perform a task, it is known as calling a function.
- Pieces of information passed to a function are known as parameters.
- When you write a function and you expect it to provide you with an answer, the repsonse is known as return value.
### Declaring a Function
- To create a function, you give it a name and then write the statements neede to achieve its task inside the curly braces.
- This is known as a function declaration
### Calling a Function
- Having declared the function, you can then execute all of the statements between its curly braces with just one line of code. This is known as calling a function.
### Declaring Functions that need information
- Sometimes a function needs specific information to perform its task. In such cases, when you declare the function you give it parameters. Inside the function, the parameters act like variables
- WHen you call a function that has paramters, you specify the values it should use in the parentheses that follow its name. The values are called arguments, and they can be provided as values or variables.
## Article: “6 Reasons for Pair Programming”
### How does it work
- pair programming commonly involves two roles: the Driver and the Navigator. The Driver is the programmer who is typing and the only one whose hands are on the keyboard.
- Handling the "mechanics" of coding, the Driver manages the text editor, swithcing files, version control, and of course writing code.
- The Navigator thinks about the big picture, what comes next, how an algorithm might be converted in to code, while scanning for typos or bugs.
- The Navigator might also utlize their computer as a second screen to look up solutions and documentation, but should not be writing any code.
### Why pair program
- Pair programming touches on all four skills: developers explain out loud what the code should do, listen to others' guidance, read code that others have written, and write code themselves.
- Greater Effiency
- Engaged Collaboration
- Learning from fellows students
- Social skills
- Job interview readiness
- Work environment readiness