# Reading Notes 05: HTML Images; CSS Color & Text
## Chapter 5: “Images” (pp.94-125)
- There are many reasons why you might want to add an image to a web page: you might want to include a logo, photograph, illustration, digram. or chart.
### Choosing Images For your Site
- A picture can say a thousand words, and great images help make the difference between an average-looking site and a really engaging one.
  - Images should: be relevant, convey information, convey the right mood. be instantly recognisable, fit the color palette
### Storing Images 
- If you are building a site from scratch, it is good preactice to create a folder for all of the images the site uses.
### Adding Images
- <img>
  - To add image into the page you need to use an <img> element. This is an empty element (which means there is no closing tag.) It must carry the following two attributes.
- src
  - This tells the browser where it can find the image file. This will usually be a relative URL will usually be a relative URL pointing to an image on your own site.
- alt 
  - This provides a text description of the image which decribes the image if you cannot see it.
- Title 
  - You can also use the title attribute with the <img> element to provide additional information about the image. Most browsers will display the content of this attribute in a tooltip when the user hover over the image.
### Height & Width of Images
- You will also often see <img> element use two other attributes that specify its size:
  - Height: This specifies the height of the image in pixels
  - Width: This specifies the width of the image in pixels.
### Where to place images in your code
- 1. Before a Paragraph: The paragraph start on a new line after the image.
- 2. Inside the start of a paragraph: The first row of text aligns with the bottom of the image.
- 3. In the middle of a paragraph: The image is placed between the words of the paragraph that it appears in.
- Block elements always appear on a new line. 
- Inline elements sit within a block level element and do not start on a new line.
### Old Code: Aligning Images Horizontally
- align 
  - The align attribute was commonly used to indicate how the other parts of a page should flow around an image. 
    - Left: This aligns the image to the left. 
    - Right: This align the image to the right.
    - Top: this aligns the first line of the surrounding text with the top of the image.
    - Middle: This aligns the first line of the surrounding text with the middle of the image.
    - Bottom: This aligns the first line of the surrounding text with the bottom of the image.
### Three Rules for creating images
- There are three rules to remember when you are creating images for your website which are summarized below. 
  - Save images in the right format
  - Save images at the right size
  - Measure images in pixels
### Tools to edit & save images
- There are several tools you can use to edit and save images to ensure that they are the right size, format, and resolution
### Image formats
- JPEG
- GIF
### Image Dimensions 
- The images you use on your website should be saved a the same width and height that you want them to appear on the page.
### Cropping Images
- When cropping images it is important not to lose valuable information. It is best to source images that are the correct shape if possible.
  - Portriat
  - LandScape
### Measuring Images and Resolution
- When sizing an image for use on the screen you should always set dimensions of the image in terms of pixels.
### Vector Images
- Vector images differ from bitmap images and are resolution-independent. Vector images are commonly created in programs such as Adobe Illustrator
### Animated Gifs
- Animated Gifs show several frames of an image in sequence and therefore can be used to create simple animations. 
### Transparency
- Creating an image that is partially transparent for the web involves slecting of two formats
  - Tranparent gif
  - PNG
### Summary 
- The <img> element is used to add images to a web page.
- You must always specify an src attribute to indicate the source of an image and an alt attribute to describe the content of an image.
- You should save images at the size you be using them on the web page and in the appropriate format.
- Photographs are best saved as JPEGs; Illustrations or logos that use flat color are better saved as GIFs
## Chapter 11: “Color” (pp.246-263)
- Color can really bring pages to life
### Foreground Color
- The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:
  - RGB Values
    - These express color in terms of how much red, green, and blue are used to make it up
  - Hex Codes
    - These are six-digit codes that represent the amount of red, green, and blue in a color, preceded by a pound or hash # sign
  - Color Names
    - There are 147 predefined color names that are recognized by browsers
