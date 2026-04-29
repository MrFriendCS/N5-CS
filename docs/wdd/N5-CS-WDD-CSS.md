# Cascading Style Sheets (CSS)

## Comments

Single line comment.

``` css
/* This comment is not displayed */
```

Multiline comment.

``` css
/*
This comment is not displayed
This comment is not displayed
*/
```

## CSS rules

Rules are terminated with a semicolon, **`;`**. A rule with a single property will be valid without a semicolon but a rule with multiple properties will not.

### Single property

``` css
selector {property: value;}
```

### Multiple properties

``` css
selector {property: value;
          property: value;}
```

## Selectors

### Element selectors

Element selectors are HTML tags without the angle brackets.  All elements of that type will have their formatting modified by the CSS rule(s).

``` css
p {property: value;}
```

### Class selectors

Class selectors use the class name with a dot in front.

``` css
.mainPara {property: value;}
```

### ID selectors

ID selectors use the ID name with a hash in front.

``` css
#importantPara {property: value;}
```

## Properties

**Note:** All examples will use a HTML element as the selector but would work equally well with class or ID selectors.

### Font

``` css
p {font-family: sans-serif;}

h1 {font-size: large;}
```

### Alignment

``` css
h2 {text-align: left;}

h3 {text-align: center;}

h4 {text-align: right;}
```

### Colour

The colour of the text and / or the background can be changed using one of the many predefined colours.  To see a list visit [W3Schools](https://www.w3schools.com/colors/colors_names.asp). 

To change the colour, the properties are:

* __text__: `color`
* __background__: `background-color`

``` css
h5 {color: DarkRed;
    background-color: Cornsilk;}
```

### Size

There is ___no___ space between a value and the unit.

``` css
img {width: 50%;
     height: 50%;}
```

``` css
video {width: 240px;
       height: 180px;}
```


## CSS Precedence

### Selectors

 * Element rules overwrite default rules
 * Class rules overwrite element rules
 * ID rules overwrite class rules

### Location

 * External rules overwrite default rules
 * Internal rules overwrite external rules
 * Inline rules overwrite internal rules
