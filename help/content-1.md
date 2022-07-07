[Back to project](../README.md)

## First Big Project

View and practice the next introduction to CSS so you can be ready to meet the rest of the HTML tags later on.

CSS is used for defining the styles for web pages. It describes the look and formatting of a document which is written in a markup language. It provides an additional feature to HTML. It is generally used with HTML to change the style of web pages and user interfaces.

**Ways to use CSS to style your HTML pages:**

1. Using the
   <mark>**style** attribute</mark>
   inside any HTML elements (inline)

   - it is used to apply unique style to a single element and you make use of the _style_ attribute using this syntax:

     `<h1 style="color:green">I am green! WOW!</h1>`

     \*<small> This way the header (h1) has now a green color.
     </small>

1. Using the
   <mark>**style** HTML tag</mark>
   inside the `<head>` section (internal)

   - it is used to apply style to a single HTML page (the page you are working on)
   - you make use of the **style** element inside the `<head>` section like in the following syntax:

     ```
     <head>
         <style>
            p {
              color: green;
            }
         </style>
     </head>
     ```

     \*<small>
     This makes all the **p** elements to have the color green inside that page only.
     </small>

1. Using the
   <mark>**style** file that is external</mark>
   and it is linked in a **link** HTML tag (external)

   - create an `css-style.css` file inside the `source-code` folder or the folder that contains the page/pages you are applying the css styles, populate it with minimal css structure and content.
   - link the `css-style.css` file inside the `page-in-work.html` you are applying it using this syntax:

     `<link rel="stylesheet" href="css-style.css">`

     \*<small>
     If you feel confused, take a look again at the **README** file inside `marianzburlea/html/general/link`
     </small>

   - the link `css-style.css` must be added inside the `<head>` section of the page.

**You can use these ways to select the TAG you want to apply the CSS style:**

1. Using the <mark>**type**</mark> attribute:

   - Example: If you want to target the **h2** tag

     ```
     h2 {
      color: blue;
     }
     ```

1. Using the <mark>**class**</mark> attribute

   - Example: If you want to target the html tag that has the class: **test-me**

     ```
     .test-me {
         color: blue;
     }
     ```

1. Using the <mark>**id**</mark> attribute

   - Example: If you want to target the html tag that has the id: **ini-mini**

     ```
     #ini-mini {
         color: blue;
     }
     ```

     \*All ids must have a unique value

**There are quite a few rules that you need to keep in mind:**

- <mark>Cascade</mark>, <mark>Specificity</mark> and <mark>Inheritance</mark>:

  - **Cascade** at a very simple level.

    - This means that the origin, the cascade layer, and the order of CSS rules matter.
    - When two rules from the same cascade layer apply and both have equal specificity, the one that is defined last in the stylesheet is the one that will be used.
    - See the example below:

      ```
      h1 {
         color: red;
      }

      h1 {
         color: blue;
      }
      ```

      \*There are two rules that could be applied for the **h1**. Both the rules are from the same source, have an identical element selector, and therefore, carry the same specificity, but the last one in the source order wins.

  - **Specifity**

        - If multiple style blocks have different selectors that configure the same property with different values and target the same element, specificity decides the property value that gets applied to the element.
        - Specificity is basically a measure of how specific a selector's selection will be:
          - An element selector is less specific: it will select all elements of that type that appear on a page, so it has less weight.
          - A class selector is more specific: it will select only the elements on a page that have a specific class attribute value, so it has more weight.
        - See the example below:

          ```
          .main-heading {
             color: red;
          }

          h1 {
             color: blue;
          }

          <h1 class="main-heading">
          This is my heading.
          </h1>
          ```

          \*In this example we can see that **h1** element has a class as well and it takes the color red from the class. If you have more **h1** elements, they all get the color blue, but only the element that has the class ".main-heading" will get color red.

  - **Inheritance**

    - Inheritance is the mechanism by which certain properties are passed on from a parent element down to its children, in the same fashion as genetics: if parents have green eyes, their children will probably also have green eyes.
    - CSS has an inheritance mechanism because otherwise CSS rules would be redundant.
    - Without inheritance, it would be necessary to specify styles like font family, font size, and text color individually — for every single element type. The code would become bloated and repetitive.
    - Using inheritance, you can specify the font properties for the html or body elements and the styles will be inherited by all other elements.
    - See Example:

    ```
      body{
         color: pink
      }

      span {
         color: red
      }

      .change-me-here{
         color: green
      }
    ```

  ```
     <body>
         <p>
         This is a main example for the Inheritance.
         </p>

         <p>
         This is another example of how to change the
         <span>color of the child</span>,
         but with the use of another tag.
         </p>

         <p class="change-me-here">
         This is yet another example of a changing in color for the child by using the class of the tag.
         </p>
     </body>
  ```

    <!-- - When you reach a moment of good understanding, after enough discover, trial and error with experimental css files, create an `README.md` file to make use of all the recent discoveries and summarise your experience.

