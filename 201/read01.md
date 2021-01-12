# 201 class 01 reading notes: Introductory HTML and JavaScript
## Introduction (pp.2-11)
- Is It hard to learn?
    - Many books that teach HTML and CSS resemble dull manuals
    - To make it easier for you to lean, we threw away the traditional template used by publishers and redesigned this book from scratch.
- The Structure of this book 
    - Html: Learning how use HTML to create web pages
    - CSS: Presentation and Layout
    - Practical: Look at HTML5 to help describe the structure of your pages
- How people access the web
    - Browsers: People access websites using software called a web browser
    - Web Severs: When you ask your browser for a web page, the request is sent across the Internet to a special comptuter known as a web server which hosts the website
    - Screen Readers: Programs that read out the contents of a computer screen to a user
    - Devices: People are accessing websites on an increasing range of devices including desktop computers, laptops, tablets, and mobile phones
- How are websites created
    - What you see: When you are looking at a website, it is most likely that your browser will be receiving HTML and CSS from the web server that hosts the site.
- How it is created
    - Small websites are often written just using HTML and CSS
    - HTML5 & CSS3: Since the web was first created there have been several versions of HTML and CSS - each intended to be an improvement on the previous version
- How the web works
     - When you visit a website, the web server hosting that site could be anywhere in the world. In order for you to find the location of the web server, your browser will first connect to a Domain Name System (DNS) server
## HTML Chapter 1: “Structure” (pp.12-39)
- HTML pages are text documents
- HTML uses tags (character that sit inside angled brackets) to give the information they surround special meaning
- Tags are often reffered to as elements
- Tags usually come in pairs. The opening tag denotes the start of a piece of content; the closing tag denotes the end.
- Opening tags can carry attributes, which tell us more about the content of that element
- Attributes require a name and a value
- To learn HTML you need to know what tags are available for you to use, what they do, and where they can go
## HTML Chapter 8: “Extra Markup” (p.176-199)
- DOCTYPES tell browsers which version of HTML you are using
- You can add commments to your code between the <!-- and -->
- The id and class attributes allow you to identify particular elements.
- The <div> and <span> elements allow you to group block-level and inline elements together
- <iframes> cut windows into your web pages through which other pages can be displayed.
- The <meta> tag allows you to supply all kinds of information about your web page
- Escape characters are used to include special characters in your pages such as <,>, and copyright
## HTML Chapter 17: “HTML5 Layout” (pp.428-451)
- Traditional HTML Layouts
    - For a long time, web page authors used <div> elemetns to group together related elements on the page (such as the elements that form a header, an article, footer or sidebar). 
    - Authors used class or if attributes to indicate the role of the <div> element in the structure of the page.
- New HTML5 Layout Elements
    - HTML5 introduces a new set of elements that allow you to divide up the parts of a page. 
    - The Names of these elements indicate the kind of content you will find in them.
    - They are still subject to change, but that has not stopped many web page authors from using them already
- Headers & Footers
    - The main header or footer that appears at the top or bottom of every page
    - A header or footer for an individual <article> or <section> within the page
- Nav 
    - The <nav> element is used to contain the major navigational blocks on the site such as the primary site navigation
- Articles 
    - The <article> element acts as a container for any section of a page that could stand alone and potentially be syndicated
- Sections
    - The <section> element grgoups related content together, and typically each section would have its own heading
- Heading groups 
     - The purpose of the <hgroup> element is to group together a set of one or more <h1> through <h6> elements so that they are treated as one single heading.
- To make HTML5 elements work in Internet Explorer 8, extra JavaScript is needed, which is avaliable free from Google.
## HTML Chapter 18: “Process & Design” (pp.452-475) 
- It is important to understand who your target audience is, why they would could to your site, what information they want to return
- Site maps allow you to plan the structure of a site
- Wireframes allow you to organize the information that will need to go in each space
- Design is about communication. Visual hierarchy helps visitors understand what you are trying to tell them
- You can differtiate between pieces of information using size, color, and style
- You can use grouping and similarity to help simplify the information you present
## Introduction
- This book explains how JavaScript can be used in browsers to make websites more interactive, interesting, and user-friendly.
- You will also learn about jQuery because it makes writing JavaScript a lot easier
## JS Chapter 1: “The ABC of Programming” (pp.11-52)
- It is best to keep JavaScript code in its own Javscript file. JavaScript text files (like HTML pages and CSS style sheets), but they have the .js extension
- The HTML <script> element is used in HTML pages to tell the browser to load the JavaScript file (rather like the <link> element can be used to load a CSS)
- If you view the cource code of the page in the browser, the JavaScript will not have changed the HTML, because the script works with the model of the web page that the browser has created.