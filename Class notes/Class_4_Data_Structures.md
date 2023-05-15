# Chapter 4: Data Structures

Created: April 27, 2023 5:35 PM
Reviewed: Yes
Type: Lecture

# Data Structures

Data structures are fundamental constructs in Python that allow you to store and organize data in an efficient and flexible manner. Python provides several built-in data structures, such as lists, tuples, dictionaries, and sets.

- Lists: A list is a collection of items that can be ordered and changed. It is a mutable data structure and is represented with square brackets. Lists are commonly used for storing and manipulating collections of related data.
- Tuples: A tuple is an immutable sequence of items. It is represented with parentheses and is commonly used for representing fixed collections of related data.
- Dictionaries: A dictionary is a collection of key-value pairs. It is represented with curly braces and is used for storing and retrieving data based on a key. Dictionaries are commonly used for representing real-world objects and relationships between objects.
- Sets: A set is an unordered collection of unique items. It is represented with curly braces and is commonly used for operations involving the intersection, union, and difference of sets.

Understanding data structures is essential for writing efficient and effective code in Python.

## Lists

Lists in Python are a collection of ordered and mutable items, represented by square brackets. They are commonly used for storing and manipulating collections of related data. Lists can contain elements of different data types, including other lists.

Some common methods associated with lists are:

- `append(x)`: Adds an item `x` to the end of the list
- `extend(iterable)`: Adds elements from an iterable (e.g. another list) to the end of the list
- `insert(i, x)`: Inserts an item `x` at a specific index `i`
- `remove(x)`: Removes the first occurrence of item `x` from the list
- `pop([i])`: Removes and returns the item at a specific index `i`, or the last item if no index is specified
- `index(x)`: Returns the index of the first occurrence of item `x`
- `count(x)`: Returns the number of times item `x` appears in the list
- `sort()`: Sorts the items in the list in ascending order
- `reverse()`: Reverses the order of the items in the list

These methods can help you manipulate and organize the data in your lists in a variety of ways.

Here is an example of creating a list and using some of its methods:

```python
# create a list of numbers
numbers = [1, 2, 3, 4, 5]

# add an item to the end of the list
numbers.append(6)

# add multiple items to the end of the list
numbers.extend([7, 8, 9])

# insert an item at a specific index
numbers.insert(0, 0)

# remove an item from the list
numbers.remove(5)

# get the index of an item in the list
index = numbers.index(3)

# count the number of times an item appears in the list
count = numbers.count(4)

# sort the items in the list
numbers.sort()

# reverse the order of the items in the list
numbers.reverse()

```

This code creates a list of numbers, adds an item to the end of the list, adds multiple items to the end of the list, inserts an item at a specific index, removes an item from the list, gets the index of an item in the list, counts the number of times an item appears in the list, sorts the items in the list, and reverses the order of the items in the list.

## Tuples

Tuples are similar to lists, but they are immutable, meaning that their contents cannot be changed after they are created. Tuples are represented with parentheses and can contain elements of different data types, including other tuples.

Tuples are commonly used for representing fixed collections of related data, such as a date or a point in 3D space. They are also used for returning multiple values from a function.

Some common methods associated with tuples are:

- `index(x)`: Returns the index of the first occurrence of item `x`
- `count(x)`: Returns the number of times item `x` appears in the tuple

The main difference between lists and tuples is that lists are mutable and tuples are immutable. This means that you can change the contents of a list, but you cannot change the contents of a tuple after it is created.

You might choose to use a tuple instead of a list when you want to represent a fixed collection of related data that cannot be changed. For example, you might use a tuple to represent a date or a point in 3D space. You might choose to use a list instead of a tuple when you want to store and manipulate a collection of related data that can change over time.

Here are some examples of tuples:

```python
# create a tuple with three items
point = (1, 2, 3)

# create a tuple with one item
single_item_tuple = (1,)

# create a tuple with different data types
mixed_tuple = (1, 'hello', True)

# use a tuple to return multiple values from a function
def get_user_info():
    name = 'Alicia'
    age = 30
    email = 'alicia@example.com'
    return name, age, email

# get the values from the tuple returned by the function
user_info = get_user_info()
name, age, email = user_info

```

In these examples, we create tuples with different numbers and types of items, and use a tuple to return multiple values from a function.

## Dictionaries

Dictionaries in Python are a collection of key-value pairs, represented with curly braces. They are used for storing and retrieving data based on a key, which can be any immutable data type (e.g. strings, numbers, tuples). Dictionaries are commonly used for representing real-world objects and relationships between objects, such as a database of users and their information.

To access a value in a dictionary, you can use the key associated with that value. For example, if you have a dictionary of user information with keys 'name', 'age', and 'email', you can access a user's email by using the key 'email'. You can also add, remove, and modify key-value pairs in a dictionary.

Some common methods associated with dictionaries are:

- `keys()`: Returns a list of all the keys in the dictionary
- `values()`: Returns a list of all the values in the dictionary
- `items()`: Returns a list of all the key-value pairs in the dictionary as tuples
- `get(key[, default])`: Returns the value associated with the key, or a default value if the key is not found
- `pop(key[, default])`: Removes the key-value pair associated with the key and returns the value, or a default value if the key is not found
- `update(other)`: Updates the dictionary with key-value pairs from another dictionary or iterable of key-value pairs

These methods can help you manipulate and organize the data in your dictionaries in a variety of ways.

```python
# create a dictionary of user information
user_info = {
    'name': 'Alicia',
    'age': 30,
    'email': 'alicia@example.com'
}

# get the value associated with a key
name = user_info['name']

# add a new key-value pair to the dictionary
user_info['phone'] = '555-555-5555'

# remove a key-value pair from the dictionary
del user_info['email']

# get a list of all the keys in the dictionary
keys = user_info.keys()

# get a list of all the values in the dictionary
values = user_info.values()

# get a list of all the key-value pairs in the dictionary as tuples
items = user_info.items()

# get the value associated with a key, or a default value if the key is not found
phone = user_info.get('phone', 'No phone number found')

# remove the key-value pair associated with a key and return the value, or a default value if the key is not found
email = user_info.pop('email', 'No email found')

# update the dictionary with key-value pairs from another dictionary or iterable of key-value pairs
other_info = {
    'address': '123 Main St',
    'city': 'Anytown'
}
user_info.update(other_info)

```

This code creates a dictionary of user information, gets the value associated with a key, adds a new key-value pair to the dictionary, removes a key-value pair from the dictionary, gets a list of all the keys in the dictionary, gets a list of all the values in the dictionary, gets a list of all the key-value pairs in the dictionary as tuples, gets the value associated with a key, or a default value if the key is not found, removes the key-value pair associated with a key and returns the value, or a default value if the key is not found, and updates the dictionary with key-value pairs from another dictionary or iterable of key-value pairs.

In Python, you can convert between different data structures using built-in functions. For example:

- `list(iterable)`: Converts an iterable (e.g. a tuple, set, or string) to a list
- `tuple(iterable)`: Converts an iterable to a tuple
- `set(iterable)`: Converts an iterable to a set
- `dict(iterable)`: Converts an iterable of key-value pairs to a dictionary
- `list(dictionary)`: Converts a dictionary to a list of its keys
- `tuple(dictionary)`: Converts a dictionary to a tuple of its keys
- `set(dictionary)`: Converts a dictionary to a set of its keys

You can also convert between different data structures using slicing and indexing. For example, you can convert a list to a tuple by slicing it with `tuple(my_list)`.

It's important to note that when you convert between data structures, you may lose some information or change the order of the elements. For example, converting a list to a set will remove any duplicate elements and change the order of the remaining elements.