### Mimimum tags knowledge to build a website

#### Top tags used to style your html pages for your web site

##### Must Know CSS properties

1. the `color` property `````````` - color, background & font section - @iulia-zburlea
1. the `background-color` property - section: color, background & font - @MariaTeo
1. the `background-image` property - section: color, background & font - @MariaTeo
1. the `display` property `````````- section: display-min-max-width-height - @MariaTeo
1. the `height` property ``````````- section: color, background & font - @MariaTeo
1. the `width` property ```````````- section: color, background & font - @MariaTeo
1. the `min-width` property ```````- section: display-min-max-width-height - @MariaTeo
1. the `min-height` property ``````- section: display-min-max-width-height - @MariaTeo
1. the `max-height` property ``````- section: display-min-max-width-height - @MariaTeo
1. the `max-width` property ```````- section: display-min-max-width-height - @MariaTeo
1. the `margin` property ``````````- section: margin & padding section - @iulia-zburlea
1. the `padding` property `````````- section: margin & padding section - @iulia-zburlea
1. the `border` property ``````````- section: border - @iulia-zburlea
1. the `border-color` property ````- section: border - @iulia-zburlea
1. the `border-width` property ````- section: border - @iulia-zburlea
1. the `border-style` property ````- section: border - @iulia-zburlea
1. the `border-radius` property ```- section: border - @iulia-zburlea
1. the `font` property ````````````- section: color, background & font - @iulia-zburlea
1. the `font-family` property `````- section: color, background & font - @iulia-zburlea
1. the `font-style` property ``````- section: color, background & font - @iulia-zburlea
1. the `font-weight` property `````- section: color, background & font - @iulia-zburlea
1. the `font-size` property ```````- section: color, background & font - @iulia-zburlea
1. the `position` property ````````- section: position & z-index - @MariaTeo
1. the `z-index` property `````````- section: position & z-index - @MariaTeo

   ##### CSS Selectors

1. the `:active` property ````- section: general/css-selectors - @MariaTeo
1. the `:hover` property `````- section: general/css-selectors - @MariaTeo
1. the `:visited` property ```- section: general/css-selectors - @MariaTeo
1. the `:link` property ``````- section: general/css-selectors - @MariaTeo

1. the `:enabled` property ````- section: general/css-selectors - @iulia-zburlea
1. the `:disabled` property ```- section: general/css-selectors - @iulia-zburlea
1. the `:checked` property ````- section: general/css-selectors - @iulia-zburlea

1. the `::before` property ````- section: general/css-selectors - @MariaTeo
1. the `::after` property `````- section: general/css-selectors - @MariaTeo

1. the `:first-child` property ````````- section: general/css-selectors - @MariaTeo
1. the `:only-child` property `````````- section: general/css-selectors - @MariaTeo
1. the `:nth-child()` property ````````- section: general/css-selectors - @MariaTeo
1. the `:last-child` property `````````- section: general/css-selectors - @MariaTeo
1. the `:nth-last-child()` property ```- section: general/css-selectors - @MariaTeo

1. the `:first-of-type` property `````` - section: general/css-selectors - @iulia-zburlea
1. the `:only-of-type` property ``````` - section: general/css-selectors - @iulia-zburlea
1. the `:nth-of-type` property ```````` - section: general/css-selectors - @iulia-zburlea
1. the `:nth-last-of-type` property ``` - section: general/css-selectors - @iulia-zburlea
1. the `:last-of-type` property ``````` - section: general/css-selectors - @iulia-zburlea

