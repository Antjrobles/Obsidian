---
title: "VsCode"
description: "Shortcuts and plugins for VsCode"
tags:
- vscode
- plugins
---
## OPTIONS TO ACTIVATE IN VsCode
- `sticky scroll`   -  [Sticky Scroll](https://www.youtube.com/watch?v=gtAl-6AqxIQ&t=54s)
 ***
## PLUGINS & CONFIG

- <mark style="background: #BBFABBA6;">SAVE CODE < ></mark>
	
	-    <u>How to use</u>:
	
		-   Select text and then right-click `Save snippet` to save.
		-   View and search saved snippets inside VS Code. In list or grid view.
		-   Share your snippets in the web app via a URL, HTMl iFrame, a photo, or on Medium & WordPress.

    - <u>Keyboard shortcuts</u>
        - Save selected snippets (MAC) - `cmd + 8` 
        - View all snippets (MAC) - `cmd + shift + 8`


- <mark style="background: #BBFABBA6;">TAILWIN CSS INTELLISENSE & TAILWIND DOCUMENTATION</mark>
  - In Vscode press `cmd + ctrl + t` and a Tailwind documentation window will pop up.
- <mark style="background: #BBFABBA6;">TAILWIND SHADES</mark>
  - Usage:
    - macOS: `cmd + k` `cmd + g`
    - Other: `ctrl + k` `ctrl + g`

- <mark style="background: #BBFABBA6;">GRAMMARLY</mark> (for MD and TXT)

- <mark style="background: #BBFABBA6;">CODE SPELL CHECKER</mark>
  - After positioning the cursor in the word, any of the following should display the list of suggestions:

  - Click on the 💡 (lightbulb) in the left hand margin.
-   [`Quick Fix`](https://code.visualstudio.com/docs/getstarted/keybindings#_rich-languages-editing "https://code.visualstudio.com/docs/getstarted/keybindings#_rich-languages-editing") Editor action command:
    -   Mac: `⌘`+`.`
    - To avoid `lorem` issues, in `settings` search `cSpell.language`  and add `lorem`.


- <mark style="background: #BBFABBA6;">HIGHLIGHT MATCHING TAG</mark>
  - Support HTML and JSX
  - Styling options, add this to settings.json:
```json
"highlight-matching-tag.styles": {
  "opening": {
    "name": {
      "underline": "yellow"
    }
  }
}
```

- <mark style="background: #BBFABBA6;">SMART SEMICOLON</mark>


- <mark style="background: #BBFABBA6;">CONVENTIONAL COMMITS</mark>
  - [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)
  - [Carlos Azaustre Guide](https://www.youtube.com/watch?v=SigVVJmUGv8&t=54s)
  - `cmd + shift + p` - Type `conventional Commits` and follow the instrucctions.
- <mark style="background: #BBFABBA6;">IMAGE PREVIEW</mark>
- <mark style="background: #BBFABBA6;">INDENT BLOCK HIGHLIGHTING</mark>
- <mark style="background: #BBFABBA6;">SVG PREVIEW</mark>


***
# TO ADD IN SETTINGS.JSON
```json
"editor.guides.bracketPairs": true,  //Line inside Bracket
"editor.guides.bracketPairsHorizontal": true,
"editor.guide.highlightActiveIndentation": true,
"editor.lineDecorationsWidth": 10,
"typescript.validate.enable": false, //ADDED BY ME TO AVOID JS WARNINGS
"javascript.validate.enable": false, //ADDED BY ME TO AVOID JS WARNINGS
"javascript.suggest.autoImports": true, //Autosuggest Imports
```

***
# HOT KEYS

- `cmd + x` - eliminar línea
- `shfit + alt + up or down arrow` - duplica línea seleccionada
- `Tecla Mayúsculas + alt + up or down arrow` -  mueve línea seleccionada arriba o abajo
- `cmd + k, cmd + c` - comentar una linea.
- `cmd + shift + /` - comment-uncomment line
- `cmd + ,` - Open settings
- `ctrl + `` - Open new terminal
- `ctrl + tab` - switch tabs
- `ctrl + b``  - collapse  main sidebar
-  `shift + cmd + e` - switch cursos to main sidebar 

- `tab`  - when line or lines selected, then indent right. To indent left: `shift + tab` , in that order.
- `shitf alt f` - Format Document.
- `cmd + shift + l` - To select all the same occurrences. Another options is `cmd + d`.
- `alt + click` - select multiple places.

