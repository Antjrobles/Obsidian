---
title: REACT
description: 'A React guide and notes'
created: 02-11-2022
tags:
- programing
- web
- javascript
---
# INTRODUCTION, LINKS AND GUIDES
- React is a JavaScript library for building user interfaces. It is commonly used for front-end development and helps developers create single page or mobile applications. React allows developers to create large web applications that can change data, without reloading the page. The main purpose of React is to be fast, scalable, and simple.
- [React](https://reactjs.org/)
- [EdRoh-Youtube]([EdRoh](https://www.youtube.com/@EdRohDev))

# MODULES OR PACKAGES
- [formik](https://formik.org/) - Formik is the world's most popular open source form library for React and React Native.
- [yup](https://www.npmjs.com/package/yup) - Yup is a JavaScript schema builder for value parsing and validation.
- [react-responsive-carousel](https://www.npmjs.com/package/react-responsive-carousel) - Powerful, lightweight and fully customizable carousel component for React apps.
- [React-Icons](https://react-icons.github.io/react-icons) - Include popular icons in your React projects easily with react-icons, which utilizes ES6 imports that allows you to include only the icons that your project is using.
- [react-toastify](https://www.npmjs.com/package/react-toastify) - 🎉 React-Toastify allows you to add notifications to your app with ease. No more nonsense! 

***
# METHODS
- `window.scrollTo(x-coord, y-coord)` - The **`scrollTo()`** method of the [`Element`](https://developer.mozilla.org/en-US/docs/Web/API/Element) interface scrolls to a particular set of coordinates inside a given element. [link](https://developer.mozilla.org/en-US/docs/Web/API/Element/scrollTo)
```javascript
element.scrollTo(0, 1000);

// another example

window.scrollTo({
  top: 100,
  left: 100,
  behavior: 'smooth'
});
```

# SYNTAX
- `? :` - Equivale a `if else`.
```javascript
funtction singleOrMArried() {
const married = true

if (married){ 
return <h1>Estoy casado</h1>
}
else {
return <h1>No estoy casasdo</h1>
};
// Se puede sustituir en React con
funtction singleOrMArried() {
const married = true
return <h1>{married ? 'Estoy Casado' : "no estoy casado"}</h1>
};
```


