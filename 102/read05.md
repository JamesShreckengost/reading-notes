# Read 05: Design web pages with ccs


## Duckett: HTML & CSS, Chapter 10: Introducing CSS
    * Understanding CSS: Thinking inside the box
        - The key to understnading CSS is to imagine there is an invisible box aorund every HTML element
        - CSS allows you to creat rules that control the way that each individual box is presented
        - Example styles: boxes, text, specific
    * CSS associates style rules with html elements
        - CSS works by associating rules with HTML elements. A CSS rule contians tow parts: a selector and a declaration
        - Selectors indicate which element the rule applies to.
        - Declarations indicate how the elemtns reffered to in the selector should be styled
    * CSS rules usually appear in a seperate document, although they may appear within a HTML image.
## Duckett: HTML & CSS, Chapter 11: Color
    * ForeGround Color
        - RGB values: These express colors in terms of how much red, green, and blue are used to make it up. for example: rgb(100,100,100)
        - Hex codes: six-digit codes that represent the amount of red, green, and blue in a color, preceded by a pound of hash sign. for example:ee3e80
        - Color names: there are 147 predefined color names that are recognized by browers. for example: DarkCyan
    * Background color
        - Css treats each Html element as if it appears in a box, and the background-color property sets the color of the background for that box
        - Ypi xan specify your choice of background color in the same three ways you can specify foreground colors.
        - Most default browsers windows have a whote background, but browser users can set a background color for thir window
    * Understanding color 
        - RGB values: Values for red, green, and blue are expressed as numbers between 0 and 225
        - Hue: Hue is near to the colloquial ideal of color. Technically speaking however, a color can also have saturation and brightness as well as hue
        - Hex Codes: Hex values represent values for red, green, and blue in hexadecimal code
        - Saturation: Saturation refers to the amoubnt of gray in a color. At maximum saturation, there would be no gray in the color. At minimum saturation, the color would be mostly gray
        - Color names: Colors are represented by predefined names. However, they are very limited in number.
        - Brightness: Brightness refers to how much black is in a color. At maximum brightness, there would be no black in the color. At minimum brightness, the color would be very dark
    
    * Contrast
        - Low Contrst: text is harder tto read when there is low contrast between backgorund and foreground colors
        - High contrast: text is easier to read when there is higher contrast between foreground and background
        - Medium contrast: for long spans of text, reducing the contrast a little bit improves readability
        - If text is reversed out (a light color on a dark background), you can increase the height between the lines and the weight of the font to make it easier to read
    * CSS3: Hsl colors
        - Hue: often represented as a color circle where the angle represents the color, although it may also be shown as a slider with values from 0 to 360
        - Saturation: represented as a percentage. 100 to 0 %.
        - Lightness: the amount of white or black in a color. lightness is represented as a percentage
        
        Sumamary:
         - It is important to ensure that there is enough contrast between any text and the background color.
        - CSS3 has introduced an extra value for RGB colors to indicate opacity. It is known as RGBA
        - CSS3 also allows you to specify colors as HSL values, with an optional opacity value. It is known as HSLA
