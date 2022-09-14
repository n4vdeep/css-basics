# CSS Basics

## Selectors
3 basic types:
- Element selector; e.g. `body`
- Class selector, starts with a period; e.g. `.gray`
- ID selector, starts with # and should be unique; e.g. `#second`
- "`*`" universal selector

## Specificity
An Element selector is the least specific followed by the class selector and then the ID selector being the most specific. 

**NB**: Inline styles will override all of the above selectors and the style element selector in specificity however.

## !important
`!important` wil override every other selector regardless of what method it is. Dont use this unless there is a valid reason.

### Selector Code Example
#### From <style></style> Tags
```
<style>
  h1 {
    font-color: purple;
  }

  p {
    font-style: italic;
  }
</style>
```
#### Inline Styles
```
<p style="color:red;">A red paragraph.</p>
```
#### From Separate Style Sheet File (style.css)
#### Element
HTML
```
<body>
...
</body>`
```
CSS
```
body {
  font-size: 22px;
}
```
#### Class
HTML
```
<p class="gray">`
```
CSS
```
.gray {
  color: gray;
}
```
#### ID
HTML
```
<p id="second">`
```
CSS
```
#second {
  font-style: italic;
}
```
#### !important
```
#second {
  color: red !important;
}
```

## Colors
There are 5 main ways to specify color in CSS:
- the color by word
- rgb
- rgba
- hexadecimal
- hsl

### Color Code Examples
```
p {
  color: red;
  color: rgb(255, 0, 0);
  color: rgba(0, 255, 0, 0.5);
  color: #0000ff;
  color: hsl(50, 100%, 50%);
}
```
Hexadecimals colors can also be entered in a short hand format of 3 characters if the sequence is repeating characters of 6:

### Example:

`color: #ffffff` > `color: #fff`\
`color: #000000` > `color: #000`\
`color: #333333` > `color: #333`

## Units
The most common unit used in CSS is pixels (px) the px is also an absolute value, there are however others:
### rem
This relates to the font size of the root element, i.e. the `html` element and NOT the parent element this is known as a relative unit.

Example:

```
html {
  font-size: 16px;
}

p {
  font-size: 2rem;
}
```
This would equate to the `p` element having a font size of 32px absolute.

### em
With this unit the parent element will look at the root element and resize according to what the root size is (usually default) and then whatever is set to `em` will be resized based on the parent element.

Example:

```
html {
  font-size: 16px // default browser font size
}

h1 {
  font-size: 3rem;
  padding: 0.5em;
}
```
Here the font size of `h1` at 3rem will be multiplied by the `html` font size of 16px giving a font size of 48px

The padding of 0.5rem looks at the 3rem font size and because this is 48px it is halved, 48x0.5=24px padding.


### vw (viewport width)
### vh (viewport height)
### % 
