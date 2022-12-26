---
title: "The DOM"
description: "Guide to modify the DOM with Javascript"
created: 13-10-2022
tags:
- programming
- javascript
- DOM
---
# DOM

## LINKS TO COURSES AND TUTORIALS
[The DOM Manipulation with Javascritpt (FreeCodeCamp))](https://www.youtube.com/watch?v=5fb2aPlgoys&t=1186s)

## DOM Manipulation
- 4 ways to get the HTML elements
   - `document.getElementById('id-from-html');` 
   - `document.getElementByClassName('class-from-html');`
   - `document.getElementByTagName('li');` - Examples: `li`, `ul` ...
   - `document.querySelector('div');` - Examples: `div`, `span`, ...
   - `document.querySelectorAll('div');` - Select all the `div` elements
- Then we can create a `const`:
    - `const title = document.querySelector('div');`
## GIVE STYLES (inline)
- Properties must be in `camelcase`: `fontSize`, not `font-size`, this is only on CSS.
- `title.style.color = 'red';` - `title` comes form the example above `const`  
- `title.style.fontSize = '2rem'` 
-  Inline styling cant be applied to more than one element.  To do it so, we have to list the items y hace un bucle:
```javascript
const listItems = document.querySelectorAll('.list-items')
listItems.style.fontsSize = '2rem'; //This wont style all the elements in the 'list-items' elements. Had to create a loop

for (i = 0; i < listItems.length; i++) {
  listItems[i].style.fontsSize = '2rem'
};
```
