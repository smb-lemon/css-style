# CSS STYLESHEET

**CSS means Cascading Style Sheet**<br>

*What is CSS?*<br>
**It is a language which is used to style or design a document**

*Example*<br>
```
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
```<h1 style = "color : yellow"> HTML Page <h1>``` <br>
***Disadvantage* : When working with the large project, inline style is not feasible solution** 

- **Style Tag `<style>` :** <br>
**Style is added using the `<style>` tag in the same document**t
```
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
``` 
## Linking HTML with CSS file
<head>
    <link rel="stylesheet", href="style.css"> ##href = css file path
</head>
```
## Color Property

**Color property is used to set the color of foreground**<br>
*Examples*<br>
```
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
```
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
```
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
```
h1 {
    font-weight: bold; //700
}
```
<p style = "font-weight : bold">Font Weight is Bold</p>

### Text Decoration<br>
**Text decoration is basically decorating text in various ways like underline , overline in text**<br>
*Example:*<br>
```
h1 {
    text-decoration: line-through;
}
```
<p style = "text-decoration: orange line-through">This text is Line Through</p>

**When the text decoration value is none, any existing underline or overline will be removed**<br>
### Line Height <br>
**Line height is basically the height between two lines**<br>
*Example:*<br>
```
h1 {
    line-height: 2;
}
```
### Letter Spacing <br>
**Letter spacing is used to space between letters horizontally**<br>
*Example:*<br>
```
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
```
h1 {
    width: 50%;
}
```
### em <br>
font size of parent, in the case of typographical property like font-size or other property like width, margin <br>
*Example:*<br>
```
#outerDiv {
    font-size: 20px;
}

#innerDiv {
    font-size: 2em;
    padding: 1em;

// font-size will be 40px as 2em & padding will be 40px as the font size is 40px
}
```
**Drawbacks of em :** Snowball effect in nested elements <br>
## rem(Root em) <br>
Font size of the root element <br>
*Example:*<br>
```
section {
    font-size: 10px;
}

div {
    font-size: 2rem; 
}

//for multiple nested divs, rem will be the root(Section)
```
### Font Family <br>
**Font family is used to specify one or more family font**<br>
*Example:*<br>
```
h1 {
    font-family: fantasy;
}
```
<p style = "font-family : fantasy">This text is fantasy's Default font</p>

## Selectors <br>
**On Importance Basis : *`Id > Class > Element`***<br>
```
<div class="greetDiv">
        <p class="greetPara">
            Hello world
        </p>
    </div>
```
```
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
```
h2 {
    property: value; !important
}
```
**If the Value is same ,it will follow cascading rule and the last value will be the final value**<br>

**In any html fine, to select any set or group of files or individual element so that we can apply style on them is called Selectors**<br>
### Universal Selector<br>
To select everything in a document<br>
*Example:*<br>
```
* {
    property: value;
}

// * is the Universal Selector
```
## Element Selector<br>
It is used to select all the elements of the same type<br>
*Example:*<br>
```
h2 {
    property: value;
}

// h2 is the Element Selector
```
## ID Selector<br>
Id selector is used based on the value of element's id attribute<br>
*Example:*<br>
```
#myId {
    property: value;
}

// myId is the ID Selector
```
## Class Selector<br>
Class selector is used based on the element's class attribute<br>
*Example:*<br>
```
.myClass {
    property: value;
}

// myClass is the Class Selector
```
## Descendant Selector<br>
Descendant selector selects elements of parent element<br>
*Example:*<br>
```
div p {
    property: value;
}

// p is the Descendant Selector
```
## Adjacent Sibling Combinator <br>
**Combinator is basically adding multiple selector together.As the descendant selector works on parent element, this sibling combinator works as sibling element, ex : h3 comes immediately after p tag.Basically they are on the same level**<br>
*Example:*<br>
```
p+h3 {
    property: value;
}