1. the `:first-letter` property ``````` - section: general/css-selectors - @iulia-zburlea
1. the `:first-line` property ````````` - section: general/css-selectors - @iulia-zburlea

1. the `:root` property - section: general/css-selectors - @mariateo
1. the `:selection` property - section: general/css-selectors - @mariateo
1. the `:focus` property - section: general/css-selectors - @mariateo
1. the `:empty` property - section: general/css-selectors - @mariateo
1. the `:target` property - section: general/css-selectors - @mariateo
1. the `:lang()` property - section: general/css-selectors - @mariateo
1. the `:not()` property - section: general/css-selectors - @mariateo

   ##### Backgound Properties

1. the `backgroung` property ```````- section: general/background - @mariateo
1. the `background-attachment` property ```````- section: general/background - @mariateo
1. the `background-color` property - See intro/color-font-and-background
1. the `background-image`tproperty - See intro/color-font-and-background
1. the `background-position` property ```````- section: general/background - @mariateo
1. the `background-repeat` property ```````- section: general/background - @mariateo
1. the `background-clip` property ```````- section: general/background - @mariateo
1. the `background-origin` property ```````- section: general/background - @mariateo
1. the `background-size` property ```````- section: general/background - @mariateo

   ##### Color Properties

1. the `color-profile` property ``````````- section: general/color-and-font - @iulia-zburlea
1. the `opacity` property ````````````````- section: general/color-and-font - @iulia-zburlea
1. the `rendering-intent` property ```````- section: general/color-and-font - @iulia-zburlea

   ##### Font Properties

1. the `font` property ``````````- See Must Know Tags
1. the `font-family` property ```- See Must Know Tags
1. the `font-style` property ```- See Must Know Tags
1. the `font-variant` property ```- section: general/color-and-font - @mariateo
1. the `@font-face` property `````- section: general/color-and-font - @mariateo
1. the `font-size-adjust` property - section: general/color-and-font - @mariateo
1. the `font-size` property ``````- See Must Know Tags ```````- section: general/color-and-font - @mariateo
1. the `font-stretch` property ```- section: general/color-and-font - @mariateo

   ##### Text Properties

1. the `color` property - See Must Know Tags - section: general/text - @mariateo

1. the `direction` property ````````````` - section: general/text - @mariateo
1. the `line-height` property ``````````` - section: general/text - @mariateo
1. the `text-decoration` property ``````` - section: general/text - @mariateo
1. the `text-indent` property ``````````` - section: general/text - @mariateo
1. the `text-transform` property ```````` - section: general/text - @mariateo

1. the `letter-spacing` property ```````` - section: general/text - @mariateo
1. the `word-spacing` property `````````` - section: general/text - @mariateo

1. the `text-align` property ```````````` - section: general/text - @mariateo
1. the `vertical-align` property ```````` - section: general/text - @mariateo
1. the `text-align-last` property ``````` - section: general/text - @mariateo

1. the `hanging-punctuation` property ``` - section: general/text - @mariateo
1. the `punctuation-trim` property `````` - section: general/text - @mariateo

1. the `text-justify` property `````````` - section: general/text - @mariateo
1. the `text-outline` property `````````` - section: general/text - @mariateo
1. the `text-overflow` property ````````` - section: general/text - @mariateo
1. the `text-shadow` property ``````````` - section: general/text - @mariateo

1. the `text-wrap` property ````````````` - section: general/text - @mariateo
1. the `word-break` property ```````````` - section: general/text - @mariateo
1. the `word-wrap` property ````````````` - section: general/text - @mariateo

