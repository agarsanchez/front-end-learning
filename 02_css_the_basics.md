[Back](README.MD)
# CSS THE BASICS
[samples html](html/css_samples.html)

## Selectors

### The classic:
```css
body {}
#myId {}
.myClass {}
* {}
```

### The forms:

```css
:checked {}
:focus {}
:disabled {}
:enabled {}
:valid {}
:invalid {}
:required {}
:optional {}
:read-only {}
```

### The helpful ones but not so famous:
```css
[title] {}
[target=_blank] {} /* equals */
[id^=list-item] {} /* starts with substring */
[href$=.pdf] {} /* ends with substring */
[href*=santander] {} /* contains substring */
[href~=facebook] {} /* contains word */

```

## Building queries to find nemo

```css
#myContainer .childItem {}
#myContainer > .directChildItem {}
input + label {}
li.completed ~ li {}
li:first-child() {}
li:nth-child(25) {}
```

## Grouping selectors
```css
.nice-paragraphs, .nice-links {color: blue;}
```

## Specificity

### 10_000 - Crazy important styles
```css
#beer {font-weight: bold!important;}
```

### 1000 - Inline styles
```html
<div class="hidden-thing" style="display: none;">
```

### 100 - IDs
```css
#important-thing {color: blue;}
```

### 10 - Classes, attributes and pseudo-classes 
```css
.nice-thing {font-weight: normal;}
[target=_blank] {}
a:hover {}
```

### 1 - Elements and pseudo-elements
```css
p {color: black;}
:before {content: 'hi there'}
```

## Building queries to sort our styles

```css
.base-product {}
.apple-products .base-product {}
.samsung-products .base-product {}
```
please get an agreement with the developers for naming conventions

## Building queries to fight
```css
#stubborn-block .inner-paragraph {} /*100 + 10 = 110*/
#stubborn-block p.inner-paragraph {} /*100 + 10 + 1 = 111*/
```
Please don't do this if you don't have 3rd party styles.