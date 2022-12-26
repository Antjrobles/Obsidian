---
title: "Nodejs"
description: "A guide of Nodejs"
created: 07-07-2022
tags:
- programming
- javascript
- nodejs
---
# NODEJS

## <mark style="background: #291d58;">INSTALLATION ON DEBIAN</mark>

- <mark style="background: #BBFABBA6;">Method 1</mark>: Install Node.js and npm from Debian Repository

  - `sudo apt install nodejs npm`
  - `node -v` - will show the version
  - `npm -v` - will show the npm version

- <mark style="background: #BBFABBA6;">Method 2</mark>: Install Node.js and npm from NodeSource
  - `sudo curl -sL https://deb.nodesource.com/setup_16.x | sudo bash -` - the NodeSource repository provides v17, v16, v14, and v12 versions.
  - `sudo apt install nodejs`
  - `node -v`
  - `npm -v`
---

##  <mark style="background: #291d58;">LINKS TO COURSES AND TUTORIALS
</mark>
- [Node.js y Express - FreeCodeCamp](https://www.youtube.com/watch?v=1hpc70_OoAg&t=3528s)

## INSTALL PACKAGES OR DEPENDCIES
- `npm install package_name` - If flag `-D` is added, means is installed as `Desarrollo` o `Development`. 

---


## <mark style="background: #291d58;">IMPORT - EXPORT</mark>
#### <mark style="background: #BBFABBA6;">EXPORT</mark>
- `module.exports.nameOfTheFuncionToExport = nameOfTheFunctionToExport`
```javascript
module.exports.myFunction = myFunction;
```
- You can give any name to `myFunction (eg. module.exports.x = myFunction)`  on the left side of the expression, but is a good idea to give it the same name of the function, because this is how its going to be exported.
#### <mark style="background: #BBFABBA6;">IMPORT</mark>
- For convection, its  common to use a `const` 
- For convection, use the same name of the module we want to import
```javascript
const variableName = require("./route-to-module");

#example from the tutorial
const saludo = require("./saludo.js")
```
- To call the module we have to "call" it.
```javascript
console.log(variableName.importedFunction);

#example from the tutorial
console.log(saludo.saludar);
```
#### EXPORT MORE THAN ONE FUNCTION
- Can add another `modue.exports.` or create an object:
```javascript
module.exports = {
  saludar: saludar,
  saludarHolaMundo: saludarHolaMundo
};
```

####  IMPORT ONLY THE MODULE WE WANT
```javascript
const { functionToImport } = require("./route-to-file.js");
```
or, to import more than one:

```javascript
const { function1, function2 } = require("./route-to-file.js");
```
- With this syntax we can ommit call the module:
```javascript
console.log(function1, function2);
```
---

## <mark style="background: #291d58;">MODULES BUILT-IN</mark>
- `http, https, fs (file system), os (operating system), path...`
#### CONSOLE
- Built-in module that implements some functions like the web console.
    * `console.log()` - print in the console
    * `console.warn()` - print a warning
    * `console.error()` - show an error message with addtional info.
    * `console.assert()` 
    * `console.table()` - print the info formatted as  a table.



#### PROCESS
- Give information about the process that is running and give us some control over it.

***
## <mark style="background: #291d58;">LOCAL MODULES</mark>
- Modules created user locally
- Commonjs: A module in CommonJS is a JavaScript file that exports one or more values, which can be imported and used by other JavaScript code. This allows you to write modular and reusable code that can be shared between different parts of your application.
- to import a funcion from another file use `require`.

```node
// my-other-file.js

// Import the doSomething() function from the my-module.js file
var doSomething = require("./my-module").doSomething;

// Use the doSomething() function in our code
doSomething();
```




