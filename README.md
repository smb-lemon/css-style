# CSS STYLESHEET

**CSS means Cascading Style Sheet**<br>

*What is CSS?*<br>
**It is a language which is used to style or design a document**

*Example*<br>
```css
h1 {
    color : green;
}
```
Here, <br> 
`h1` is a Selector,<br>
`color` is a Property,<br>
`green` is a value

*How to include styles?*<br>
- **Inline Style :**<br>
**Writing styles directly inline in each element of the programme.**<br>
```css 
<h1 style = "color : yellow"> HTML Page <h1>
```
***Disadvantage* : When working with the large project, inline style is not feasible solution** 

- **Style Tag `<style>` :** <br>
**Style is added using the `<style>` tag in the same document**t
```html
<head>
    <style>
        h2 {
            background-color : white;
        }
    </style>
</head>
```
- **External StyleSheet :**<br>
**Writing CSS elements in a separate file or document and link this with HTML file**<br>
```html
## Linking HTML with CSS file
<head>
    <link rel="stylesheet", href="style.css"> ##href = css file path
</head>
```
## Color Property

**Color property is used to set the color of foreground**<br>
*Examples*<br>
```css
color: purple;
color: #00a400;
color: rgb(214, 122, 127);
color: hsl(30deg 82% 43%);
color: hsla(237deg 74% 33% / 61%);
color: hwb(152deg 0% 58% / 70%);
```
***Background Color Property***<br>
**Background Color Property is used to set the color of the background**<br>
*Examples*<br>
```css
background-color: purple;
background-color: #00a400;
background-color: rgb(251, 180, 219);
background-color: hsl(30deg 82% 43%);
background-color: hsla(237deg 74% 33% / 61%);
background-color: hwb(152deg 0% 58% / 70%);
```
**RGB TO HEX**<br>
`color  : #ffffff ` <br>
##1st ff is Red(R),<br>
##2nd ff is Green(G), <br>
##3rd ff is Blue(B)
- Convert the red, green and blue color values from decimal to hex.
- Concatenate the 3 hex values of the red, green and blue togather: RRGGBB.

## Text Property

### Text Align<br>
Text align is relative to the parent.It changes with the parent element.<br>
*Example:*<br>
```css
h1 {
    text-align : center;
}
```
<p style = "text-align : center; font-weight : bold">Text Align to Center</p>
**In CSS3 , there are two new value in added. `text-align : start, text-align : end`**<br>
**For horizontal allignment and extra spaces,`text-align : justify` value is used**<br>

### Font Weight<br>
**font-weight is used to resize the font into bold or other relevent formate.It usually evaluate from 100-900**<br>
*Example:*<br>
```css
h1 {
    font-weight: bold; //700
}
```
<p style = "font-weight : bold">Font Weight is Bold</p>

### Text Decoration<br>
**Text decoration is basically decorating text in various ways like underline , overline in text**<br>
*Example:*<br>
```css
h1 {
    text-decoration: line-through;
}
```
<p style = "text-decoration: orange line-through">This text is Line Through</p>

**When the text decoration value is none, any existing underline or overline will be removed**<br>
### Line Height <br>
**Line height is basically the height between two lines**<br>
*Example:*<br>
```css
h1 {
    line-height: 2;
}
```
### Letter Spacing <br>
**Letter spacing is used to space between letters horizontally**<br>
*Example:*<br>
```css
h1 {
    letter-spacing: 10px;
}
```
### Font Size units in CSS<br>
| Absoulute  | Relative   |
|------------|------------|
| *px        | *%         |
| pt         | *em         | 
| pc         | *rem        |
| cm         | ch         |
| mm         | vh         |
| in         | vw + many more   | 
| 

` 1 inch = 96 px`<br>
### Percentage %<br>
It is often defined as the size of a relative to an element's parent object <br>
*Example:*<br>
```css
h1 {
    width: 50%;
}
```
### em <br>
font size of parent, in the case of typographical property like font-size or other property like width, margin <br>
*Example:*<br>
```css
#outerDiv {
    font-size: 20px;
}

#innerDiv {
    font-size: 2em;
    padding: 1em;

/* font-size will be 40px as 2em & padding will be 40px as the font size is 40px */
}
```
**Drawbacks of em :** Snowball effect in nested elements <br>
## rem(Root em) <br>
Font size of the root element <br>
*Example:*<br>
```css
section {
    font-size: 10px;
}

div {
    font-size: 2rem; 
}

/* for multiple nested divs, rem will be the root(Section) */
```
### Font Family <br>
**Font family is used to specify one or more family font**<br>
*Example:*<br>
```css
h1 {
    font-family: fantasy;
}
```
<p style = "font-family : fantasy">This text is fantasy's Default font</p>

