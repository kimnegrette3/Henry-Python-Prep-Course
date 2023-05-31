# Math 2: Functions

Created: May 6, 2023 12:39 PM
Reviewed: Yes
Type: Lecture

### Limits

A limit is the value that a function approaches as the input (usually denoted as x) gets closer and closer to a certain value. Limits are important in math functions because they help us understand the behavior of a function around a given point. By studying limits, we can determine if a function is continuous, has a hole or a jump, or if it approaches infinity at a certain point. Additionally, limits are used in calculus to find derivatives and integrals of functions.

For the function 1/x, as x approaches 0 from the left (i.e., x < 0), the function approaches negative infinity (i.e., the function gets smaller and smaller without bound in the negative direction). Conversely, as x approaches 0 from the right (i.e., x > 0), the function approaches positive infinity (i.e., the function gets larger and larger without bound in the positive direction). This is an example of a function that has a vertical asymptote at x=0, since the function approaches infinity as x approaches 0 from either side.

![Untitled](Math%202%20Functions%209bc923bdcf4e489bba8c70292a9b4568/Untitled.png)

### Continuity

Continuity is a property of a function where there are no abrupt changes or breaks in the graph. In other words, a function is continuous if it does not have any holes, jumps, or breaks. For a function to be continuous at a point, the limit of the function as x approaches that point must exist and be equal to the value of the function at that point. In simpler terms, if you can draw the graph of a function without lifting your pen from the paper, then the function is continuous. Continuity is important in calculus because it allows us to use certain mathematical techniques, such as the Mean Value Theorem and the Intermediate Value Theorem, to analyze functions and solve problems.

- Limits from left and right exist and are finite? YES
- Limits from left and right are equal? YES
- Limits from left and right are equal to the valu of the function in that point? YES

—> Then, we can say the the function is continuos at that point

*All three statements need to be True

### Discontinuity

Discontinuity is a property of a function where there is a sudden break or jump in the graph. A function can be discontinuous at a point if the limit of the function as x approaches that point does not exist, or if the limit exists but is not equal to the value of the function at that point. There are three types of discontinuities: removable, jump, and infinite. A removable discontinuity occurs when there is a hole in the graph at a certain point, but the limit of the function at that point exists. A jump discontinuity occurs when the limit of the function from the left and right exists, but they are not equal. An infinite discontinuity occurs when the limit of the function at a certain point is infinity or negative infinity. Discontinuities can make it difficult to analyze functions and solve problems using mathematical techniques like calculus.

- Limits from left and right exist and are finite? NO
- Limits from left and right are equal? NO
- Limits from left and right are equal to the valu of the function in that point? NO

—> Then, we can say the the function is NOT continuos at that point

*If one of the three statements are False, the function is NOT continuous

Discontinuity is a property of a function where there is a sudden break or jump in the graph. There are **three main types of discontinuity: removable, jump, and infinite**.

A **removable discontinuity** occurs when there is a hole in the graph at a certain point, but the limit of the function at that point exists. This means that the function can be made continuous by filling in the hole or removing the point of discontinuity. A common example of a removable discontinuity is the function $(x^2 - 1)/(x-1)$, which has a hole at $x=1$.

**Jump discontinuity** occurs when the limit of the function from the left and right exists, but they are not equal. In other words, the function "jumps" from one value to another at a certain point. A classic example of a jump discontinuity is the function $f(x) = 1/x$, which has a jump discontinuity at $x = 0$.

An **infinite discontinuity** occurs when the limit of the function at a certain point is infinity or negative infinity. This typically occurs when the denominator of a fraction approaches 0, resulting in an unbounded value. For example, the function $f(x) = 1/x$ has an infinite discontinuity at $x=0$, since the function approaches positive infinity as x approaches 0 from the right, and negative infinity as x approaches 0 from the left.

Discontinuities can make it difficult to analyze functions and solve problems using mathematical techniques like calculus. Therefore, it is important to identify the type of discontinuity and its location in the function in order to find ways to address it.

![Untitled](Math%202%20Functions%209bc923bdcf4e489bba8c70292a9b4568/Untitled%201.png)

### Derivability

Derivability is a property of a function that **measures how fast the function is changing at a given point.** The derivative of a function at a point is defined as the limit of the difference quotient as the distance between two points approaches zero. In other words, the derivative measures the slope of the tangent line to the function at a given point.

Derivatives are used in calculus to solve a variety of problems, such as finding the maximum and minimum values of a function, computing rates of change, and determining the concavity of a function. They are also used in data science to analyze trends in data and make predictions about future outcomes.

To find the derivative of a function, you can use a variety of techniques, such as the power rule, chain rule, and product rule. Once you have found the derivative of a function, you can use it to solve a variety of problems and gain deeper insights into the behavior of the function.

In order for a function to be derivable at a point, it must be continuous at that point. Additionally, the limit of the difference quotient as the distance between two points approaches zero must exist and be finite. If these conditions are met, then the function is said to be differentiable at that point.

The derivability of a function is related to its “smoothness” and “predictibility”. It is easier to find a tangent line in a function without abrupt changes in slope. 

![Untitled](Math%202%20Functions%209bc923bdcf4e489bba8c70292a9b4568/Untitled%202.png)

![Untitled](Math%202%20Functions%209bc923bdcf4e489bba8c70292a9b4568/Untitled%203.png)

### Functional analysis and critical points

Derivatives are used in functional analysis to help determine the critical points of a function. Critical points are points on a function where the derivative is either zero or undefined. They are important because **they can help us identify the maximum and minimum values of a function, as well as the points of inflection,** where the concavity of the function changes.

A point of inflection is a point on a function where the concavity changes. It occurs when the second derivative changes sign from positive to negative or vice versa. Points of inflection can help us understand the curvature of a function and identify regions where the slope is increasing or decreasing. Not all functions have points of inflection, but analyzing them can give insights into the behavior of the function.

To find the critical points of a function, we first take the derivative of the function. Then, we set the derivative equal to zero and solve for x. The values of x that we get are the critical points of the function. We also need to check the values of the derivative to see if they are undefined at certain points.

Once we have identified the critical points of a function, we can use them to analyze the behavior of the function. For example, if we know that a function has a critical point at x = 3, we can plug in values on either side of 3 to see if the function increases or decreases in that region. We can also use the second derivative test to determine whether the critical point is a maximum or a minimum.

Functional analysis is an important tool in calculus and many other areas of mathematics and science. By analyzing the behavior of functions, we can gain insights into complex systems and make predictions about their behavior.

![Untitled](Math%202%20Functions%209bc923bdcf4e489bba8c70292a9b4568/Untitled%204.png)

![Untitled](Math%202%20Functions%209bc923bdcf4e489bba8c70292a9b4568/Untitled%205.png)

### Multivariate function

A multivariate function is a function that takes more than one input variable. For example, the function 

$$
f(x,y) = x^2 + y^2 
$$

is a multivariate function that takes two input variables, x and y. Multivariate functions are used in many areas of math and science, including calculus, physics, and engineering.

In calculus, multivariate functions are used to study surfaces and volumes in three-dimensional space. The partial derivative is a key concept in calculus that allows us to find the rate of change of a multivariate function with respect to one of its input variables, while holding the other variables constant.

Multivariate functions can also be analyzed using techniques from linear algebra, such as eigenvectors and eigenvalues. These techniques can be used to find critical points of multivariate functions and to study their behavior near these points.

In summary, multivariate functions are an important concept in math and science that allow us to study complex systems with multiple input variables.