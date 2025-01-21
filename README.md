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

` 1 inch = 96 px`<br>
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
||ID    |Class, attributes & Pseudo class|Element & Sudo-Element|----|----
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
- example : <br> 
    ```
   button {
    background-color: inherit;
   }
    ```