1. the `unicode-bidi` property `````````` - section: general/text - @mariateo
1. the `white-space` property ``````````` - section: general/text - @mariateo

   ##### Border and Outline Properties

1. the `border` property - See Must Know Tags
1. the `border-top` property `````````````` - section: general/border-and-outline - @iulia-zburlea
1. the `border-right` property ```````````` - section: general/border-and-outline - @iulia-zburlea
1. the `border-bottom` property ``````````` - section: general/border-and-outline - @iulia-zburlea
1. the `border-left` property ````````````` - section: general/border-and-outline - @iulia-zburlea

1. the `border-color` property - See Must Know Tags
1. the `border-top-color` property ```````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-right-color` property `````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-bottom-color` property ````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-left-color` property ``````` - section: general/border-and-outline - @iulia-zburlea - in progress

1. the `border-style` property - See Must Know Tags
1. the `border-top-style` property ```````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-right-style` property `````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-bottom-style` property ````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-left-style` property ``````` - section: general/border-and-outline - @iulia-zburlea - in progress

1. the `border-width` property - See Must Know Tags
1. the `border-top-width` property ```````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-right-width` property `````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-bottom-width` property ````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-left-width` property ``````` - section: general/border-and-outline - @iulia-zburlea - in progress

1. the `outline` property ```` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `outline-color` property ``````````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `outline-style` property ``````````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `outline-width` property ``````````` - section: general/border-and-outline - @iulia-zburlea - in progress

1. the `border-image` property ``` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-image-repeat` property ````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-image-outset` property ````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-image-slice` property `````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-image-source` property ````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-image-width` property `````` - section: general/border-and-outline - @iulia-zburlea - in progress

1. the `border-radius` property - See Must Know Tags
1. the `border-top-right-radius` property `` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-top-left-radius` property ``` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-bottom-right-radius` property - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `border-bottom-left-radius` property - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `box-decoration-break` property ````` - section: general/border-and-outline - @iulia-zburlea - in progress
1. the `box-shadow/box-shadow` property ```` - section: general/border-and-outline - @iulia-zburlea - in progress

   ##### Box Properties

1. the `overflow-x` property ```````` - section: general/box - @mariateo
1. the `overflow-y` property ```````` - section: general/box - @mariateo
1. the `overflow-style` property ```````` - section: general/box - @mariateo
1. the `rotation` property ```````` - section: general/box - @mariateo
1. the `rotation-point` property ```````` - section: general/box - @mariateo

   ##### Dimension Properties

1. the `height` property - See Must Know Tags ````- @MariaTeo
1. the `width` property - See Must Know Tags `````- @MariaTeo

1. the `min-heigth` property - See intro/display-min-max-width-height ````- @MariaTeo
1. the `max-heigth` property - See intro/display-min-max-width-height ````- @MariaTeo
1. the `min-width` property - See intro/display-min-max-width-height ````- @MariaTeo
1. the `max-width` property - See intro/display-min-max-width-height ````- @MariaTeo

   ##### Margin Properties

1. the `margin` property ```````` - section: intro/margin-and-padding - @mariateo
1. the `margin-bottom` property ```````` - section: general/margin - @mariateo
1. the `margin-top` property ```````` - section: general/margin - @mariateo
1. the `margin-left` property ```````` - section: general/margin - @mariateo
1. the `margin-right` property ```````` - section: general/margin - @mariateo

   ##### Padding Properties

1. the `padding` property ```````` - section: intro/margin-and-padding - @mariateo
1. the `padding-bottom` property ```````` - section: general/margin - @mariateo
1. the `padding-top` property ```````` - section: general/margin - @mariateo
1. the `padding-left` property ```````` - section: general/margin - @mariateo
1. the `padding-right` property ```````` - section: general/margin - @mariateo

   ##### Positioning Properties

1. the `position` property ```````` - section: intro/position-z-index - @mariateo

1. the `bottom` property ```````` - section: intro/position-z-index - @mariateo
1. the `top` property ```````` - section: intro/position-z-index - @mariateo
1. the `left` property ```````` - section: intro/position-z-index - @mariateo
1. the `right` property ```````` - section: intro/position-z-index - @mariateo

1. the `display` property ```````` - section: intro/display-min-max-width-height - @mariateo
1. the `visibility` property
1. the `overflow` property

1. the `float` property
1. the `clear` property

1. the `clip` property
1. the `clip-path` property

1. the `cursor` property
1. the `z-index` property ```````` - section: intro/position-z-index - @mariateo

   ##### Grid Properties

1. the `grid-columns` property
1. the `grid-rows` property

   ##### Table Properties

