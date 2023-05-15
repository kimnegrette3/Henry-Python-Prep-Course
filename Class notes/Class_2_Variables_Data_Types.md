# Chapter 2: Variables and Data Types

Created: April 27, 2023 5:35 PM
Reviewed: Yes
Type: Lecture

# Chapter 2: Variables and Data Types

In programming, data refers to the information that is used and manipulated by a program. It can be as simple as a single number or character or as complex as a database of information. Programs use data to perform operations, make decisions, and produce output.

Variables are used to store and manipulate data in a program. They can be thought of as containers that hold a particular value. When you define a variable, you give it a name, and assign a value to it using the equals sign (=). For example, to create a variable called `x` that holds the value `5`, you would write:

```python
x = 5

```

Variables in Python are dynamically typed, meaning you do not need to specify the data type of a variable when you define it. Instead, Python automatically determines the data type based on the value that is assigned to the variable. This can make programming in Python more flexible and efficient.

Python has several built-in data types that can be used to store different kinds of data. These include:

- Integers (int): whole numbers, like 5 or -3
- Floats (float): decimal numbers, like 3.14 or -0.5
- Strings (str): sequences of characters, like "hello" or "world"
- Booleans (bool): values that are either True or False

To specify the data type of a variable, you can use a type hint. Type hints are annotations that tell Python what type a variable should be. For example, to specify that a variable `x` should be an integer, you would write:

```python
x: int = 5

```

In addition to these built-in data types, Python also allows you to create your own custom data types using classes. Classes are a way of defining a new data type that has its own properties and methods.

Overall, understanding variables and data types is crucial for writing Python programs that can store and manipulate information effectively. By using the correct data types and variables, you can write programs that are more efficient, easier to read and maintain, and less prone to errors.

## Operations between variables in Python

In Python, you can perform various operations between different variables. Some common operations include:

- Addition (+): adds two values together
- Subtraction (-): subtracts one value from another
- Multiplication (*): multiplies two values
- Division (/): divides one value by another
- Modulo (%): returns the remainder of a division operation
- Exponentiation (**): raises one value to the power of another

Here are some examples:

```python
# Addition
x = 5
y = 3
z = x + y
print(z)  # Output: 8

# Subtraction
x = 5
y = 3
z = x - y
print(z)  # Output: 2

# Multiplication
x = 5
y = 3
z = x * y
print(z)  # Output: 15

# Division
x = 5
y = 3
z = x / y
print(z)  # Output: 1.6666666666666667

# Modulo
x = 5
y = 3
z = x % y
print(z)  # Output: 2

# Exponentiation
x = 5
y = 3
z = x ** y
print(z)  # Output: 125

```

By using these operations, you can perform complex calculations and manipulate data in your Python programs.

In Python, you can also perform some operations between string data. Here are some examples:

```python
# Concatenation (+)
str1 = "Hello"
str2 = "world"
str3 = str1 + " " + str2
print(str3)  # Output: "Hello world"

# Repetition (*)
str1 = "Hello"
str2 = str1 * 3
print(str2)  # Output: "HelloHelloHello"

# Indexing and Slicing
str1 = "Hello"
print(str1[0])  # Output: "H"
print(str1[1:3])  # Output: "el"

# Length
str1 = "Hello"
print(len(str1))  # Output: 5

```

Note that you cannot perform mathematical operations like addition or subtraction between strings.

You can convert a variable from one data type to another using type conversion functions. The most common type conversion functions in Python are `int()`, `float()`, `str()`, and `bool()`. Here are some examples:

```python
# Converting a string to an integer
x = "5"
y = int(x)
print(y)  # Output: 5

# Converting a string to a float
x = "3.14"
y = float(x)
print(y)  # Output: 3.14

# Converting a number to a string
x = 5
y = str(x)
print(y)  # Output: "5"

# Converting a boolean to a string
x = True
y = str(x)
print(y)  # Output: "True"

# Converting a string to a boolean
x = "True"
y = bool(x)
print(y)  # Output: True

```

Note that not all conversions are possible. For example, you cannot convert a string containing letters to an integer or float. In addition, some conversions may result in loss of precision or information, such as when converting a float to an integer.

It is also important to note that not all data types can be compared or used together in the same operation. For example, you cannot add a string and an integer together. In such cases, you may need to convert one of the values to a compatible data type before performing the operation.

## Notebooks vs Scripts

Using a script or a notebook for writing code in Python has its own advantages and disadvantages.

A script is a standalone file that contains a set of instructions written in Python. It can be executed from the command line or an IDE (integrated development environment) to perform a specific task. A script is useful when you want to automate a process or perform a task repeatedly.

On the other hand, a notebook is an interactive document that allows you to combine code, text, and visualizations in a single document. Notebooks are useful when you want to explore data, create visualizations, or share your work with others. Notebooks are also useful for teaching purposes as they allow students to follow along with the code and see the results in real-time.

Here are some pros and cons of each one:

**Scripts**

- Pros:
    - Easy to automate a process or perform a task repeatedly
    - Can be executed from the command line or an IDE
    - Good for large codebases and complex projects
- Cons:
    - Can be difficult to debug and test
    - Lack of interactivity and visualizations
    - Not ideal for exploring data or sharing work with others

**Notebooks**

- Pros:
    - Interactive and allows you to combine code, text, and visualizations in a single document
    - Ideal for exploring data and creating visualizations
    - Good for teaching purposes
- Cons:
    - Not as easy to automate a process or perform a task repeatedly
    - Can be slow when dealing with large codebases and complex projects
    - Can be difficult to share with others who do not have access to the same notebook environment

In general, scripts are better suited for automating repetitive tasks and working on large codebases and complex projects. Notebooks are better suited for exploratory data analysis, creating visualizations, and sharing work with others.