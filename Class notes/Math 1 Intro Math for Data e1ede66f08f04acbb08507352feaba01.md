# Math 1: Intro Math for Data

Created: May 6, 2023 9:51 AM
Reviewed: Yes
Type: Lecture

## General Concepts

### Types of Numbers

- **Natural numbers (N)**: These include all positive integers, such as 1, 2, 3, 4, 5, etc.
- **Whole numbers (W)**: These include all natural numbers and 0, such as 0, 1, 2, 3, 4, 5, etc.
- **Integers (Z)**: These include all positive and negative whole numbers, such as -3, -2, -1, 0, 1, 2, 3, etc.
- **Rational numbers (Q)**: These include all numbers that can be expressed as a fraction, such as 1/2, 0.75, -3.25, etc.
- **Irrational numbers (I)**: These include all numbers that cannot be expressed as a fraction and have an infinite decimal expansion, such as √2, π, etc.
- **Real numbers (R)**: These include all rational and irrational numbers, such as 3, -1/2, √2, π, etc.

For example, 3 is a natural number, 0 is a whole number, -2 is an integer, 1/2 is a rational number, and √2 is an irrational number.

![Untitled](Math%201%20Intro%20Math%20for%20Data%20e1ede66f08f04acbb08507352feaba01/Untitled.png)

**Types of Numbers in Python**

In Python, there are several types of numbers that can be used in programming:

- **int**: These are integers, such as 1, 2, 3, etc. They are stored in the computer's memory as binary digits, or "bits". In Python, you can declare an integer using the `int` keyword, such as `x = 5`.
- **float**: These are decimal numbers, such as 2.5, 3.14, etc. They are also stored in the computer's memory as bits, but they use a different format than integers. In Python, you can declare a float using the `float` keyword, such as `x = 3.14`.
- **complex**: These are numbers with a real and imaginary part, such as 3+4j. They are stored in the computer's memory as two floats, one for the real part and one for the imaginary part. In Python, you can declare a complex number using the `complex` keyword, such as `x = 3+4j`.

Python also has a built-in function called `type()` which you can use to check the type of a variable. For example, `type(5)` would return `<class 'int'>` because 5 is an integer.

It's important to understand the type of numbers you are working with in Python because certain operations, such as division, can behave differently depending on the type of numbers involved. For example, dividing two integers in Python will return an integer, while dividing a float and an integer will return a float.

### Geometry: Angles and trigonometry

Angles are an important concept in geometry and are used extensively in programming and machine learning. An angle is formed by two rays that share a common endpoint, called the vertex. The amount of rotation needed to rotate one ray to coincide with the other ray is called the angle between the rays. Angles are typically measured in degrees or radians.

Trigonometry is a branch of mathematics that deals with the relationships between the sides and angles of triangles. It has many practical applications in programming and machine learning, such as in 3D graphics and computer vision.

In programming, angles can be used to calculate the direction of movement or the orientation of an object in space. For example, in a video game, the angle of a player's movement can be used to determine the direction in which the player is moving. In machine learning, angles can be used to represent data in a high-dimensional space, which can make it easier to analyze and classify data.

Trigonometry functions, such as sine, cosine, and tangent, are commonly used in programming and machine learning to calculate angles and distances between points in space. These functions can be used to perform complex calculations and can help to simplify many programming and machine learning tasks.

**Sine, Cosine, and Tangent Functions**

Sine, cosine, and tangent are trigonometric functions that are commonly used in mathematics, science, and engineering. They are defined as follows:

- **Sine (sin)**: The sine of an angle is the ratio of the length of the opposite side to the length of the hypotenuse in a right triangle.
- **Cosine (cos)**: The cosine of an angle is the ratio of the length of the adjacent side to the length of the hypotenuse in a right triangle.
- **Tangent (tan)**: The tangent of an angle is the ratio of the length of the opposite side to the length of the adjacent side in a right triangle.

These functions are often used to calculate the angles and distances between points in space in programming and machine learning. For example, the cosine function can be used to calculate the dot product between two vectors, which is a measure of their similarity. The sine and cosine functions can be used to calculate the orientation of an object in space, such as a spacecraft or a robot.

![Untitled](Math%201%20Intro%20Math%20for%20Data%20e1ede66f08f04acbb08507352feaba01/Untitled%201.png)