### Background Color 
- CSS treats each HTML element as if it appears in a box, and the background-color property sets the color of the background for that box.
### Understanding Color
- Every color on a computer screen is created by mixing amounts of red, gree, and blue . To find the color you want, you can use a color picker.
  - RGB Values: Values for red, green, and blue are expressed as numbers between 0 and 255
  - Hex Codes: Hex Values represent values for red, green ,and blue in hexadecimal code.
  - Color Names: Color are represented by predefined names
  - Hue: Hue is neat to the colloquial idea of color.
  - Saturation: Saturation refers to the amount of in a color.
  - Brightness: Brightness refers too how much black is in a color.
### Contrast
- When picking foreground and background colors, it is imprtant to ensure that there is enough contrast for the text to be legiable
- Low Contrast, High Contrast, Medium Contrast
### CSS3
- Opacity
  - CSS3 introduces the opacity property which allows you to specify the opacity of an element and any of its child elements.
  - The CSS3 rgbs property allows you to specify a color, just like an RGB valuem but adds a fourth value to indicate opacity.
-  Colors
  - CSS3 introduces an entirely new and intuitive way to specify color using hue, saturation, and lightness values.
  - Hue
  - Saturation
  - Lightness
  - alpha: This is expressed as a number between 0 and 1.0
### Summary 
- Color not only brings your site to life, but also helps convey the mood and evokes reactions.
- There are three ways to specify color in CSS: RGB values, Hex codes, and color names.
- Color pickers can help you find the color you want.
- It is omporatnt to ensure that there is enough contrast between any text and the background color.
- CSS3 has introduced an extra value for RGB colors indicate opacity. It is known as RGBA.
- CSS3 also allows you to specify color as HSL values, with an optional opacity value. It is known as HSLA.
## Chapter 12: “Text” (pp.264-299)
- The properties that allow you to control the appearance of text can be split into two groups:
  - Those that directly affect the font and its appearance
  - Those that would have the same effect on text no matter what dont you were using.
### Typeface Terminology 
- Serif: serif fonts have extra details on the ends of the main strokes of the letters.
- Sans-Serif: Sans-Serif font have straight ends to letters, and therefore have a much cleaner design
- Monospace: Every letter in a monospace (for fixed-width) font is the same width.
- the font weight not only adds emphasis but can also affect the amoount of white space on a page.
- Italic font have cursive aspect to some of the lettering. 
### Choosing a typeface for your website
- When choosing a typeface, it is important to understand that a browser will usually only display it if it;s installed on that user's computer
### Techniques that offer a wider choice of typefaces
- There are several ways to use fonts other than those listen on the previous page. However, typefaces are subject to copyright, so the techniques tou can choose from are limited by their repective licenses
- If you design on a Mac, it is important to check what the typefaces look like on a pc becuase pcs can render type less smoothly. But ig you design on a PC, then it should look fine on a mac
  - Font-Family: The user's computer needs the typeface installed. CSS is used to specify the typeface.
  - Font-Face: CSS specifies where a font can be downloaded from if it is not installed on the computer.
  - Service-Based Font-Face: Commercial services give users access to a wider range of fonts using @font-face.
  - Images: You can create a graphic that contains the text as you want it to appear in a different typeface.
  - Sifr: The font is embedded into a Flash movie, and JavaScript replaces specified HTML text with a flash version of it.
  - Cufon: Cufon offers similar functionality to Sifr. It JavaScript to create either an SVG and VML version of the text.
### Type Scales
- you may have noticed programs such as word, photoshop and inDesign offer the same sizes of text. 
### Units of type size
- Pixels: Setting font size in the pixels in the best way to ensure that the type appears at the type appears at the size you intended
- Percentages: The default size of text in a web browser in 16 pixels. Using percentages of this amount, you can create a scale where the default text is 12 pixels, and headings are sized in relation to this.
- EMs: Ems allow you to change the size of text relation to the size of the text in the parent element. Since the default size of text in web browsers is 16 pixels, you can use similar rules to those shown for percentages
### More Font Choice
- @font-face allows you to use a font, even if it is not installed on the computer of the person browsing, by allowing you to specify a path to a copy of the font, which will be downloaded if it is not on the user's machine
### Understanding Font Formats
- Different browsers support different formats for fonts, so you will need to supply the font in several variations to reach all browsers.
### Bold
- font-weight: The font-weight property allows you to create bold text. There are two values that this property commonly takes:
- The font-weight property allows you to create bold text. There are two values that this property commonly takes:
  - normal: This causes text to appear at a normal weight.
  - bold: This causes text to appear bold