## Selectors <br>
**On Importance Basis : *`Id > Class > Element`***<br>
```css
<div class="greetDiv">
        <p class="greetPara">
            Hello world
        </p>
    </div>
```
```css
div.greetDiv .greetPara{
    color: aliceblue;
}

.greetDiv p.greetPara{
    color: black;
}

.greetDiv .greetPara{
    color: brown;
}
```
### Specificity Calculation in CSS<br>
Inline| ID  | Class | Element | Code                        |Total
|-----|-----|-------|---------|-----------------------------|----|
|| 0   | 2     | 1       | div.greetDiv .greetPara     |0 2 1
|| 0   | 2     | 1       | .greetDiv p.greetPara       |0 2 1
|| 0   | 2     | 0       | .greetDiv .greetPara        |0 2 0
|Inline|ID    |Class, attributes & Pseudo class|Element & Sudo-Element|----|----
|

### !important<br>
**To show most specific things in document**<br>
*Example:*<br>
```css
h2 {
    property: value; !important
}
```
**If the Value is same ,it will follow cascading rule and the last value will be the final value**<br>

**In any html fine, to select any set or group of files or individual element so that we can apply style on them is called Selectors**<br>
### Universal Selector<br>
To select everything in a document<br>
*Example:*<br>
```css
* {
    property: value;
}

/* (*) is the Universal Selector */
```
## Element Selector<br>
It is used to select all the elements of the same type<br>
*Example:*<br>
```css
h2 {
    property: value;
}

/* h2 is the Element Selector */
```
## ID Selector<br>
Id selector is used based on the value of element's id attribute<br>
*Example:*<br>
```css
#myId {
    property: value;
}

/* myId is the ID Selector */
```
## Class Selector<br>
Class selector is used based on the element's class attribute<br>
*Example:*<br>
```css
.myClass {
    property: value;
}

/* myClass is the Class Selector */
```
## Descendant Selector<br>
Descendant selector selects elements of parent element<br>
*Example:*<br>
```css
div p {
    property: value;
}

/* p is the Descendant Selector */
```
## Adjacent Sibling Combinator <br>
**Combinator is basically adding multiple selector together.As the descendant selector works on parent element, this sibling combinator works as sibling element, ex : h3 comes immediately after p tag.Basically they are on the same level**<br>
*Example:*<br>
```css
p+h3 {
    property: value;
}

/* + is the sibling combinator */
```
## Child Combinator <br>
**Child  combinator works as parent and children relation.ex : selects all button which are direct children of span.Child combintor can only go one level up(disadvantage)**<br>
*Example:*<br>
```css
span > button {
    property: value;
}

/* > is the child combinator */
```
## Attribute Selector<br>
**Attribute selector selects elements based on the presence or value of a given attribute**<br>
*Example:*<br>
```css
input[attriute=""] {
    property: value;
}

/* = is the Attribute Selector */
```
## Pseudo Class<br>
A keyword added to the selector that specifies a special state of the selected elements<br>
- **hover**
    - example : <br> 
    ```css
    button:hover{
    background-color: black;
    }
    ```
- **active**
    - example : <br> 
    ```css
    p:active{
    font-weight: bold;
    }
    ```
- **checked**
     - example : <br> 
    ```css
    input[type="radio"]:checked + label{
    color: red;
    font-weight: bold;
    }
    ```
- **nth-of-type**
     - example : <br> 
    ```css
   div:nth-of-type(3){
    background-color: cornflowerblue;
    }
    ```
- **default**
    - example : <br> 
    ```css
   input:default {
  box-shadow: 0 0 2px 1px coral;
    }

    input:default + label {
    color: coral;
    }

    //checked required
    ```