// + is the sibling combinator
```
## Child Combinator <br>
**Child  combinator works as parent and children relation.ex : selects all button which are direct children of span.Child combintor can only go one level up(disadvantage)**<br>
*Example:*<br>
```
span > button {
    property: value;
}

// > is the child combinator
```
## Attribute Selector<br>
**Attribute selector selects elements based on the presence or value of a given attribute**<br>
*Example:*<br>
```
input[attriute=""] {
    property: value;
}

// = is the Attribute Selector
```
## Pseudo Class<br>
A keyword added to the selector that specifies a special state of the selected elements<br>
- **hover**
    - example : <br> 
    ```
    button:hover{
    background-color: black;
    }
    ```
- **active**
    - example : <br> 
    ```
    p:active{
    font-weight: bold;
    }
    ```
- **checked**
     - example : <br> 
    ```
    input[type="radio"]:checked + label{
    color: red;
    font-weight: bold;
    }
    ```
- **nth-of-type**
     - example : <br> 
    ```
   div:nth-of-type(3){
    background-color: cornflowerblue;
    }
    ```
- **default**
    - example : <br> 
    ```
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
    ```
   :disabled {
    background-color: grey;
   }

    //disabled required
    ```
## Pseudo Element<br>
A keyword added to the selector which is used to modify specific part of the element <br>
- **first-letter**
    - example : <br> 
    ```
   h1::first-letter {
    color: grey;
   }
    ```
- **first-line**
    - example : <br> 
    ```
   h1::first-line {
    color: blue;
   }
    ```
- **selection**
    - example : <br> 
    ```
   p::selection {
    background-color: blue;
   }
    ```
## Inheritance<br>
When we need apply some style to div as parent element, it will apply to all other element in that div(**`button,input`** etc are different).To use the same value in these elements we can use `inherit` value.**`height,width,border`(non-inherit**)<br>

 Example : <br> 
```
   button {
    background-color: inherit;
   }
```
## Box Model <br>
- **Height**
    - Height refers as the area of content height.<br>

    Example : <br> 
    ```
   div {
    height: 100px;
   }
    ```
- **Width**<br>
    - Width refers as the area of content width.<br>

    Example : <br> 
    ```
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
    ```
   div {
    border-width: 5px;
    border-style: solid;
    border-color: blue;
   }

   // Border shorthand

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
    ```
   div {
    border-top: 5px;
    border-left-color: red;
    border-right-style: dashed;
   }

   // Border Side shorthand

   div {
    border-bottom : 5px solid blue;
   }
    ```
    - **Border Radius** (to control the edges of the border)<br>

     Example : <br> 
    ```
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
    ```
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
    ```
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
```
   h2 {
    display: inline;
   }
```
```
// inline-block behaves like inline but element style is block
   h2 {
    display: inline-block;
   }
```
```
// does not display the element
   h2 {
    display: none;
   }
```
## Alpha Channel <br>
It is used to show the opacity of colors <br>
 Example : <br> 
```
   div {
    background-color: rgba(255,0,0,0.5)
   }

   // a range from 0 - 1;
```
## Opacity <br>
It is used to show the opacity of element <br>
 Example : <br> 
```
   div {
    opacity: 1;
   }

   // opacity range from 0 - 1;
```
## Transition <br>
Transition enables us to define the transition between two states of an element  <br>
 Example : <br> 
```
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
```
   div {
    transform: rotate(45deg);
   }
``` 
- scale <br>

Example : <br> 
```
   div {
    transform: scale(2);
   }

   //div size will be double
```
- translate <br>

Example : <br> 
```
   div {
    transform: translate(20px, 30px);
   }

   //20px is the movement frim x-axis, 30px is the y-axis movement
```
- skew <br>

Example : <br> 
```
   div {
    transform: skew(30deg);
   }

   //div will resize in tilt shape
```
## Box Shadow <br>
It adds shadows effect around an element's frame <br>
**box-shadow**<br>

**`box-shadow: 2px 2px 10px red;`** <br>

   - 2px is along x-axis
   - 2px is along y-axis
   - 10px is blur radius
   - red is the color 