1. the `border-spacing` property
1. the `border-collapse` property
1. the `empty-cells` property

1. the `table-layout` property
1. the `caption-side` property

   ##### Multi-column Properties

1. the `columns` property
1. the `column-count` property
1. the `column-fill` property
1. the `column-width` property
1. the `column-span` propertys
1. the `column-gap` property

1. the `column-rule` property
1. the `column-rule-color` property
1. the `column-rule-style` property
1. the `column-rule-width` property

   ##### List Properties

1. the `list-style` property
1. the `list-style-image` property
1. the `list-style-position` property
1. the `list-style-type` property

##### Hyperlink Properties

1. the `target` property
1. the `target-name` property
1. the `target-new` property
1. the `target-position` property

   ##### Content and Paged Media Properties

1. the `bookmark-label` property
1. the `bookmark-level` property
1. the `bookmark-target` property

1. the `hyphenate-after` property
1. the `hyphenate-before` property
1. the `hyphenate-character` property
1. the `hyphenate-lines` property
1. the `hyphenate-resources` property

1. the `float-offset` property
1. the `hyphens` property
1. the `image-resolution` property
1. the `marks` property
1. the `string-set` property

   ##### Generated Content Properties

1. the `content` property
1. the `counter-increment` property
1. the `counter-reset` property
1. the `quotes` property
1. the `crop` property
1. the `move-to` property
1. the `page-policy` property

   ##### Marquee Properties

1. the `marque-direction` property
1. the `marque-play-count` property
1. the `marque-speed` property
1. the `marque-style` property

   ##### Paged Media Properties

1. the `page` property

1. the `fit` property
1. the `size` property

1. the `fit-position` property
1. the `image-orientation` property

   ##### Print Properties

1. the `orphans` property
1. the `widows` property

1. the `page-break-before` property
1. the `page-break-inside` property
1. the `page-breakafter` property

   ##### Ruby Properties

1. the `ruby-align` property
1. the `ruby-position` property
1. the `ruby-overhang` property

   ##### Animation Properties

1. the `@keyframes` property
1. the `animation` property
1. the `animation-name` property
1. the `animation-duration` property
1. the `animation-timing-function` property
1. the `animation-delay` property
1. the `animation-iteration-count` property
1. the `animation-direction` property
1. the `animation-play-state` property

   ##### 2D/3D Transform Properties

1. the `tranform` property
1. the `tranform-origin` property
1. the `tranform-style` property
1. the `perspective` property
1. the `perspective-origin` property
1. the `backface-visibility` property

   ##### Transition Properties

1. the `trasition` property
1. the `transition-property` property
1. the `transition-duration` property
1. the `transition-timing-function` property
1. the `transition-delay` property

   ##### User-interface Properties

1. the `appearance` property
1. the `box-sizing` property
1. the `icon` property
1. the `outline-offset` property
1. the `resize` property

1. the `nav-index` property
1. the `nav-up` property
1. the `nav-right` property
1. the `nav-down` property
1. the `nav-left` property

   ##### Other Properties

1. the `align-items` property
1. the `calc` property
1. the `url` property
1. the `hsl` property
1. the `hsla` property
1. the `justify-content` property
1. the `@media` property
1. the `opacity` property

1. the `flex-direction` property
1. the `flex-flow` property
1. the `flex-grow` property
1. the `flex-shrink` property
1. the `flex-wrap` property

1. the `rotateX` property
1. the `rotateY` property
1. the `rotateZ` property

1. the `scaleX` property
1. the `scaleY` property
1. the `scaleZ` property

1. the `translate` property
1. the `translateX` property
1. the `translateY` property
1. the `translateZ` property
1. the `translate3d` property

!--
Reference link no. 1:
https://lucidar.me/en/web-dev-class/lesson-2-09-most-used-css-properties/

Reference link no. 2:
https://developer.mozilla.org/en-US/docs/Learn/CSS

Reference link no. 3:
https://webplatform.github.io/docs/tutorials/inheritance_and_cascade/

Reference link no. 4:
https://www.script-tutorials.com/css-reference/#marquee

-->

@iulia-zburlea
@mariateo