- **disabled**
    - example : <br> 
    ```css
   :disabled {
    background-color: grey;
   }

    //disabled required
    ```
## Pseudo Element<br>
A keyword added to the selector which is used to modify specific part of the element <br>
- **first-letter**
    - example : <br> 
    ```css
   h1::first-letter {
    color: grey;
   }
    ```
- **first-line**
    - example : <br> 
    ```css
   h1::first-line {
    color: blue;
   }
    ```
- **selection**
    - example : <br> 
    ```css
   p::selection {
    background-color: blue;
   }
    ```
## Inheritance<br>
When we need apply some style to div as parent element, it will apply to all other element in that div(**`button,input`** etc are different).To use the same value in these elements we can use `inherit` value.**`height,width,border`(non-inherit**)<br>

 Example : <br> 
```css
   button {
    background-color: inherit;
   }
```
## Box Model <br>
- **Height**
    - Height refers as the area of content height.<br>

    Example : <br> 
    ```css
   div {
    height: 100px;
   }
    ```
- **Width**<br>
    - Width refers as the area of content width.<br>

    Example : <br> 
    ```css
   div {
    width: 300px;
   }
    ```
- **Border**<br>
    - Use to set element's border<br>
        - border-width
        - border-style
        - border-color<br>

     Example : <br> 
    ```css
   div {
    border-width: 5px;
    border-style: solid;
    border-color: blue;
   }

   /* Border shorthand */

   div {
    border : 5px solid blue;
   }
    ```
    - **Border Sides** (to control the individual side of the box)<br>
        - border-left
        - border-right
        - border-top
        - border-bottom<br>

     Example : <br> 
    ```css
   div {
    border-top: 5px;
    border-left-color: red;
    border-right-style: dashed;
   }

   /* Border Side shorthand */

   div {
    border-bottom : 5px solid blue;
   }
    ```
    - **Border Radius** (to control the edges of the border)<br>

     Example : <br> 
    ```css
   div {
    border-radius: 5px;
   }
    ```
- **Padding**
    - padding-left
    - padding-right
    - padding-top
    - padding-bottom<br>

     Example : <br> 
    ```css
   div {
    padding-left: 5px;
    padding-right: 5px;
   }
    ```
    - Padding Shorthand
        - for all sides<br>
       ` padding: 20px;`<br>

       - top & bottom | left and right<br>
       `padding: 10px 20px`<br>

       - top | left & right | bottom<br>
       `padding: 10px 20px 10px;`<br>

       - top | right | bottom | left ***(clockwise)**<br>
       `padding: 2px 5px 2px 5px;`

- **Margin**<br>
     **To set spacing in the outside of the border**<br>
    - margin-left
    - margin-right
    - margin-top
    - margin-bottom <br>

    Example : <br> 
    ```css
   div {
    margin-left: 5px;
    margin-right: 5px;
   }
    ```
    - Margin Shorthand
        - for all sides<br>
       ` margin: 20px;`<br>

       - top & bottom | left and right<br>
       `margin: 10px 20px`<br>

       - top | left & right | bottom<br>
       `margin: 10px 20px 10px;`<br>

       - top | right | bottom | left ***(clockwise)**<br>
       `margin: 2px 5px 2px 5px;`<br>

## Inline Vs Block Element<br>
- Inline Element
    - Takes up only necessary width
    - Don't start from new line

- Block Element
    - Takes up the full width available
    - Start from new line

## Display<br>
**It sets whether an element is treated as a block or inline element and the layout used for it's children**<br>
    Example : <br> 
```css
   h2 {
    display: inline;
   }
```
```css
/* inline-block behaves like inline but element style is block */
   h2 {
    display: inline-block;
   }
```
```css
/* does not display the element */
   h2 {
    display: none;
   }
```
## Alpha Channel <br>
It is used to show the opacity of colors <br>
 Example : <br> 
```css
   div {
    background-color: rgba(255,0,0,0.5)
   }

   /* a range from 0 - 1; */
```
## Opacity <br>
It is used to show the opacity of element <br>
 Example : <br> 
```css
   div {
    opacity: 1;
   }

   /* opacity range from 0 - 1; */
```
## Transition <br>
Transition enables us to define the transition between two states of an element  <br>
 Example : <br> 
