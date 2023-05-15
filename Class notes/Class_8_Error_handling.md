# Chapter 8: Error handling

Created: May 5, 2023 12:43 PM
Reviewed: Yes
Type: Lecture

# Chapter 8: Error handling

Error handling is an important aspect of Python programming that ensures efficient and effective code execution by detecting and responding to errors. Python provides a range of built-in error types such as SyntaxError, TypeError and ValueError, which can be raised when errors occur.

Advantages of error handling in Python include:

- Improved code reliability and robustness
- Enhanced debugging capability
- Improved user experience

## Black box testing

Black box testing is a technique used to test the functionality of a Python program without examining its internal structures or workings. This type of testing focuses on the inputs and outputs of the program, and ensures that the program behaves correctly according to its specifications. Black box testing is important for verifying that a program is working correctly from the user's perspective, and can help identify errors that may not be visible from examining the code alone.

### Unit testing

Unit testing is a type of testing that involves testing individual pieces, or units, of code in isolation from the rest of the program. This is typically done by writing test functions or test cases that specifically target a particular function or module, and verifying that the output is as expected. Unit tests are useful for ensuring that individual functions or modules work as expected, and can help identify errors early in the development process.

### Integration testing

Integration testing is a type of testing that involves testing how different parts of a program work together. This is typically done by testing the interactions between different modules or subsystems, and ensuring that they work correctly when combined. Integration tests are useful for verifying that a program works as expected when all the pieces are put together, and can help identify errors that may not be visible from testing individual units in isolation.

### unittest module

The unittest module is a built-in Python library that provides a framework for writing and running unit tests. It includes a number of helpful methods and classes for creating test cases, running tests, and reporting the results.

To use the unittest module, you typically create a separate test file that imports the module you want to test and defines a series of test cases. Each test case is a separate method that tests a specific aspect of the code being tested. The unittest module provides a range of assertion methods for testing conditions and values, such as assertEqual() and assertTrue().

Once you have defined your test cases, you can use the unittest module to run them and report the results. The module provides a TextTestRunner class that can output the results in a variety of formats, including plain text, HTML, and XML.

Unit testing with the unittest module is an important part of the development process, as it helps ensure that individual pieces of code are working as expected and can help identify errors early on.

An example of using the unittest module to test a simple function could look like this:

```python
import unittest

def square(x):
    return x ** 2

class TestSquare(unittest.TestCase):
    def test_square_positive(self):
        self.assertEqual(square(2), 4)
        self.assertEqual(square(3), 9)

    def test_square_negative(self):
        self.assertEqual(square(-2), 4)
        self.assertEqual(square(-3), 9)

if __name__ == '__main__':
    unittest.main()

```

In this example, the `square()` function is being tested using the `unittest` module. The `TestSquare` class defines two separate test cases, `test_square_positive()` and `test_square_negative()`, which each test the `square()` function with different inputs. The `assertEqual()` method is used to verify that the output of `square()` matches the expected output.

The `if __name__ == '__main__':` block at the end of the file is used to run the tests when the file is executed directly.

When this code is run, the output will show whether or not the tests passed or failed. If a test fails, the output will indicate which test failed and what the actual output was versus the expected output.

```python
python -m unittest test_square.py
.
----------------------------------------------------------------------
Ran 1 test in 0.000s

OK

```

## Crystal box testing

Crystal box testing, also known as white box testing, is a software testing technique that involves examining the internal structure and implementation of a program to ensure that it is functioning correctly. This type of testing is typically done by software developers, who have access to the source code and can examine it in detail.

The goal of crystal box testing is to identify errors or bugs in the internal logic of a program, such as incorrect calculations or improper use of data structures. This type of testing can help ensure that a program is functioning correctly on a low level, and can help identify errors that may not be visible from black box testing alone.

Crystal box testing can be done using a variety of techniques, including code reviews, static analysis, and dynamic analysis. Code reviews involve examining the source code of a program line by line to identify potential errors or areas of improvement. Static analysis involves using automated tools to analyze the source code and identify potential errors or vulnerabilities. Dynamic analysis involves running the program and examining its behavior at runtime to identify errors or unexpected behavior.

Overall, crystal box testing is an important part of the software development process, as it helps ensure that programs are functioning correctly and can help identify errors early in the development process.

One example of crystal box testing using the `unittest` module might involve testing the internal implementation of a function to ensure that it is working correctly. This could involve examining how the function handles edge cases or testing specific branches of the code to ensure that it behaves as expected.

For example, consider the following function that calculates the factorial of a number:

```python
def factorial(n):
    if n < 0:
        raise ValueError('Factorial is only defined for non-negative integers')
    elif n == 0:
        return 1
    else:
        return n * factorial(n - 1)

```

This function uses recursion to calculate the factorial of a number. To test this function using crystal box testing, we might define a series of test cases that examine how the function behaves for different inputs.

