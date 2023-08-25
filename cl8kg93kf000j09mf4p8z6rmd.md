---
title: "Adding Items in a JavaScript Array"
seoTitle: "Adding Items at Start, Middle, and End of a JavaScript"
seoDescription: "In this article, we will learn how we can add items at the start/beginning, middle, and end of a JavaScript Array."
datePublished: Tue Sep 27 2022 17:05:26 GMT+0000 (Coordinated Universal Time)
cuid: cl8kg93kf000j09mf4p8z6rmd
slug: adding-items-in-a-javascript-array
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1664294709712/pJg_xuqvO.png
tags: javascript, array, array-methods

---

The array is one of the essential Data Structures. In JavaScript, we have many built-in Array methods to manipulate an array. In this article, we will learn how we can add items at the **start**, **middle**, and **end** of a JavaScript Array. 

## Declaring an empty Array

```javascript
// We can declare an array using Array() constructor function
const arr = new Array();
// or Simply using an empty square bracket
const arr = [];
```

## Initializing an Array

```javascript
//  Initializing the array with two integers 3, 4
const arr = new Array(3, 4);
// or
const arr = [3, 4];
```
Now let's add items to this array.

## Adding items at the beginning/start
- We will use the `unshift()` method for doing this
- You can add any number of items
- You can add not only numbers but also different types of elements other than numbers

```javascript
arr.unshift(1, 2)
// [1, 2, 3, 4]
```
## Adding items in the middle
- It is slightly tricky😉 but not much complex
- Our current Array,  `const arr = [1, 2, 3, 4];`
- We want to add 7 and 8 in between 2 and 3
- We will use the `splice()` function for this
- `splice()` function takes 3 parameters
-  **First Parameter:** Before which position do we want to add
- **Second Parameter:** How many numbers do we want to delete (We will not use this parameter as we don't want to delete any number now)
- **Third Parameter:** The items we want to add in the middle
- So, we will keep our second parameter as 0
- After that, we will add the elements we want to add in the middle
- `splice(2, 0, 7, 8)`
- Before 3, the index of 3 is 2
- 0 as Second Parameter as we don't want to do any delete operation
- We want to add 7, 8 that's why we adding 7, 8 as the last parameter
- You can add as many items as you want
- You can add not only numbers but also different types of elements other than numbers

```javascript
arr.splice(2, 0, 7, 8);
// Now, the new resultant array will be
// [1, 2, 7, 8, 3, 4]
```

## Adding elements at the end of the array

- This one is simple
- We will use `push()` operation
- You can add any number of items
- You can add not only numbers but also different types of elements other than numbers

```javascript
arr.push(5, 6);
// Now, the new resultant array will be
// [1, 2, 7, 8, 3, 4, 5, 6]
```
## All at once
Now let's summarize the article with a single code snippet.

```javascript
// Declaring an array
const arr = [];
console.log(arr);
// []

# Intializing an array
arr = [3, 4];
console.log(arr);
// [3, 4];

// Adding items at the beginning/ start of the array
arr.unshift(1, 2)
console.log(arr);
// [1, 2, 3, 4]

// Adding items in the middle of the array
arr.splice(2, 0, 7, 8);
console.log(arr);
// [1, 2, 7, 8, 3, 4]

// Adding items at the end of the array
arr.push(5, 6);
console.log(arr);
// [1, 2, 7, 8, 3, 4, 5, 6]

```
Thank you so much for reading this. Hope to see you in another article. This is my first published article. Please give me a like for the inspiration.

You can also read this article in my Twitter Thread. Don't forget to follow me on Twitter. Thanks again.

%[https://twitter.com/MusfiqDehan/status/1568235913821716487]