```css
   div {
    height: 100px;
    width: 100px;
    background-color: red;
    transition-duration: 2s;
   }

   div:hover {
    background-color: blue;
   }
```
**Shorthand Method**<br>
property name | duration | timing-function | delay <br>
`transition: margin-top 2s ease-in-out 0.2s`<br>

## Transform CSS <br>
Transform property lets us rotate, skew, scale or translate an element <br>
- rotate <br>

Example : <br> 
```css
   div {
    transform: rotate(45deg);
   }
``` 
- scale <br>

Example : <br> 
```css
   div {
    transform: scale(2);
   }

   /* div size will be double */
```
- translate <br>

Example : <br> 
```css
   div {
    transform: translate(20px, 30px);
   }

   /* 20px is the movement frim x-axis, 30px is the y-axis movement */
```
- skew <br>

Example : <br> 
```css
   div {
    transform: skew(30deg);
   }

   /* div will resize in tilt shape */
```
## Box Shadow <br>
It adds shadows effect around an element's frame <br>
**box-shadow**<br>

**`box-shadow: 2px 2px 10px red;`** <br>

   - 2px is along x-axis
   - 2px is along y-axis
   - 10px is blur radius
   - red is the color <br>
## Background Image <br>
It lets us set image as a background <br>
Example : <br> 
```css
   div {
    background-image: url(""); /*location of the image */
    background-size: contain; /* contain takes same image size as original */
                    : cover;   /* cover takes crop size of the image */
                    : auto;    /* auto takes stretch size of the image */
   }

```
## Position <br>
Position is used in CSS to set an element how is this positioning in the document. `top`, `right`, `bottom`, `left` determine the final location of the element <br>
- static
    - the `top,right,left,bottom` and `z-index` properties have no effect.This is use as a default value <br>

    Example : <br> 
```css
   div {
    position: static;
   }

   /* the position will be static and no top, bottom etc value will apply on this div */
```
- relative
    - the position is related to offset itself based on the top, bottom, left, right <br>

    Example : <br> 
```css
   div {
    position: relative;
    top: 100px;
    left: 100px;
   }

   /* the position will be on the right side of that element position due to the position set left=100px and bottom side of that element position due to top=100px.There will be empty space for the moved div also.*/
```
- absolute
    - the element is removed from the normal document flow, and no space has been created for the element in the page layout.It is positioned relative to it's closest positioned ancestor, if any; otherwise it is placed relative to initial containing block.<br> 

    Example : <br> 
```css
   div {
    position: absolute;
    top: 100px;
    left: 100px;
   }
    /* the position will be counting from the document body if no position applied on parent element.So it will move 100px from top of the document and move 100px from left side of the document.There will be no empty space for absolute position */  
```
- fixed
    - the element is removed from the normal document flow.No space is created for the element in the page layout. It is positioned relative to the initial containing block established by the viewpoint.<br>
    Example : <br> 
```css
   div {
    position: fixed;
    top: 100px;
    left: 100px;
   }
   /* the element will be fixed in the document.It will position in same as absolute value but it will move along with the document scrolling.*/
```
## Flexbox <br>
Flexible box layout. It is a one-dimensional layout method for arranging items in raws or columns<br>
### Flexbox Model <br>
flexbox model is basically directional based.If it's direction is row-based(---),
the `main axis` will be row type and the `cross axis` will be column side.If the direction is column-based(|), the main axis will be column-based .
and cross axis will be row side.<br>

### Flex Direction <br>
It sets how flex items are placed in the flex container, along which axis and direction <br>
- `flexbox-direction: row;` // main axis , left to right
- `flexbox-direction: row-reverse;` // main axis, right to left
- `flexbox-direction: column;` // main axis , top to bottom
- `flexbox-direction: column-reverse;` // main axis, bottom to top <br>

Example : <br> 
```css
   div {
    display: flex;
    flex-direction: row; /* main axis will be directed as row side */
    flex-direction: column; /* main axis will be column wise */
   }
```
### Justify Content <br>
Tells the browser about distributing space between and around content items along main axis <br>
```css
# `justify-content: flex-start;` /* placed elements at the top of main axis */
# `justify-content: flex-end;` /* placed at the bottom of the main axis */
# `justify-content: center;` /* center the elements in main axis */
```

