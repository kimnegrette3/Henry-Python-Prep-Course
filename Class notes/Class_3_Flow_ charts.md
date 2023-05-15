# Chapter 3: Flow charts

Created: April 27, 2023 5:35 PM
Reviewed: Yes
Type: Lecture

# Chapter 3: Flow charts and Conditional sentences

Flow charts are graphical representations used to illustrate the flow of logic or sequence of operations in a process. In programming, flow charts are used to represent algorithms and program logic.

Flow charts consist of various shapes, including rectangles, diamonds, and circles, which are used to represent different elements in the process. Rectangles represent process steps, diamonds represent decision points, and circles are used to indicate the beginning or end of a process.

Flow charts are useful in programming as they provide a visual representation of the logic and sequence of operations in a program. They make it easy to understand the program flow and identify potential errors. They are also useful in communicating the program's design to stakeholders.

In summary, flow charts are an essential tool in programming as they help in designing, visualizing, and communicating the program's logic and sequence of operations.

![Untitled](Chapter%203%20Flow%20charts%2028ad5aa36c05434fb4dda4e4df1fd09d/Untitled.png)

![Untitled](Chapter%203%20Flow%20charts%2028ad5aa36c05434fb4dda4e4df1fd09d/Untitled%201.png)

## Conditional sentences if, elif, else

Conditional sentences in Python allow for the execution of different code based on whether a certain condition has been met or not. This is similar to the decision points represented by diamond shapes in flow charts.

In Python, conditional statements are created using the `if`, `elif`, and `else` keywords. The `if` statement executes a block of code if a certain condition is true. The `elif` statement is used to check additional conditions if the previous conditions were not met. The `else` statement executes a block of code if none of the previous conditions were true.

Here's an example of a simple program that uses conditional statements:

```python
x = 10
if x > 5:
    print("x is greater than 5")
elif x == 5:
    print("x is equal to 5")
else:
    print("x is less than 5")

```

This program first checks if `x` is greater than 5. If it is, it prints "x is greater than 5". If not, it checks if `x` is equal to 5. If it is, it prints "x is equal to 5". If neither of these conditions are true, it prints "x is less than 5".

In a flow chart, this program could be represented using rectangles to represent the process steps and diamonds to represent the decision points. The `if` statement would be represented by a diamond, with two branches leading from it. One branch would lead to the `print("x is greater than 5")` statement, while the other branch would lead to another diamond representing the `elif` statement. This process would continue until the final `else` statement is reached.

In summary, conditional statements in Python are used to execute different code based on whether a certain condition has been met or not, and can be represented in flow charts using decision points and branches.

## Loop statements: while and for

Loop statements in Python allow for the repeated execution of a block of code. There are two types of loop statements in Python: `while` loops and `for` loops.

A `while` loop will repeat a block of code as long as a certain condition is true. The condition is checked at the beginning of each iteration of the loop. Here's an example of a simple program that uses a `while` loop:

```python
i = 0
while i < 5:
    print(i)
    i += 1

```

This program will print the numbers 0 through 4, because the `while` loop will repeat the `print(i)` statement as long as `i` is less than 5. The `i += 1` statement increments `i` by 1 during each iteration of the loop.

A `for` loop is used to iterate over a sequence of values. Here's an example of a simple program that uses a `for` loop:

```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

```

This program will print the strings "apple", "banana", and "cherry", because the `for` loop iterates over the sequence of strings in the `fruits` list and assigns each string to the variable `fruit`. The `print(fruit)` statement is then executed for each value of `fruit`.

In a flow chart, loop statements can be represented using rectangles to represent the process steps and arrows to represent the flow of the loop. The decision point represented by the loop condition is typically represented by a diamond.

In summary, loop statements in Python allow for the repeated execution of a block of code, and can be represented in flow charts using process steps and arrows.

### Break and continue sentences

In Python, the `break` and `continue` statements are used to control the flow of loop statements.

The `break` statement is used to exit a loop prematurely. When encountered, the loop will immediately terminate and execution will continue with the next statement after the loop. Here's an example of a program that uses the `break` statement:

```python
i = 0
while i < 10:
    if i == 5:
        break
    print(i)
    i += 1

```

This program will print the numbers 0 through 4, because the `while` loop will terminate when `i` is equal to 5, due to the `break` statement. The `print(i)` statement will not be executed when `i` is equal to 5.

The `continue` statement is used to skip the rest of the current iteration of a loop and move on to the next iteration. Here's an example of a program that uses the `continue` statement:

```python
i = 0
while i < 10:
    i += 1
    if i % 2 == 0:
        continue
    print(i)

```

This program will print the odd numbers from 1 to 9, because the `continue` statement is encountered whenever `i` is even. When `i` is even, the `print(i)` statement will not be executed and the loop will move on to the next iteration.

In a flow chart, the `break` and `continue` statements can be represented using decision points and arrows to represent the flow of the loop.

In summary, the `break` and `continue` statements in Python are used to control the flow of loop statements. The `break` statement is used to exit a loop prematurely, while the `continue` statement is used to skip the rest of the current iteration of a loop and move on to the next iteration.