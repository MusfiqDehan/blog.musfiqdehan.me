---
title: "Pass by Value vs Pass by Reference"
seoTitle: "Pass by Value vs Pass by Reference"
seoDescription: "When a piece of data is passed to a function or method, there are two main ways in which it can be passed: pass by value and pass by reference"
datePublished: Mon Mar 20 2023 10:08:07 GMT+0000 (Coordinated Universal Time)
cuid: clfgnynga000409l83smffyw7
slug: pass-by-value-vs-pass-by-reference
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1679306660110/44c9fa6d-54c9-4e32-a63d-706ba18a8e3e.png
tags: javascript, python, computer-science, pass-by-value, pass-by-reference

---

In computer programming, when a piece of data is passed to a function or method, there are two main ways in which it can be passed: pass by value and pass by reference.

## **Pass by Value**

In pass by value, the value of the argument is passed to the function or method. This means that if the function or method modifies the value of the argument, the original value of the argument is not changed. This is because the function or method is working with a copy of the original value, rather than the original value itself.

Here is an example of pass by value in C++:

```cpp
#include <iostream>
using namespace std;

void increment(int x) {
    x++;
}

int main() {
    int y = 5;
    increment(y);
    cout << y << endl; // Outputs 5
    return 0;
}
```

In this example, the `increment` function takes an `int` argument `x` and increments it by 1. However, when we call the `increment` function with the value of `y`, the value of `y` is not modified because the function is working with a copy of the value of `y`.

Here is an example of pass by value in Python:

```python
def increment(x):
    x += 1

y = 5
increment(y)
print(y)  # Outputs 5
```

And here is an example of pass by value in JavaScript:

```javascript
function increment(x) {
    x++;
}

let y = 5;
increment(y);
console.log(y);  // Outputs 5
```

## **Pass by Reference**

In pass by reference, the reference (or memory address) of the argument is passed to the function or method. This means that if the function or method modifies the value of the argument, the original value of the argument is also changed. This is because the function or method is working with the original value itself, rather than a copy of the value.

Here is an example of pass by reference in C++:

```cpp
#include <iostream>
using namespace std;

void increment(int &x) {
    x++;
}

int main() {
    int y = 5;
    increment(y);
    cout << y << endl; // Outputs 6
    return 0;
}
```

In this example, the `increment` function takes an `int` argument `x` and increments it by 1. When we call the `increment` function with the value of `y`, the value of `y` is modified because the function is working with the original value of `y`, rather than a copy.

Here is an example of pass by reference in Python:

```python
def increment(x):
    x[0] += 1

y = [5]
increment(y)
print(y)  # Outputs [6]
```

And here is an example of pass by reference in JavaScript:

```javascript
function increment(x) {
    x++;
}

let y = 5;
increment(y);
console.log(y);  // Outputs 6
```

It's important to note that in some languages, such as **Python** and **JavaScript**, all arguments are passed by reference.