# Functions in Python

In this article, we will learn about functions using Python Programming Language.

## What is a function?

Functions are

* **Self-contained** modules of code that accomplish a specific task.
    
* Functions usually **take in** data, process it, and **return** a result.
    
* Once a function is written, it can be used over and over and over again.
    
* Functions can be **called** from the inside of other functions.
    

Suppose we want to add two numbers.

```python
a = 10
b = 20
print(a + b)
```

We want to add two different numbers again like

```python
x = 5
y = 7
print(x + y)
```

Now by using the function, we can reduce this repetition:

```python
def add_two_numbers(a, b):
	return a + b
	
print(add_to_numbers(10, 20))
print(add_to_numbers(5, 7))
```

In this simple program, we reduce 6-4=2 lines by using a function. If we use functions for large programs, the reduction of the lines will be more.

## Types of Functions

In python, we have two types of functions.

1. Build-In Function
    
2. User-Defined Functions
    

## 1\. Built-In Function

Python has many built-in functions that allow you to perform common tasks without writing your own code. Here are some examples of built-in functions in Python:

* `print()`: Prints a string to the console.
    
* `len()`: Returns the length of a string, list, tuple, or dictionary.
    
* `max()`: Returns the maximum value from a list or tuple.
    
* `min()`: Returns the minimum value from a list or tuple.
    
* `sum()`: Returns the sum of all elements in a list or tuple.
    
* `abs()`: Returns the absolute value of a number.
    
* `type()`: Returns the data type of a value.
    

For example:

```python
# Print a string
print("Hello, World!")

# Get the length of a string
string_length = len("Hello, World!")
print(string_length)  # Output: 12

# Get the maximum value from a list
numbers = [1, 2, 3, 4, 5]
max_number = max(numbers)
print(max_number)  # Output: 5

# Get the minimum value from a tuple
numbers = (1, 2, 3, 4, 5)
min_number = min(numbers)
print(min_number)  # Output: 1

# Get the sum of a tuple
numbers = (1, 2, 3, 4, 5)
total = sum(numbers)
print(total)  # Output: 15

# Get the absolute value of a number
number = -5
abs_number = abs(number)
print(abs_number)  # Output: 5

# Get the data type of a value
value = 5
data_type = type(value)
print(data_type)  # Output: <class 'int'>
```

You can find a complete list of Python's built-in functions in the official Python documentation.

## 2\. User-Defined functions

You can define your own functions in Python using the `def` keyword. Here is an example of a simple function that takes two arguments and returns their sum:

```python
def sum(a, b):
  result = a + b
  return result

print(sum(1, 2))  # Output: 3
```

The function `sum()` has two parameters, `a` and `b`, and a return statement that returns the sum of `a` and `b`. You can call the function by providing values for the arguments in the parentheses after the function name. In this example, the function is called with the arguments `1` and `2`, and the output is `3`.

You can also define default values for the arguments in the function definition. If an argument is not provided when the function is called, the default value is used instead. Here is an example:

```python
def sum(a, b=0):
  result = a + b
  return result

print(sum(1))  # Output: 1
print(sum(1, 2))  # Output: 3
```

In this example, the function `sum()` has a default value of `0` for the argument `b`. If you call the function with only one argument, like `sum(1)`, the value of `b` will be `0` and the output will be `1`. If you call the function with two arguments, like `sum(1, 2)`, the default value is overridden, and the output is `3`.

Thanks for reading this article. Hope you have got some idea about functions using python. We will discuss other topics about python in another article. Till then, keep learning and keep growing.