Example : <br> 
```css
   div {
    display: flex;
    flex-direction: row;
    justify-content: flex-end;

    /* main axis is left to right, so elements will be placed bottom of the main axis */
   }
```
### Flex Wrap <br>
Sets whether flex items are forced onto one line or can wrap onto multiple line .The `flex-wrap` property specifies whether the flexible items should wrap or not.<br>
```css
# `flex-wrap: nowrap;` /* default wrap state, no changes as it tries to fit in one line */
- `flex-wrap: wrap;` /* the element value of width or height will be applicable, could be into multiple lines */ 
- `flex-wrap: wrap-reverse;` /* cross axis reverse */
```

Example : <br> 
```css
   div {
    height: 50px;
    width: 200px;
    display: flex;
    flex-direction: row;
    justify-content: flex-end;
    flex-wrap: wrap;
   }

   /*it will try to fit all elements of div with the same height and width*/
```
### Align Item <br>
Distribute our items along cross axis <br>
```css
# `align-items: flex-start;` /* cross axis top */
# `align-items: flex-end;` /* cross axis bottom */
# `align-items: center;` /* center the elements in cross axis */
# `align-items: baseline;` /* any type of content in element moves to same baseline */
```
Example : <br> 
```css
   div {
    height: 50px;
    width: 200px;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    flex-wrap: wrap;
    align-items: flex-end;
   }
```
### Align Content <br>
It sets the distribution of space between and around content items along a flexbox cross axis.
Align-items defines how the browser distributes space between and around items vertically.
Think of it as justify-content but for the vertical axis <br>
```css
# `align-content: flex-start;` /* The items are packed flush to each other against the edge of the alignment container depending on the flex container's cross-start side. This only applies to flex layout items. For items that are not children of a flex container */
# `align-content: flex-end;` /* The items are packed flush to each other against the edge of the alignment container depending on the flex container's cross-end side. This only applies to flex layout items. For items that are not children of a flex container, this value is treated like end */
# `align-content: center;` /* content will move to center along cross axis */
# `align-content: space-around;` /* add spaces to content from top, bottom and middle along cross axis */
# `align-content: space-evenly;` /* add spaces evenly */
```

Example : <br> 
```css
   div {
    height: 50px;
    width: 200px;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    flex-wrap: wrap;
    align-content: flex-start;
   }
```
### Align Self <br>
Distribute an item along cross axis . **Specificity** : `align-self > align-items`<br>
```css
# `align-self: flex-start;` /* cross axis top for individual item */
# `align-self: flex-end;` /* cross axis bottom for individual item */
# `align-self: center;` /* center the element in cross axis */
# `align-self: baseline;` /* any type of content in a element moves to same baseline */
```

Example : <br> 
```css
   div {
    height: 50px;
    width: 200px;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-item: flex-start;
   }
   .classDiv {
    align-self: flex-end;
   }

   /* align-self value will be counted for that individual div */
```
### Flex Sizing
Flex sizing is used to resize the flex <br>
- `flex-basis;` // It sets the initial size of a flex item
Example : <br> 
```css
   div {
    height: 50px;
    width: 200px;
    display: flex;
    flex-direction: row;
    justify-content: flex-start;
    align-items: flex-start;
   }
   .classDiv {
    flex-basis: 200px;
   }

   /* flex basis will be 200px width for that individual div */
```
### Flex Grow

It specifies how much the of the flex container's remaining space should be assigned to the flex item's main size <br>

Example: <br>
```css
    div {
        flex-grow: 1; /*occupy total width or height of the div*/
    }
```
### Flex Shrink <br>
Flex shrink is used when elements overflow from the div. it sets the flex shrink factor of a flex item. <br>
 Example: <br>
```css
    div {
        flex-shrink: 2; /* shrink double width or height of element from other elements on the div */
    }
```
### Flex Shorthand <br>
- `flex-grow` | `flex-shrink` | `flex-basis` <br>
**`flex: 2 2 50px;`** <br>

- `flex-grow` | `flex-basis` <br>
**`flex: 2 50px;`** <br>

- `flex-grow(unitless)` <br>
**`flex: 2;`** <br>

