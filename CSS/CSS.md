---
title: "CSS"
description: "Programming language to style HMTL"
created: 27-10-2022
tags:
  - css
  - Programming
  - bootstrap
  - tailwind
---

# INTRODUCION AND LINKS

- Cascading Style Sheets (CSS) is a style sheet language used for describing the presentation of a document written in a markup language such as HTML. CSS is a cornerstone technology of the World Wide Web, alongside HTML and JavaScript.

## FRAMEWORKS DE CSS

- [Bootstrap](https://getbootstrap.com/)
- [Tailwind](https://tailwindcss.com/)
- [Bulma](https://bulma.io/)

````ad-note
icon: css3-alt
collapse: true
color: 26, 41, 206

- Cargar siempre los estilos CSS dentro de la etiqueta  `<head></head>`,  asi cargará la página más rapido.
- Para cargar una hoja de estilos  se utiliza la etiqueta  \<link>
```css
`<link rel="stylesheet" href="styles.css" type="text/css">`
````

## SOME NOTES AND TIPS

- SOME GOOGLE FONTS:
  - `CINZEL`
  - `PLAYFAIR`
  - `FAUNA ONE`

## PROPIEDADES

- `color`: para indicar el color de la fuente;
- para seleccionar un `id=""` - se utiliza `#/nombre_del_id { }`
- para seleccionar una clase `class=""` - se utiliza el punto `.nombre_de_class { }`

### TEXT PROPERTIES

- `writing-mode:` - The `writing-mode` property specifies whether lines of text are laid out horizontally or vertically.

```css
writing-mode: vertical-lr; /* will display the text vertically */
```

## REGLAS

- `@apply` - La regla CSS `@apply` permite a un autor almacenar un conjunto de declaraciones CSS en una variable `de autor` (a named variable), para a continuación, hacer referencia a ellas (incluirlas) en otras reglas de estilo. Por ejemplo:

```css
.app {
  height: 100%;
  background-color: #010026;
  @apply text-white; /* Detault color of the text is going to be white */
}
```
