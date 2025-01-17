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