- `flex-basis` <br>
**`flex: 50px;`**<br>

## CSS Grid

Setting a container's display to grid will make all the children grid items.Works like a block element or container <br>
Example : <br>
```css
container{
    display: inline-grid;
}
/* inline-grid value works like inline */
```
### Grid Template <br>
They define the line and tracks sizing of grid <br>
Example : <br>
```css
div {
    grid-template-rows: 50px 50px 50px;
    grid-template-columns:100px 100px 100px;
}
```
**Repeat**<br>
Repeat is divided into all available spaces <br>
```css
# `grid-template-rows: repeat(3, 1fr);` /* 1 fraction of 100% width available spaces, count = 3; */
# `grid-template-rows: 1fr 1fr 1fr;` /* alternative approach */
# `grid-template-column: repeat(3, 1fr);` /* 1 fraction of 100% height available spaces */
# `grid-template-column: 1fr 1fr 1fr;` /* alternative approach */
```

### Grid Gaps <br>
Define the gaps between lines <br>
```css
# `row-gap: 10px;`
# `column-gap: 10px;`
# `grid-gap: rowGap columnGap;` /* for single value, both rowGap and columnGap will be same*/
```

### Grid Column <br>
Define an item's starting position and ending position inside the column <br>
```css
# `grid-column-start: line_number;` /* the value will be occupied for the whole horizontal line till end value*/
# `grid-column-end: line_number;` /* end value*/
# `grid-column: startColumn / endColumn;` /*defining both starting and ending for the shorthand technique*/
# `grid-column: startColumn / span number;`/* span means how many column we need after starting*/
```

### Grid Rows <br>
Define an item's starting position and ending position inside the row <br>
 ```css
# `grid-row-start: line_number;` /* the value will be occupied for the whole vertical line till end value*/
# `grid-row-end: line_number;` /* end value */
# `grid-row: startRow / endRow;` /*defining both starting and ending for the shorthand technique*/
# `grid-row: startRow / span number;`/* span means how many row we need after starting*/
```

Example : <br>
```css
#div {
    grid-column: 1 / 3; /* 1 = startColumn, 3 = endColumn */
    grid-row: 1 / span 3; /*1 = startRow , span = 3(occupies 3 row) */
}
```
### Grid Properties <br>

- Horizontal
    - `justify-items;` // for multiple items(container)
        - `justify-items: center;`
        - `justify-items: start;`
        - `justify-items: end;`
 
    - `justify-self;` // single item (item)

- Vertical
    - `align-items;` // for multiple items (container)
    - `align-self;` // for single item (item)
- Both Direction
    - `place-items;`
    - `place-self;`
   
    Example :<br>
    ```css
    .container {
        place-items: center; // if both justify-item and align-items are same
    } 

    #item {
        place-self: start; // if both jusify-self and align-self are same
    }
    ```
## CSS Animation 

To animate CSS element <br>
Example : <br>
```css
    @keyframes myAnimation {
        from {font-size: 20px;}
        to {font-size: 40px;}
    }
    
    //alternative
    @keyframes myAnimation {
        0% {font-size: 20px;}
        50% {font-size: 30px;}
        100% {font-size: 30px;}
    }

    div {
        animation-name: fontAnimation;
        animation-duration: 3s;
        animation-timing-function: ease-in;
        animation-delay: 0;
        animation-iteration-count: 2;
        animation-direction: normal;

        /*Shorthand */
        animation: fontAnimation 3s ease-in 0s 2 normal;
    }
```
## Media Queries
Help to create a responsive website <br>
Media features - width (of viewpoint) <br>
Example : <br>
```css
@media(width: 400px){
div {
   background-color: red;
    }
}
```
## Z- Index 
It decides the stack level of elements. Overlapping elements with a larger z-index cover  those with a smaller one. position should not be static or default. <br>
Example : <br>
```css
div1 {
    position: relative;
    z-index: auto(0); /*default value*/
    z-index: 1; /* if the value is higher than other z-index, it will show in front */
    }

div2 {
    position: relative;
    z-index: -1; /*if the value is lower than other z-index, it will stay behind the other element*/
}
```

### Color Palette
- Primary Color: `#3498db`
- Secondary Color: `#2ecc71`
- Background: `#f4f4f4`
