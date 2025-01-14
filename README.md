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
