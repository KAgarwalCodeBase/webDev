## Resources:

[fontawesome](https://fontawesome.com/): For fonts and emojis.  
[pexels](https://pexels.com/): For free images and videos.  
[w3schools](https://www.w3schools.com/css/): For learning CSS.  
[Codepip](https://codepip.com/games/): Games to play for learning flexbox and CSS grid.


## Types of CSS:
1 - Inline CSS  
2 - Internal CSS  
3 - External CSS  

## Colors
1 - Colors Name  
2 - RGB  
3 - HEX  

## Units:
There are two types of length units: absolute and relative.
### Absolute Units
![Absolute Units](../assets/absolute-unit.png)

### Relative Units
![Relative Units](../assets/relative-unit.png)

## Font formatting in CSS

`font-family: sans-serif;`  
`font-size: 20px;`  
`text-transform: capitalize;`  
`line-height: 20px; [space between two lines]`  
`letter-spacing: 5px; [space between two characters]`  
`word-spacing: 10px; [space between two words]`  
`text-align: center;`  
`text-decoration: underline;`  
`cursor: auto;`  
`font-weight: bold;`  

For using more fonts: https://fonts.google.com

## Box model

### Border
`border-width: 20px;`  
`border-styled: dotted;`  
`border-color: red;`  
`border: 10px dotted teal;`  
`border-right: 10px dotted teal;`  
`border-left: 10px dotted teal;`  
`border-top: 10px dotted teal;`  
`border-bottom: 10px dotted teal;`  

### Padding
`padding-left: 10px`  
`padding-right: 10px`  
`padding-top: 10px`  
`padding-bottom: 10px`  
`padding: 10px 20px; [10px for top and bottom, 20px for left and right]`  

### Margin
`margin: 10px;`  
`margin-left: 10px;`  
`margin-right: 10px;`  
`margin-top: 10px;`  
`margin-bottom: 10px;`  

### Background Properties
`background-color: green;`  
`background-image: url("img1");`  
`background-repeat: no-repeat;`  
`background-size: cover;`  
`background-position: bottom;`  
`background-attachment: fixed;`   

## Gradient in CSS
There are two types of gradient linear and radial.

`background-image: liner-gradient(to bottom, rgba(..), rgba(..)), url(...);`

`background-image: radial-gradient(blue, skyblue), url(...);`


## Filters

`filter: blur(10px);`  
`filter: brightness(50%);`  
for more info: https://www.w3schools.com/cssref/css3_pr_filter.php

## Advance Selector in CSS

### class selector

### id selector  

### Everything selector  
`select everything in html`
```
* {
    border: 2px solid red;
  }
```
<br>

`select everthing inside the section`
```
section * {
    border: 2px solid teal;
}
```
<br>

`Element class selector`
```
<div>This is sample div</div>
<div class='text'> This is text class div </div>


div.text{
    color: teal;
}

This selector will select the div which have class text.
```

`List of all CSS selectors`
![CSS selector Img](../assets/css-selectors.png)

## Display Property in CSS

`Inline`: It does not take height and width
example: span, img etc.

`Block`: Displays an element as a block element. It starts on a new line, and takes up the whole width.

`inline-block`: Display an element as inline-level block container.

`none`: Element is completely remove from DOM.

`List of all different kind of display properties`
![CSS selector Img](../assets/css-display-property.png)


## Using Fonts

Go to `fontawesome.com `and search for respective icon and add it's html in the code.
And also add cdn stylesheet link of font awesome from `cdnjs.com`.


## Box Shadow

`index.html`
```
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <div></div>
    </body>
</html>
```

`style.css`
```
/* x y blurness color*/
div{
    width:200px;
    height:200px;
    background:rgb(105, 105, 205);
    box-shadow: 15px 10px 4px orange;
}
```

## CSS Inheritance

Inheritance is when we declare something on an element, and it also applies that element's decendant.

CSS inheritance is only applied to typography related properties to its child and not for layout related properties.  

`index.html`
```
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" href="style.css">
    </head>
    <body>
        <div class="parent">
            Hello
            <div class="children">World</div>
        </div>
    </body>
</html>

```
`style.css`
```
/*Layout properties are not implicit inherit by children, required to use inherit keyword.*/
.parent{
    font-family: Cambria;
    font-weight: bold;
    font-style: italic;
    font-size: 2rem;
    color: orange;
    width: 100px;
    height: 100px;
    background-color: teal;
}

.children{
    position: relative;
    left: 100px;
    width: inherit;
    height: inherit;
    background-color: inherit;
}
```
![CSS Inheritance Example](../assets/css-inheritance.png)


## CSS positions

In position relative element is not leaving its position.
Whereas in position absolute, element is leaving its position.

Fixed: The element is positioned relative to the browser window	


![CSS Position Values](../assets/css-position-values.png)


## Flexbox

`display: flex`  

This properties work on main axis.  
`flex-direction: column` [default: row]  
`flex-wrap: wrap`  
`justify-content: center;`  

This properties work on cross axis.  
`flex-wrap: wrap`  
`align-content: space-between;` [align-content works with flex-wrap not a standalone.]

This properties work on single items.  
`order: 1;`  
`align-self: center;`  
`flex-grow: 1;` [default 0]  
`flex-basis: 10px;`  
`flex-shrink:4;`

Note:  
1 - The two properties `flex-direction` and `flex-wrap` are used so often together that the shorthand property `flex-flow` was created to combine them. This shorthand property accepts the value of the two properties separated by a space.

For example, you can use `flex-flow`: row wrap to set rows and wrap them.

Try using flex-flow to repeat the previous level.


2 - `align-items`: This CSS property aligns items vertically and accepts the following values:

`flex-start`: Items align to the top of the container.  
`flex-end`: Items align to the bottom of the container.  
`center`: Items align at the vertical center of the container.  
`baseline`: Items display at the baseline of the container.  
`stretch`: Items are stretched to fit the container.  




3 - `align-content`: It is used to set how multiple lines are spaced apart from each other. This property takes the following values:

`flex-start`: Lines are packed at the top of the container.  
`flex-end`: Lines are packed at the bottom of the container.  
`center`: Lines are packed at the vertical center of the container.  
`space-between`: Lines display with equal spacing between them.  
`space-around`: Lines display with equal spacing around them.  
`stretch`: Lines are stretched to fit the container.  

This can be confusing, but `align-content` determines the spacing between lines, while `align-items` determines how the items as a whole are aligned within the container. When there is only one line, `align-content` has no effect.

for practicing flex box: [flexfroggy](https://flexboxfroggy.com/)


## CSS Grid

The CSS Grid Layout Module offers a grid-based layout system, with rows and columns, making it easier to design web pages without having to use floats and positioning.  

`Difference between grid and flex box.`  
<image src="../assets/css-grid1.png" alt="css grid image 1" width="300" style="border: 2px solid orange">
<br/><br/>
`Grid Line`  
<image src="../assets/css-grid2.png" alt="css grid image 1" width="300" style="border: 2px solid orange">
<br/><br/>
`Grid Track`  
<image src="../assets/css-grid3.png" alt="css grid image 1" width="300" style="border: 2px solid orange">
<br/><br/>
`Grid Cell`  
<image src="../assets/css-grid4.png" alt="css grid image 1" width="300" style="border: 2px solid orange">
<br/><br/>
`Grid Area`  
<image src="../assets/css-grid5.png" alt="css grid image 1" width="300" style="border: 2px solid orange">

### Need to set display property of container as grid.  
`display: grid;`  

### For defining number of columns and rows:  
`grid-template-columns: 100px 100px 100px;`  
`grid-template-rows: 100px 100px 100px;`  

### By Using repeat function.  
`grid-template-columns: repeat(3, 100px);`  
`grid-template-rows: repeat(3, 100px);`  

### Providing name to lines:  
`grid-template-columns: [startc]100px 100px [endc]100px;`  
`grid-template-rows: [startr]100px 100px [endr]100px;`  

### Using fractional values with respect to view viewport.  
`grid-template-columns: 2fr 1fr 3fr;`  

### Using minmax Function, so control the size of element  
`grid-template-columns: 1fr minmax(200px, 1fr) 1fr;`  

    
### Using auto-fit  
`grid-template-columns: repeat(auto-fit, 200px);`  

### Using auto-fill  
`grid-template-columns: repeat(auto-fill, 200px);`  

## Defining size of particular html element.
```
aside {
    grid-column-start: 1;
    grid-column-end: 3;

    /*grid-column: 1/3; (shortcut)*/
}
```
### For Defining the template structure, by using grid-template-area and grid-area.

```
.container{
    background-color: rgb(34, 34, 34);
    padding: 20px;
    height: 100vh;
    /*Grid Stuff*/
    display: grid;
    grid-template-columns: repeat(4, 100px);
    grid-template-rows: repeat(5, 100px);
    grid-gap: 10px;

    grid-template-areas: 
    "h h h h" 
    "m m m m"
    "s s . a"
    "f f f f";
}

header{
    grid-area:h;
}

main{
    grid-area: m;
}

section{
    grid-area: s;
}

aside {
    grid-area: a;
}

footer{
    grid-area:f;
}
```
<br/>
<img src="../assets/css-grid-layout.png" style="border:2px solid orange;" alt="CSS Grid Layout Image">

For practicing css grid: [Grid Garden](https://cssgridgarden.com/)

## Media Query

Media queries allow you to apply CSS styles depending on a device's media type.

```
@media screen and (max-width: 900px) {
    body {
        background-color:aliceblue;
    }
}
```