```python
import unittest

class TestFactorial(unittest.TestCase):
    def test_factorial_positive(self):
        self.assertEqual(factorial(5), 120)
        self.assertEqual(factorial(10), 3628800)

    def test_factorial_zero(self):
        self.assertEqual(factorial(0), 1)

    def test_factorial_negative(self):
        with self.assertRaises(ValueError):
            factorial(-1)

if __name__ == '__main__':
    unittest.main()

```

In this example, the `TestFactorial` class defines three separate test cases, each of which tests a different aspect of the `factorial()` function. The `test_factorial_positive()` and `test_factorial_zero()` test cases examine how the function behaves for positive integers and zero, respectively, while the `test_factorial_negative()` test case verifies that the function raises an appropriate error when given a negative input.

The `assertEqual()` method is used to verify that the output of `factorial()` matches the expected output, while the `assertRaises()` method is used to verify that the function raises a `ValueError` when given a negative input.

When this code is run, the output will show whether or not the tests passed or failed. If a test fails, the output will indicate which test failed and what the actual output was versus the expected output.

```python
python -m unittest test_factorial.py
...
----------------------------------------------------------------------
Ran 3 tests in 0.000s

OK

```

In this example, all three test cases pass, indicating that the `factorial()` function is functioning correctly according to our expectations.

### Black box vs. Crystal box testing

| Black box testing | Crystal box testing |
| --- | --- |
| Tests functionality without examining internal structure | Examines internal structure and implementation |
| Focuses on inputs and outputs of program | Focuses on low-level details of program |
| Verifies that program behaves correctly according to specifications | Verifies that program is functioning correctly on a low level |
| Useful for verifying that program works from user's perspective | Useful for identifying errors in internal logic |
| Can identify errors that may not be visible from examining code alone | Can help ensure that program is functioning correctly |
| Examples include unit testing and integration testing | Examples include code reviews, static analysis, and dynamic analysis |
| Typically done by testers or quality assurance professionals | Typically done by software developers |

### Exception handling

Exception handling is the process of detecting and responding to errors that occur during program execution. In Python, exceptions are raised when an error occurs, and can be caught and handled using try-except blocks.

Here's an example:

```python
try:
    x = int(input("Please enter a number: "))
except ValueError:
    print("That was not a valid number. Please try again.")

```

In this example, the `input()` function is used to get a number from the user, which is then converted to an integer using the `int()` function. If the user enters something other than a number, a `ValueError` will be raised. To handle this error, a try-except block is used. The `try` block contains the code that may raise an exception, and the `except` block contains the code that should be executed if an exception is raised.

If a `ValueError` is raised, the code in the `except` block will be executed, which in this case simply prints an error message and prompts the user to try again.

Here's another example that shows how to handle multiple types of exceptions:

```python
try:
    x = int(input("Please enter a number: "))
    result = 10 / x
except ValueError:
    print("That was not a valid number. Please try again.")
except ZeroDivisionError:
    print("You cannot divide by zero. Please try again.")
else:
    print("The result is:", result)

```

In this example, the `input()` function is used to get a number from the user, which is then converted to an integer using the `int()` function. If the user enters something other than a number, a `ValueError` will be raised. If the user enters 0, a `ZeroDivisionError` will be raised when the code attempts to divide by zero.

To handle these errors, two separate `except` blocks are used, one for `ValueError` and one for `ZeroDivisionError`. If either of these exceptions is raised, the corresponding error message will be printed. If no exception is raised, the code in the `else` block will be executed, which in this case simply prints the result of the division.

By using try-except blocks to handle exceptions, you can prevent your program from crashing when errors occur, and provide more informative error messages to your users.

Here are 20 of the most commonly used exceptions in Python:

1. `Exception`: The base class for all exceptions in Python.
2. `ValueError`: Raised when a function or operation receives an argument that has the right type but an inappropriate value.
3. `TypeError`: Raised when a function or operation receives an argument of the wrong type.
4. `IndexError`: Raised when a sequence index is out of range.
5. `KeyError`: Raised when a dictionary key is not found.
6. `AttributeError`: Raised when an attribute reference or assignment fails.
7. `IOError`: Raised when an I/O operation (such as a file open) fails.
8. `ImportError`: Raised when an import statement fails.
9. `NameError`: Raised when a variable name is not found.
10. `RuntimeError`: Raised when an error occurs that doesn't fit into any other category.
11. `StopIteration`: Raised when an iterator is exhausted.
12. `ZeroDivisionError`: Raised when division or modulo by zero is attempted.
13. `FileNotFoundError`: Raised when a file or directory is not found.
14. `NotImplementedError`: Raised when an abstract method or function is called that is not implemented.
15. `IndentationError`: Raised when the indentation of Python code is not correct.
16. `SyntaxError`: Raised when the syntax of Python code is not correct.
17. `OverflowError`: Raised when the result of an arithmetic operation is too large to be represented.
18. `MemoryError`: Raised when an operation runs out of memory.
19. `RecursionError`: Raised when a function or method calls itself too many times.
20. `KeyboardInterrupt`: Raised when the user interrupts the execution of a program (for example, by pressing Ctrl+C on the keyboard).

Note that this list is not exhaustive, and there are many other exceptions that can be raised in Python.

