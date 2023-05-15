# Chapter 6: Functions

Created: May 4, 2023 4:15 PM
Reviewed: Yes
Type: Lecture

# Chapter 6: Functions

Functions are an essential component of programming as they allow us to break down complex tasks into smaller, more manageable pieces of code. In Python, functions are defined using the "def" keyword followed by the function name and any necessary parameters enclosed in parentheses.

Here's an example of a simple function that takes in two parameters and returns their sum:

```python
def add_numbers(x, y):
    sum = x + y
    return sum

```

To use this function, we can call it by its name and pass in the required parameters:

```python
result = add_numbers(2, 3)
print(result)

```

This will output "5" to the console.

Functions can also have optional parameters and default values. For example:

```python
def greet(name, greeting='Hello'):
    print(greeting + ', ' + name + '!')

```

In this case, the "greeting" parameter is optional and has a default value of "Hello". If we call the function with only the "name" parameter, the default greeting will be used:

```python
greet('John') # outputs "Hello, John!"

```

Finally, functions can also return multiple values using tuples:

```python
def get_name_and_age():
    name = 'Alice'
    age = 25
    return name, age

```

We can then assign the returned values to separate variables:

```python
name, age = get_name_and_age()
print(name) # outputs "Alice"
print(age) # outputs 25

```

By using functions, we can make our code more modular, easier to read and maintain, and less prone to errors.

## Namespace

Functions in Python have their own namespace, which is a space where variables and names defined within a function are separate from those defined outside of the function. This means that you can define variables within a function that have the same name as variables defined outside of the function, and they will not interfere with each other.

For example, consider the following code:

```python
x = 10

def my_func():
    x = 5
    print(x)

my_func()
print(x)

```

In this case, we have a variable `x` defined outside of the function `my_func` with a value of `10`. Within the function, we define another variable `x` with a value of `5`. When we call `my_func()`, it will print `5`, since that is the value of `x` within the function. However, when we print `x` outside of the function, it will still print `10`, since that is the value of `x` outside of the function.

This separation of namespaces allows for better organization and modularity in our code. However, it is important to be aware of variable scope when working with functions to avoid unexpected behavior.

It is also worth noting that functions can access variables defined outside of the function, but they cannot modify them unless they are declared as `global` or `nonlocal`. This means that if you define a variable outside of a function and then pass it as a parameter to the function, any changes made to the variable within the function will not affect the original variable outside the function, unless you declare it as `global` or `nonlocal`.

In conclusion, by using functions in Python and understanding their namespace, we can make our code more modular, easier to read and maintain, and less prone to errors.

## Recursiveness

Recursive functions are functions that call themselves within their own definition. They can be used to solve problems that can be broken down into smaller sub-problems.

For example, here's a simple recursive function that calculates the factorial of a number:

```python
def factorial(n):
    if n == 1:
        return 1
    else:
        return n * factorial(n-1)

```

This function takes a number `n` and returns the factorial of that number. The factorial of a number is the product of all positive integers up to and including that number.

The function works by checking if `n` is equal to 1. If it is, it returns 1 (since the factorial of 1 is 1). Otherwise, it multiplies `n` by the result of calling the factorial function with `n-1` as the argument. This continues until `n` is equal to 1, at which point the function returns 1 and the recursion stops.

Recursive functions can be a powerful tool in programming, but they can also be tricky to understand and debug. It's important to make sure that recursive functions have a base case (like the `n == 1` check in the factorial function) that will eventually be reached, otherwise the function will keep calling itself indefinitely and cause an error.

Here's another example of a recursive function that calculates the nth Fibonacci number:

```python
def fibonacci(n):
    if n <= 1:
        return n
    else:
        return fibonacci(n-1) + fibonacci(n-2)

```

This function takes a positive integer `n` and returns the nth number in the Fibonacci sequence. The Fibonacci sequence is a series of numbers in which each number is the sum of the two preceding numbers, starting from 0 and 1.

The function works by checking if `n` is less than or equal to 1. If it is, it returns `n` (since the first two numbers in the Fibonacci sequence are 0 and 1). Otherwise, it returns the sum of calling the `fibonacci` function with `n-1` as the argument (which will return the `n-1`th Fibonacci number) and calling the `fibonacci` function with `n-2` as the argument (which will return the `n-2`th Fibonacci number). This continues until the base case of `n <= 1` is reached, at which point the recursion stops and the function returns the desired Fibonacci number.

Recursive functions can be a powerful tool in programming, but they can also be tricky to understand and debug. It's important to make sure that recursive functions have a base case that will eventually be reached, otherwise the function will keep calling itself indefinitely and cause an error.

## Parameter passing

### By value:

When variables are passed as parameters to a function, a copy of the variable is created and passed to the function. This means that any changes made to the variable within the function only affect the copy of the variable within the function, and not the original variable outside of the function. If you want to modify the original variable from within the function, you need to declare it as `global` or `nonlocal`. Otherwise, any changes made to the variable within the function will not affect the original variable outside of the function.

### By reference:

When a complex object such as a list is passed as a parameter to a function, a reference to the object is passed instead of a copy. This means that any modifications made to the object within the function will affect the original object outside of the function. For example:

```python
def modify_list(my_list):
    my_list.append(4)
    return my_list

original_list = [1, 2, 3]
modified_list = modify_list(original_list)
print(modified_list) # outputs [1, 2, 3, 4]
print(original_list) # outputs [1, 2, 3, 4]

```

In this case, the `modify_list` function takes a list as a parameter, appends the value `4` to the list, and returns the modified list. When we call the function with `original_list` as the argument, it modifies the original list and returns the modified list. When we print both `modified_list` and `original_list`, we can see that they both contain the value `[1, 2, 3, 4]`.

It's important to be aware of parameter passing in Python to avoid unexpected behavior when working with functions.

## Lambda function

A lambda function is a small, anonymous function in Python that can have any number of arguments, but can only have one expression. They are defined using the "lambda" keyword, followed by the function's arguments and the expression to be evaluated.

Here's an example of a lambda function that takes in a number and returns its square:

```python
square = lambda x: x ** 2
print(square(2)) # outputs 4

```

Lambda functions are often used as a way to create simple, one-line functions without having to define a named function. They are particularly useful when you need to pass a function as an argument to another function, such as the `map()` or `filter()` functions.

For example, here's how you could use a lambda function with the `map()` function to apply a function to each element of a list:

```python
numbers = [1, 2, 3, 4, 5]
squares = list(map(lambda x: x ** 2, numbers))
print(squares) # outputs [1, 4, 9, 16, 25]

```

In this case, the lambda function `lambda x: x ** 2` is passed as the first argument to the `map()` function. The `map()` function applies the lambda function to each element of the `numbers` list and returns a new list containing the results.

Lambda functions can also be used with the `filter()` function to filter out elements from a list based on a certain condition:

```python
numbers = [1, 2, 3, 4, 5]
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers) # outputs [2, 4]

```

In this case, the lambda function `lambda x: x % 2 == 0` is passed as the first argument to the `filter()` function. The `filter()` function applies the lambda function to each element of the `numbers` list and returns a new list containing only the elements for which the lambda function returns `True` (in this case, the even numbers).

Lambda functions can be a powerful tool in Python, but they should be used judiciously. While lambda functions can make code more concise and readable, they can also make code more difficult to understand and debug if used excessively. In general, lambda functions are best used for simple, one-line functions that are used only once or twice in a program.