The **unit circle i**s a circle with a radius of 1 unit, centered at the origin of a coordinate plane. It is commonly used in trigonometry to define the values of sine and cosine for all angles between 0 and 360 degrees (or 0 and 2π radians). The unit circle is divided into four quadrants, and the values of sine and cosine are positive or negative depending on the quadrant in which the angle falls. The unit circle is useful because it allows us to visualize the relationships between the trigonometric functions and the angles they represent.

![Untitled](Math%201%20Intro%20Math%20for%20Data%20e1ede66f08f04acbb08507352feaba01/Untitled%202.png)

**In Python,** these functions are available in the `math` module. You can use the `sin()`, `cos()`, and `tan()` functions to calculate the sine, cosine, and tangent of an angle, respectively. For example, `math.sin(30)` would return the sine of 30 degrees.

### Logarithms and exponentials

Logarithms and exponentials are two important mathematical concepts that are used extensively in programming and machine learning. They are closely related and have many practical applications, such as in finance, engineering, and data analysis.

### Properties of Logarithms and Exponentials

Logarithmic and exponential functions have many important properties that make them useful in programming and machine learning. Some of these properties include:

- **Product Rule**: $`log_a(xy) = log_a(x) + log_a(y)`$ and $`a^(x+y) = a^x * a^y`$
- **Quotient Rule**: $`log_a(x/y) = log_a(x) - log_a(y)`$ and $`a^(x-y) = a^x / a^y`$
- **Power Rule**: $`log_a(x^y) = y*log_a(x)`$ and $`(a^x)^y = a^(xy)`$
- **Change of Base Formula**: $`log_a(x) = log_b(x) / log_b(a)`$

These properties can be used to simplify and manipulate logarithmic and exponential expressions, making them easier to work with in programming and machine learning. For example, the product and quotient rules can be used to simplify complex expressions involving logarithmic or exponential functions, while the power rule can be used to calculate the values of exponential functions for large or small values of `x`.

### Functions

A mathematical function is a rule that assigns a unique output value to each input value. In other words, it takes one or more inputs and produces a single output. Functions are used extensively in mathematics, science, and engineering to model and analyze complex systems and phenomena.

The most common types of functions include:

- **Linear functions**: These are functions of the form $`y = mx + b`$, where `m` i8s the slope, `b` is the y-intercept, and `x` is the input variable. Linear functions have a constant rate of change and produce a straight line when graphed.
- **Quadratic functions**: These are functions of the form $`y = ax^2 + bx + c`$, where `a`, `b`, and `c` are constants and `x` is the input variable. Quadratic functions have a curved shape and are commonly used to model parabolic motion.
- **Exponential functions**: These are functions of the form $`y = a^x`$, where `a` is a constant and `x` is the input variable. Exponential functions have a characteristic curve that starts at the point `(0,1)` and curves upward as `x` increases. They are commonly used to model growth or decay.
- **Logarithmic functions**: These are functions of the form $`y = log_a(x)`$, where `a` is a constant and `x` is the input variable. Logarithmic functions have a characteristic curve that starts at the point `(1,0)` and curves upward as `x` increases. They are commonly used to solve exponential equations and to model data that grows or decays logarithmically.

**In Python,** mathematical functions are available in the `math` module. You can use the `sin()`, `cos()`, and `tan()` functions to calculate the sine, cosine, and tangent of an angle, respectively. You can use the `log()` function to calculate logarithms with any base, and the `exp()` function to calculate exponential functions. Additionally, you can use the `pow()` function to raise a number to a power, and the `sqrt()` function to calculate the square root of a number.

**Domain and image of functions**

The **domain** of a function is the set of all possible input values for the function. In other words, it is the set of all `x` values for which the function is defined. For example, the domain of the function $`f(x) = 1/x`$ is all real numbers except for 0, because the function is undefined for `x = 0`. For most of the functions, the domain includes real numbers: `Dom=R`

The **image** (also called the range) of a function is the set of all possible output values for the function. In other words, it is the set of all `y` values that the function can produce. For example, the image of the function $`f(x) = x^2`$ is all non-negative real numbers, because the function can only produce non-negative output values.

In mathematics, a **partitioned domain** is a way of defining the domain of a function by dividing it into separate regions, each with its own set of conditions for the input. This can be useful when the function is defined differently in different parts of its domain, or when certain inputs are not allowed in certain regions.

For example, consider the function $`f(x) = sqrt(x-3)`$. This function is only defined for $`x >= 3`$, because the square root of a negative number is not a real number. We can define the domain of this function using a partitioned domain as follows:

