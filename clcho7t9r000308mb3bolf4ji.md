# Deleting Items from a JavaScript Array

In this article, we will discuss how we can delete or remove items from the start, middle, and end of a JavaScript Array.

## Taking an Array

First, let's take an array name `fruits`.

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];
```

Now we will see different approach of removing/deleting items from this array.

## Removing item from Beginning

To remove an item from the beginning of an array, you can use the `shift()` method, which removes the first element of the array and returns it. For example:

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];

// Remove the first item from the array
var first = fruits.shift();

// The array now contains ["Orange", "Apple", "Mango"]
// The variable "first" contains the removed element: "Banana"
```

## Removing Item from the Middle

To remove an item from the middle of an array, you can use the `splice()` method, which allows you to specify the index at which to begin removing elements and the number of elements to remove. For example:

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];

// Remove the second item (index 1) from the array
var removed = fruits.splice(1, 1);

// The array now contains ["Banana", "Apple", "Mango"]
// The variable "removed" contains the removed element: "Orange"
```

## Removing Item from the End

To remove an item from the end of an array, you can use the `pop()` method, which removes the last element of the array and returns it. For example:

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];

// Remove the last item from the array
var last = fruits.pop();

// The array now contains ["Banana", "Orange", "Apple"]
// The variable "last" contains the removed element: "Mango"
```

You can also use the `slice()` method to remove items from an array without modifying the original array. This method allows you to specify a range of elements to include in a new array. For example:

```javascript
var fruits = ["Banana", "Orange", "Apple", "Mango"];

// Create a new array with the second and third items of the original array
var removed = fruits.slice(1, 3);

// The original array remains unchanged: ["Banana", "Orange", "Apple", "Mango"]
// The new array contains the removed elements: ["Orange", "Apple"]
```

## Note

It's important to note that the `splice()`, `shift()`, and `pop()` methods modify the original array, whereas the `slice()` method creates a new array. This means you need to use a different approach depending on whether you want to modify the original array or create a new one.

Thanks for reading this article. We will discuss another topic in another article.