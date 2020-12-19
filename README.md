# Web_Development_Training

## DAY 1:
### Basic HTML & HTML 5
###### Basic Structure:
```
<!DOCTYPE html> <!-- declare html (HTML5) -->
<html>
  <head>
    <!-- metadata elements (link, meta, title, style) -->
  </head>
  <body>
    <!-- page elements -->
  </body>
</html>
```

###### Basics:
- Comment:
  - `<!--  -->`
###### Body:
- **Organization:**
  - main
    - ```
      <main>
        ...helps search engines/other developers find the main content of your page. 
      </main>
      ```
  - header
  - footer
  - div:
    - general purpose container for other elements
  - nav
  - video
  - article
  - section
- **Page Elements:**
  - Headings: 
    - `<h1>  </h1>`
    - `<h2>  </h2>`
    - `<h3>  </h3>`
    - `<h4>  </h4>`
    - `<h5>  </h5>`
    - `<h6>  </h6>`
  - Paragraph:
    - `<p>  </p>`
    - Note: lorem ipsum is usually used as placeholder text
  - Images:
    - Self-closing
    - `<img src="/path" alt="displayed if img fails or to improve accessibility">`
    - If image is decorational, set `alt` empty
  - Links (Anchor):
    - NOTE: `target="_blank" opens the link in a new page
    - NOTE: Dead links to be replaced later (`href = "#"`) 
    - External Links:
      - `<a href = "link"> Display Text </a>`
    - Internal Links:
      - Given an element an id attribute set to "name-of-id"
        - EX: `<h2 id = "name-of-id"> </h2>`
      - `<a href = "#name-of-id"> Display Text </a>`
    - Make elements a link by nesting:
      - EX: Image is now a link
        ```
        <a href = "#"> 
          <img src= ...>
        </a>
        ```
  - Lists:
    - Bullet Unordered List:
      ```
      <ul>
        <li> item </li>
        <li> item </li>
      </ul>
      ```
    - Ordered List:
      ```
      <ol>
        <li> Item 0 </li>
        <li> Item 1 </li>
      </ol>
      ```
  - Web Form:
    ```
     <form action = "/url-where-you-want-to-submit-form-data">
      <imput type ....> 
      ...
      <button type = "submit" > This button submits the form </button>
     </form>
    ```
    - Input Types:
      - Self-closing
      - NOTE: Make a input required with the attribute required 
        `<input type = "text" required>`
      - TEXT: 
        - `<input type = "text" placeholder = "display temp">`
      - RADIO/CHECKBOX:
        - Can be nested in a `<label>` element
        - Best practice to put a `for` attribute in the label whose value matches the id set to the input
        - Reports their values from the `value` attribute 
          - `on is the default if there is no value`
        - `checked` attribute (checked by default)
        - EX: 
            ```
            <label for = "indoor">
              <input type-"radio" id = "indoor" name = "indoor-outdoor" value = "indoor" checked>
            </label>
            ```

### Basic CSS
###### STYLE BLOCKS:
- Read from top to bottom
- **Create a CSS Selector:**
  - EX: All `<h2>` elements will be red
    ```
    <style>
      h2{
        color: red;
      }
    </style>
    ```
- **CSS Class Declarations**
  - NOTE: Class names start with a .
  - reusable styles that can be used/added to HTML elements
  - Apply with the class attribute (`class = "blue-text`)
    - Apply multiple classes with a space in between class names (`class = "class1 class2 class3 ..."`)
  - EX: 
    ```
    <style>
      .blue-text{
        color: blue;
      }
    </style>
    ```
- **CSS ID Declarations**
  - NOTE: ID names start with the #
  - Best Practice: Should be unique 
  - Benefits:
    - Style a single element (shouldn't be reused)
    - Use them to select/modify specific elements with JS
  - `<id = "name-of-id">`
- **CSS VARIABLES**
  - use the var anywhere else in the CSS
  - `--var-name: value`
  - Use:
    - ```
      background: var(--penguin-skin);
                : var(--penguin-skin, black); (fallback; not for browser compatibility)
      ```
  - **Browser Fallback:**
    - Add a standard declaration
      - ```
        background: red;
        background: var( --red-color);
        ```
  - **Global Variables:**
    - `:root(pseudo-class selector that matches the root element of the document)`
      - creating variables in root make them available globally.
        - all child elements that use the variable, use it
      - can overwrite these values by declaring them again within a specific element
    - EX: ```
          @media (max-width: 350px):
            :root{
              redefinitions;
            }
          ```
    
- **INHERITANCE:**
  - BODY:
    - Every html page has a body
    - All elements in body will inherit that style of body
    - Class declarations overrides a body
    - `body{ ... }`
- **OVERRIDE DECLARATIONS:**
  - id > class
  - class > body declaration
  - css read from top to bottom
  - inline > style block
  - NOTE: use the `!important` to put priority
    - `<color: red !important>`
    
###### STYLE:
- Best practice to end style declarations with a `;`
- **TEXT:**
  - Color:
    - color property controls an elements text color
    - `color: blue; `
  - Font:
    - `font-size:`
    - `font-family`
      - standard fonts
        - sans-serif 
        - serif
        - monospace
      - imported fonts (ex. Google Fonts):
        - import at the top: '<link href="link to front" rel = "stylesheet" type = "text/css" >'
        - 'font-family: imported-font, fallback-font;'
          - imported-font has ""
- **BACKGROUND COLOR:** 
  - `background-color : green;`
- **BORDER:**
  - ```
    border-color: red;
    border-width: 5px;
    border-style: solid;
    border-radius: 10px; <!-- rounds the corners of the border -->
                 : 50%;     
    ```
- **COLOR:**
- **SIZE:**
  - `width` (px)
    - controls an elements width
    - `width: 100px;`
- **SPACE CONTROL:**
  - padding
    - controls the amount of space between the elements and its border
    - ```
      padding: 10px
      padding-top: 10px
      padding-right: 10px
      padding-bottom: 10px
      padding-left: 10px
      padding: T R B L; (Clockwise)
      ```
  - margin
    - controls the amount of space between an elements border and surrounding elements
    - if negative, the element will get larger
    - ```
      margin: 
      margin-top:
      margin-right:
      margin-bottom:
      margin-left:
      margin: T R B L; (Clockwise)
      ```
---
