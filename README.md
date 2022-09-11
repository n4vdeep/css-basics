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
### body
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
````

### .gray
HTML
```
<p id="second" class="gray">`
```
CSS
```
.gray {
  color: gray;
}
```
### #second

```
<p id="second" class="gray">`
```
```
#second {
  font-style: italic;
}
```