### Assertions

In Python, an assertion is a statement that checks whether a condition is true, and raises an exception if it is not. Assertions are typically used to check for conditions that should always be true, such as checking that a variable has a certain value or that a function returns the expected output.

Assertions can be used to catch errors early in the development process, and can help ensure that your code is working correctly before you release it to users.

Here's an example:

```python
def divide(x, y):
    assert y != 0, "Divide by zero error"
    return x / y

print(divide(10, 2))   # Output: 5.0
print(divide(10, 0))   # AssertionError: Divide by zero error

```

In this example, the `divide()` function is used to divide two numbers. Before the division is performed, an assertion is used to check that the second number is not equal to zero. If the second number is zero, an `AssertionError` is raised with the message "Divide by zero error".

When the `divide()` function is called with the arguments 10 and 2, the output is 5.0, as expected. However, when the function is called with the arguments 10 and 0, an `AssertionError` is raised with the message "Divide by zero error".

Assertions can be a useful tool for catching errors early in development, but they should be used judiciously. Assertions can be disabled globally in Python using the `-O` (optimize) command line option or the `PYTHONOPTIMIZE` environment variable, so it is important to ensure that your code still works correctly even when assertions are disabled.

Overall, assertions are a useful tool for catching errors early in development, and can help ensure that your code is working correctly. However, they should be used carefully and judiciously to avoid false positives or false negatives.

### Exceptions vs. Assertions

Exceptions and assertions are both used for error handling in Python, but they serve different purposes.

Exceptions are used to handle errors that occur during program execution, such as when a function is called with invalid arguments or when a file cannot be found. Exceptions are raised when an error occurs and can be caught and handled using `try`-`except` blocks. Exception handling allows you to handle errors gracefully and prevent your program from crashing.

Assertions, on the other hand, are used to check for conditions that should always be true, such as checking that a variable has a certain value or that a function returns the expected output. Assertions are typically used for debugging and testing purposes, and can be used to catch errors early in the development process. If an assertion fails, an `AssertionError` is raised.

In summary, exceptions are used to handle errors that occur during program execution, while assertions are used to check for conditions that should always be true.

### EAFP vs. LBYL principles

Python provides two main approaches to exception handling and flow control: the **EAFP (Easier to Ask Forgiveness than Permission)** principle and the **LBYL (Look Before You Leap) principle.**

**The EAFP principle** is based on the idea that it is easier to handle exceptions that are raised when something goes wrong, rather than trying to anticipate every possible error beforehand. This approach involves writing code that assumes everything will work as expected, and then using try-except blocks to catch and handle any exceptions that are raised.

Here's an example:

```python
try:
    file = open("example.txt")
    content = file.read()
    file.close()
except FileNotFoundError:
    print("The file was not found.")

```

In this example, the `open()` function is used to open a file called `example.txt`, and the `read()` method is used to read its contents into a variable called `content`. If the file is not found, a `FileNotFoundError` will be raised. Rather than checking whether the file exists before opening it, the code simply tries to open the file and then handles the exception if it is raised.

**The LBYL principle**, on the other hand, is based on the idea of looking before you leap, and involves checking for potential errors before they occur. This approach involves writing code that explicitly checks for potential errors before executing a particular action.

Here's an example:

```python
import os

if os.path.exists("example.txt"):
    file = open("example.txt")
    content = file.read()
    file.close()
else:
    print("The file was not found.")

```

In this example, the `os.path.exists()` function is used to check whether the file `example.txt` exists before attempting to open it. If the file exists, the code opens it and reads its contents. If the file does not exist, the code prints an error message.

Both approaches have their advantages and disadvantages, and the choice between them depends on the specific requirements of your program. The EAFP approach can make your code more concise and easier to read, but may be less efficient if exceptions are raised frequently. The LBYL approach can make your code more explicit and easier to debug, but may result in more verbose and repetitive code.

**In general, the EAFP approach is preferred in Python, as it is more Pythonic and can lead to more concise and readable code**. However, the LBYL approach may be more appropriate in certain situations, such as when performance is a concern or when it is important to explicitly check for potential errors.

It's worth noting that Python's built-in functions and modules generally follow the EAFP approach, and raise exceptions when errors occur rather than returning error codes or values. This makes it easier to write concise and readable code, and encourages users to handle exceptions explicitly using try-except blocks.

Overall, both the EAFP and LBYL principles are important concepts in Python programming, and understanding when to use each approach can help you write more effective and efficient code.

### Good practices, a summary

Some good practices for error handling and debugging in Python include:

- Using exception handling to gracefully handle errors and prevent program crashes
- Logging errors and other important information to help with debugging
- Writing clear and descriptive error messages that provide useful information to users and developers
- Using assertions to catch errors early in development
- Writing comprehensive unit tests to ensure that individual pieces of code are working correctly
- Using static analysis tools to identify potential errors or vulnerabilities in the code
- Following best practices for code organization and documentation to make the code easier to understand and maintain.

These practices can help ensure that Python programs are reliable, robust, and easy to maintain, and can help identify errors early in the development process.