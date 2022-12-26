---
title: "Javascript - Arrays"
description: "Arrays in Javascript"
created: 28-06-2022
tags:
- javascript
- programming
- arrays
---



# ARREGLOS o ARRAYS

- Los arrays o arreglos van entre corchetes `[]`
- Los objetos siempre van entre corchetes `{}`


## METHODS


### <u>Acceder a un elemeto dentro de un array</u>
``` javascript
const numeros = [10, 20, 30, 40, 50];
const meses = ["Enero", "Febrero", "Marzo", "Abril", "Mayo", "Junio", "Julio"];

console.table(numeros[2]); // Print number 30. Is the element number 2. Arrays start_at 0.
console.table(numeros[3]); // Print  number 40
console.table(numeros[4]); // Print  numbers 50
```

---
####  <u>List all the elements of an array`for.Each`</u>

``` javascript
numeros.forEach( function(numeros) {
     console.log(numeros)
});
```


#### <u>Saber la longitud de un arrays.`length`</u>
`console.log(numeros.length);`

#### <u>Add elements to an array.`push` and `unshift`</u>
-  <mark>Metodo 1 (Poco común)</mark>
`numeros[6] = 60;` -  introducir numero del ultimo elemento del array [6]
`meses[7] = "Agosto";`
 - <mark>Metodo 2</mark>
`numeros.push(100);` -  Agrega un elemento al final del array. No es necesario saber cuantos elementos hay.
`meses.push("Diciembre");`
 - <mark>Metodo 3</mark> 
`numeros.unshift(1, 2, 3);`  - `unshift` agrega elementos al principio del array.

####  <u>To delete elements inside an array.`pop` and `shift`</u>
`numeros.pop();`  - `pop()` delete the last element
`meses.pop();`  

`numeros.shift();`  - `shift` delete the first element

`meses.splice(2, 1);`   - `splice` delete the element number 2 of the array and only 1 element. 
`meses.splice(2, 3);` - delete pos 2 and the 3 subsequent elements.

## REST OPERATOR o SPREAD OPERATOR (recommended method)

`const nuevosMeses = [...meses, "Junio"];` -  copy the `const` and the added the new element at the end.
`const nuevosNumeros = [-10, ...numeros];`  - add element at the beginning. 


### <u>Find elements inside an array.`find()`</u>
- [find](https://www.youtube.com/watch?v=t9Hw86Vc-gU)

```javascript
const numbers = [10, 20, 30, 40, 50];

const greaterThan25 = numbers.find(num => num > 25);

console.log(greaterThan25); // 30

// To locate the element inside the array
console.log ( numbers.indexOf(greaterThan25) ); // 2
```

### <u>Sort elements inside an array.`sort()`</u>
- [sort](https://www.youtube.com/watch?v=d0_9rc8mF4g)
```javascript
const months = ["May", "June", "April", "November"];
console.log( months.sort() ); //["April","June","May","November"]. Alphabetically

// whith number, from lowest to higher but taking the first number of the element
const numbers = [100, 2, 55, 10, 77];
console.log(numbers.sort()); //[10, 100, 2, 55, 77];

// To order from lowest to higher
const numbers = [100, 2, 55, 10, 77];
const numbersInOrder = numbers.sort((a, b) => a - b);
console.log(numbersInOrder);
```
- To sort objects inside an array check the link above.



