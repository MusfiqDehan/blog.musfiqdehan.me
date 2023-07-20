---
title: "CRUD Operations in a JavaScript Array"
seoTitle: "CRUD Operations in a JavaScript Array"
seoDescription: "Read this article to understand CRUD Operations in a JavaScript Array"
datePublished: Fri Oct 21 2022 10:19:30 GMT+0000 (Coordinated Universal Time)
cuid: clkb04tnn000a09mu711yghc9
slug: crud-operations-in-a-javascript-array
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1689848092734/b5e0976e-272e-42ec-b45e-25aa5ec826b6.png
tags: javascript, array, musfiqdehan, crud-operations

---

CRUD stands for "Create, Read, Update, and Delete," and refers to the four basic operations you can perform on data in a database or data store. These operations can also be performed on arrays in JavaScript. Here's how you can perform each of these operations on an array.

## **Create (Add)**

To add an element to an array, you can use the `push()` method:

```javascript
Copy codelet fruits = ['apple', 'banana', 'orange'];

// Add a new element to the end of the array
fruits.push('mango');

console.log(fruits); // ['apple', 'banana', 'orange', 'mango']
```

You can also add an element to the beginning of the array using the `unshift()` method:

```javascript
Copy codelet fruits = ['apple', 'banana', 'orange'];

// Add a new element to the beginning of the array
fruits.unshift('pear');

console.log(fruits); // ['pear', 'apple', 'banana', 'orange']
```

## **Read (Retrieve)**

To retrieve an element from an array, you can use the array's index:

```javascript
Copy codelet fruits = ['apple', 'banana', 'orange'];

let firstFruit = fruits[0]; // 'apple'
let secondFruit = fruits[1]; // 'banana'
let thirdFruit = fruits[2]; // 'orange'
```

You can also use the `indexOf()` method to find the index of a specific element in the array:

```javascript
Copy codelet fruits = ['apple', 'banana', 'orange'];

let index = fruits.indexOf('banana'); // 1
```

## **Update (Modify)**

To update an element in an array, you can simply reassign the value at a specific index:

```javascript
Copy codelet fruits = ['apple', 'banana', 'orange'];

fruits[1] = 'pear';

console.log(fruits); // ['apple', 'pear', 'orange']
```

## **Delete (Remove)**

To remove an element from an array, you can use the `splice()` method:

```javascript
Copy codelet fruits = ['apple', 'banana', 'orange'];

// Remove the second element (index 1)
fruits.splice(1, 1);

console.log(fruits); // ['apple', 'orange']
```

You can also use the `shift()` method to remove the first element of the array, or the `pop()` method to remove the last element:

```javascript
Copy codelet fruits = ['apple', 'banana', 'orange'];

// Remove the first element
fruits.shift();

console.log(fruits); // ['banana', 'orange']

// Remove the last element
fruits.pop();

console.log(fruits); // ['banana']
```

## Conclusion

I hope after reading this article, you are clear about the CRUD operations in a JavaScript Array. If you have any questions or feedback, regarding this article, please let me know in the comment section. Thanks.