# Introdution
Cascading style sheets (CSS) is used to describe / style the presentation of a HTML document.

## Types of style sheet
There are three types of style sheet assiociated with a HTML document
- User agent (Browser style sheet)
- User style sheet
- Author style sheet

### User agent style sheets
- A user agent is **any software that retrieves and presents Web content for end users or is implemented using Web technologies that help in retrieving, rendering and interacting with Web
content.** In most cases, the **user agent will typically be the web browser.**
- The browser will apply style sheets to all web documents (Eg: black text, blue links, purple links for visited sites etc)
- However, once **we apply a style sheet to a document**, it will **override the browser's style sheet as an author style sheet will always override a browser's stlye sheet.**

### User style sheets
- User style sheets are set by the user within their own web browser.
- These style sheets will override the browser's default stylesheets for that user only.

### Author style sheets
- Author style sheets are **style sheets which are applied by us, authors who develops the website.**
- Everything we do to change the visual of the document, from choosing fonts, colours and laying out pages in CSS is done using author style sheets.
- Author style sheets can be **applied inside an HTML document** or by **linking to an external file.**

### Style sheet precedence
The following CSS declarations are applied in this order (from lowest to highest priority):
- user agent stylle sheet (web browser style sheet)
- user style sheet normal
- author style sheet normal
- author style sheet important
- user style sheet important

Note: Without the usage of !importnant declaration, the order goes like this (author to user to browser style)

## CSS selectors and declarations
CSS is **composed of style rules that describe the styling to be applied to the HTML document.** Each rule consists of two parts which are:
- **selector** = HTML element name, class name or an id name
- **declaration** = CSS styling property and the value which is assigned to the property.

**Example:**

![image](https://github.com/Fong20/Learning-repository/assets/150316121/3fbaac24-ba6e-468d-979c-f09c11e4ead9)

## Inserting style sheets
There are generally three ways of inserting style sheets
- Embedded
- Inline
- External

  ### Embedded
  - it is found in the head section of the HTML document
  - it applies to the entire webpage
 
  ### Inline
  - It is found in the body section of the HTML document
  - It only applies to a specific element
  - This can be done by either using class selector or id selector
 
  ### External
  - All the **styling codes are stored in a separate file wth .css file extension.**
  - It can be **applied to the HTML file by using the HTML link element in the head section of the HTML file.** The styling applies to all webpages as long as it is linked to the css file.
 
    ![image](https://github.com/Fong20/Learning-repository/assets/150316121/d08332c1-abf8-4eaa-a530-b68798b69d88)
