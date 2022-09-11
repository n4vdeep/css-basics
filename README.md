# CSS Basics

## Selectors
3 basic types:
- Element selector; e.g. `body`
- Class selector, starts with a period; e.g. `.gray`
- ID selector, starts with # and should be unique; e.g. `#second`
- "`*`" universal selector

## Specificity
An Element selector is the lease specific followed by the class selector and then the ID selector being the most specific. 

NB:Inline styles will override all of the above selectors and the style element selector in specificity however.

## !important
`!important` wil override every other selector regardless of what method it is. Dont use this unless there is a valid reason.

## Selector Code Example
### Element
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
### Class
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
### ID
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
### !important
```
#second {
  color: red !important;
}
```