### Italic 
- font-style: If you want to create italic text, you can use font-style property. There are three values this property can take:
  - normal: This causes text to appear in a normal style (as opposed to italic or oblique.)
  - italic: This causes text to appear italic
  - oblique: This causes text to appear oblique
### uppercase & lowercase
- text-tranform: The text-transform property is used to change the case of text ggiving it one of the following values:
  - Uppercase: This causes the text to appear uppercase
  - lowercase: This causes the text to appear lowercase
  - Capitalize: This causes the first word to appear capitalized
### Underline & Strike 
- text-decoration: The text-decoration property allows youu to specify the follwing values:
  - none: This removes any decoration already applied to the text.
  - underline: This adds a line underneath the text.
  - overline: This adds a line over the top of the text.
  - line-through: This adds a line through words
  - blink: This animates the text to make it flash on and off (however this is generally frowned upon, as it is considered rather annoying.)
### Leading
- line-height: Leading is a term typographers use for the vertical space between lines of text. In a typeface, the part of the basline is called a descender, while the highest point of a letter is called the ascender. Leading is measured from the bottom of the descender on one line to the next.
### Alignment
- text-align: The text-align property allows you to control the alignment of text. The property can take one of four values:
  - left: this indicates that the text should be left-aligned
  - right: This indicates that text should be right-aligned
  - center: This allows you to center text
  - justify: This indicates that every line a paragraph, except the last line, should be set to take up the full width of the containing box.
### Identing text
- text-indent: The text-indent property allows you to indent the first line of text within an element. The amount you want the line indented by can be specified by can be specified in a bumber of ways but is usually given in pixels or ems
### Drop Shadow
- text-shadow: The text-shadow property has become commonly used despite lacking support in all browser
### First Letter or line
- :first-letter, :first-line
  - You can specify different values for the first letter or first line of text inside an elemnt using
    :first-letter and
    :first-line
  - Technically these are not properties. They are known as psuedo-elements.
### Styling Links 
- :link, :visited
  - Browsers tend to show links in blue with an underline by default, and they will change the color of links that have been visited to help users know which pages they have been to.
  - In CSS, there are two psuedo classes that allow you to set different styles for links that have and have not yet been visited.
    - :link
      - This allows you to set styles for links that have not yet been
    - :visited
      - This allows you to set styles for links that have been clicked on.
### Attribute Selectors 
- You met most popular CSS selectors on page 238. There are also a set attribute selectors that allow you to create rules that apply to elements that have an attribute with a specific value.
  Selector: Existence [] Matches a specific attribute (whatever its value)
  Selector: Equality [=] Matches a specific attribute with a specific value
  Selector: Space [~=] Matches a specific attribute whose value appears in a space seperated list of words
  Selector: Prefix [^=] Matches a specific attribute whose value begins with a specific string 
  Selector: Substring [*=] Matches a specific attribute whose value contains a specific substring 
  Selector: Suffix [$=] Matches a specific attribute whose value ends with a specific string
### Summary
- There are properties to control the chouce of font, size, weight, style, and spacing.
- There is limited choice of fonts that you can assume most people will have installed.
- If you want to use a wider range of typefaces there are several options, but you need to have the right license to use them
- You can control the space between line of text, individual letters, and words. Text can also be aligned to the left, right, center, or justified. It can also be indented.
- You can use psuedo-classes to change the style of an element when a user hovers over or clicks on text, or when they have visited a link.
