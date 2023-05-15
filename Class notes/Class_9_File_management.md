# Chapter 9: File management

Created: May 5, 2023 10:12 PM
Reviewed: Yes
Type: Lecture

# File management

File management is an essential aspect of programming that involves reading, writing, and manipulating files. In Python, external data refers to any data that is stored outside of the program's code, such as text files, CSV files, JSON files, and more.

To work with external data in Python, you first need to open the file using the built-in `open()` function. This function takes two arguments: the path to the file and the mode in which you want to open the file (read, write, append, etc.).

After opening the file, you can use various methods to read or write data to the file. For example, the `read()` method can be used to read the contents of a file, while the `write()` method can be used to write data to a file.

It's important to properly close the file after you're done working with it using the `close()` method. Alternatively, you can use the `with` statement to automatically close the file once you're done working with it.

In summary, external data in Python refers to any data that is stored outside of the program's code, and working with external data involves opening, reading, writing, and manipulating files using various methods and functions.

### in/out

`input()` is a built-in Python function that allows the user to input data from the console. It takes a string as an argument, which is used as a prompt for the user to enter data. Here's an example:

```
name = input("Enter your name: ")
print("Hello, " + name)

```

In this example, the `input()` function prompts the user to enter their name, and the user's input is stored in the `name` variable. The `print()` function is then used to output a greeting to the console.

`print()` is another built-in Python function that is used to output data to the console. It takes one or more arguments, which can be of any data type, and outputs them to the console. Here's an example:

```python
x = 10
y = 20
print("The sum of", x, "and", y, "is", x + y)

```

In this example, the `print()` function is used to output a sentence to the console that includes the values of the variables `x` and `y`, as well as their sum.

`print()` can also be used to format output using placeholders. For example, the following code uses the `%` operator to insert values into a string:

```python
name = "John"
age = 30
print("My name is %s and I'm %d years old" % (name, age))

```

In this example, `%s` is a placeholder for a string, and `%d` is a placeholder for an integer. The values of the `name` and `age` variables are inserted into the string using the `%` operator.

### sys module

The `sys` module in Python provides access to some variables used or maintained by the interpreter and to functions that interact strongly with the interpreter. It comes with the Python standard library, and thus does not require any external installation.

One common use of the `sys` module is to access arguments passed to the Python script via the command line. The `argv` variable is a list in Python, which contains the command-line arguments passed to the script. Here's an example:

```python
import sys

print("The command line arguments are:")
print(sys.argv)

```

This code will print out the command line arguments passed to the script when it was run.

Another use case for the `sys` module is to exit a Python script. The `exit()` function in the `sys` module allows you to exit a Python script with a status code. Here's an example:

```python
import sys

print("Exiting the script with a status code of 1")
sys.exit(1)

```

This code will exit the Python script with a status code of 1.

The `sys` module also provides access to other interpreter-related variables and functions, such as `sys.stdin`, `sys.stdout`, and `sys.stderr`, which allow you to interact with the standard input, output, and error streams, respectively. For example, you can use `sys.stdout.write()` to write to the standard output stream.

These are just a few examples of how the `sys` module can be used in a Python script. There are many other functions and variables available in the module, which you can explore further in the Python documentation.

### Sequential files

There are two types of files: binary files and sequential files. Binary files contain data in a format that can be directly interpreted by a computer, such as images, videos, and executable programs. Sequential files, on the other hand, contain data that is organized in a specific order, such as a CSV file or a text file. To access a sequential file, the computer must read through the file in order, while binary files can be accessed more quickly and efficiently. However, sequential files are usually easier for humans to read and modify, while binary files are often used to store large amounts of data that need to be accessed quickly.

### os module

The `os` module in Python provides a way of interacting with the operating system. It comes with the Python standard library, and thus does not require any external installation.

One common use of the `os` module is to manipulate files and directories. The `os` module provides functions such as `os.listdir()` to list the contents of a directory, `os.mkdir()` to create a new directory, `os.rename()` to rename a file or directory, and `os.remove()` to delete a file.

Another use case for the `os` module is to get information about the operating system. The `os.name` variable contains the name of the operating system (e.g. `"posix"` for Unix-based systems or `"nt"` for Windows), while the `os.getcwd()` function returns the current working directory.

The `os` module also provides functions for working with environment variables, setting file permissions, and more. For example, `os.environ` is a dictionary-like object that contains the environment variables for the current process.

The `os` module in Python provides a way of interacting with the operating system. It comes with the Python standard library, and thus does not require any external installation.

Some of the methods in the `os` module for managing files include `os.open()` for opening a file, `os.write()` for writing to a file, `os.read()` for reading from a file, and `os.close()` for closing a file. You can also use the `os.path` module to manipulate file paths, such as joining paths using `os.path.join()`, getting the basename of a path using `os.path.basename()`, and more.

The `os.system()` method in Python allows you to execute a shell command from within a Python script. It returns the exit status of the command, which can be used to determine if the command was successful or not. However, it is not recommended to use this method for complex tasks, as it is not very flexible and can be difficult to debug.

These are just a few examples of how the `os` module can be used to manage files in a Python script. There are many other functions and variables available in the module, which you can explore further in the Python documentation.

### Web scrapping

Web scraping is the process of extracting data from websites. This can be useful for a variety of purposes, such as data analysis, research, and automation. Web scraping involves writing code that accesses a website's HTML code and extracts the relevant data. This can be done using libraries such as **Beautiful Soup** and **Scrapy** in Python. However, it is important to note that web scraping can be illegal or against the terms of service of some websites, so it should be done carefully and ethically. It is also important to respect website owners' privacy and not overload their servers with requests.