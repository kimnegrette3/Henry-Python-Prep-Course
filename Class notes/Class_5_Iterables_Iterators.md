# Chapter 5: Iterables and iterators

Created: April 27, 2023 5:35 PM
Reviewed: Yes
Type: Lecture

# Chapter 5: Iterables and Iterators

In Python, an **iterable** is an object that can be used in an iteration, which means it can be used in a for loop. An iterable is any object that implements the `__iter__()` or `__getitem__()` method. Examples of iterables in Python include lists, tuples, dictionaries, and sets.

An **iterator** is an object that produces the next value in a sequence when you call `next()` on it. Iterators are used to iterate over iterables. Iterators implement the `__next__()` method. Once all the values have been generated, calling `next()` on the iterator raises the `StopIteration` exception.

Here's an example using a list:

```python
my_list = [1, 2, 3, 4, 5]

# using a for loop
for item in my_list:
    print(item)

# using a while loop
iter_list = iter(my_list)
while True:
    try:
        item = next(iter_list)
        print(item)
    except StopIteration:
        break

```

Output:

```
1
2
3
4
5
1
2
3
4
5

```

In the example above, `my_list` is an iterable. We can use it in a for loop or convert it to an iterator using the `iter()` function and use a while loop to iterate over its elements.

In conclusion, iterables are objects that can be used in an iteration, and iterators are objects that produce the next value in a sequence when you call `next()` on them. Both are essential concepts in Python programming, and understanding them will help you write more efficient and effective code.

The `zip()` function is a built-in Python function that takes two or more iterables and returns an iterator that generates tuples containing the elements from each of the iterables. If the iterables have different lengths, the `zip()` function will stop after the shortest one is exhausted.

Here's an example:

```python
names = ['Alice', 'Bob', 'Charlie']
ages = [25, 35, 45]
genders = ['female', 'male', 'male']

for name, age, gender in zip(names, ages, genders):
    print(f"{name} is {age} years old and is {gender}")

```

Output:

```python
Alice is 25 years old and is female
Bob is 35 years old and is male
Charlie is 45 years old and is male

```

In the example above, we use the `zip()` function to iterate over three lists simultaneously and print out information about each person.

The `zip()` function is often used to combine data from multiple sources into a single iterable that can be easily processed together.

Here's an example of iteration with conditionals:

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]

for number in numbers:
    if number % 2 == 0:
        print(f"{number} is even")
    else:
        print(f"{number} is odd")

```

Output:

```
1 is odd
2 is even
3 is odd
4 is even
5 is odd
6 is even
7 is odd
8 is even
9 is odd
10 is even

```

In the example above, we iterate over a list of numbers and use a conditional to determine whether each number is even or odd. Depending on the result, we print out a message indicating whether the number is even or odd.

The `enumerate()` function is a built-in Python function that returns an iterator that generates tuples containing the index and value of each element in an iterable. It is often used in for loops to keep track of the index of the current element being processed.

Here's an example:

```python
fruits = ['apple', 'banana', 'cherry']

for i, fruit in enumerate(fruits):
    print(i, fruit)

```

Output:

```
0 apple
1 banana
2 cherry

```

In the example above, we use the `enumerate()` function to iterate over a list of fruits and print out the index and value of each element. The `enumerate()` function returns an iterator that generates tuples containing the index and value of each element, which we unpack into the variables `i` and `fruit`.

The `enumerate()` function can also take an optional second argument, which specifies the starting value of the index. By default, the index starts at 0, but you can specify a different starting value if needed.

Here's an example:

```python
fruits = ['apple', 'banana', 'cherry']

for i, fruit in enumerate(fruits, start=1):
    print(i, fruit)

```

Output:

```
1 apple
2 banana
3 cherry

```

In the example above, we use the `enumerate()` function with a starting index of 1 to iterate over a list of fruits and print out the index and value of each element, starting at 1 instead of 0.