- For $`x >= 3`$, $`f(x) = sqrt(x-3)`$
- For $`x < 3`$, $`f(x)`$ is undefined

![Representation of a partitioned domain function g(a)](Math%201%20Intro%20Math%20for%20Data%20e1ede66f08f04acbb08507352feaba01/Untitled%203.png)

Representation of a partitioned domain function g(a)

Using a partitioned domain can help to clarify the conditions under which the function is defined and can make it easier to work with in mathematical and computational contexts.

**A function can only have one element of the image for each element of the domain** because it is a rule that assigns a unique output value to each input value. In other words, if the function were to produce two different output values for the same input value, it would violate this rule and would not be a function.

![Untitled](Math%201%20Intro%20Math%20for%20Data%20e1ede66f08f04acbb08507352feaba01/Untitled%204.png)

Understanding the domain and image of a function is important because it can help you to identify where the function is defined and what types of output values it can produce. This can be useful in many applications, such as data analysis, optimization, and modeling.

### Equation of a Line

An **equation of a line** is a mathematical expression that describes a line in a Cartesian plane. The general form of an equation of a line is 

$$
y = mx + b 
$$

where `m` is the slope of the line and `b` is the y-intercept of the line. The slope of a line is the ratio of the change in y to the change in x, and can be calculated using the formula 

$$
m = (y_2 - y_1) / (x_2 - x_1)
$$

where: 

$$
 (x_1, y_1) and (x_2, y_2) 
$$

are two points of a line.

The slope of a line can be interpreted as the rate of change of the line. If the slope is positive, the line slopes upwards as it moves to the right, indicating an increase in the value of y as the value of x increases. If the slope is negative, the line slopes downwards as it moves to the right, indicating a decrease in the value of y as the value of x increases.

The y-intercept of a line can be calculated by substituting `x = 0` into the equation of the line and solving for `y`. This point indicates the value of `y` when `x = 0`, i.e. the position where the line crosses the y-axis.

The equation of the line can also be written in the form of a **linear function** as $`f(x) = mx + b`$, where $`y = f(x)`$. In this case, the linear function describes the relationship between `x` and `y` on the line.

In summary, the equation of a line is a fundamental tool in analytic geometry and is used to describe and model lines in a Cartesian plane. The slope and y-intercept are two important properties of a line that can be calculated from its equation, and the linear function describes the relationship between `x` and `y` on the line.

![Untitled](Math%201%20Intro%20Math%20for%20Data%20e1ede66f08f04acbb08507352feaba01/Untitled%205.png)

### Graphs

Graphs are visual representations of mathematical functions that can be used to analyze and model complex systems and phenomena. They are commonly used in mathematics, science, engineering, and data analysis to visualize data and relationships between variables.

A graph is typically composed of two axes, the x-axis and the y-axis, which represent the input and output variables of a function, respectively. The points on the graph represent the values of the function for different input values, and the shape of the graph can provide insights into the behavior of the function.

![Representation of f(x) = 2*x](Math%201%20Intro%20Math%20for%20Data%20e1ede66f08f04acbb08507352feaba01/Untitled%206.png)

Representation of f(x) = 2*x

In programming and machine learning, graphs can be used to visualize data and relationships between variables, to identify patterns and trends, and to model complex systems and phenomena. For example, in data analysis, graphs can be used to visualize the distribution of data, the relationship between variables, and the performance of predictive models.

Python has several libraries that can be used to create and manipulate graphs, including **matplotlib** and **seaborn**. These libraries provide a wide range of functions and tools for creating and customizing graphs, including line graphs, scatter plots, bar charts, and histograms.

To create a graph in Python, you typically start by importing the appropriate library and then using its functions to specify the data and plot the graph. For example, to create a simple line graph in matplotlib, you might use the following code:

```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4, 5]
y = [2, 4, 6, 8, 10]

plt.plot(x, y)
plt.show()

```

This code would create a line graph with the input values `x = [1, 2, 3, 4, 5]` and the output values `y = [2, 4, 6, 8, 10]`. The `plt.plot()` function specifies the data to be plotted, and the `plt.show()` function displays the graph on the screen.

Graphs can be used to model and analyze a wide range of phenomena, from the behavior of financial markets to the spread of infectious diseases. They are an essential tool in many fields of study and can help to reveal insights and patterns that might otherwise go unnoticed.