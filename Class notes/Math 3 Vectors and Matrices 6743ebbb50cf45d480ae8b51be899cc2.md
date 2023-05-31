# Math 3: Vectors and Matrices

Created: May 16, 2023 12:42 PM
Reviewed: Yes
Type: Lecture

# Vectors

Vectors are mathematical objects that are used to represent quantities that have both magnitude and direction. They are commonly used in physics, engineering, and mathematics to describe quantities such as velocity, force, and displacement.

A vector is represented by an arrow, with the length of the arrow indicating the magnitude of the vector and the direction of the arrow indicating the direction of the vector. In two-dimensional space, a vector can be represented by a pair of numbers (x,y), where x and y represent the horizontal and vertical components of the vector, respectively. In three-dimensional space, a vector can be represented by a triplet of numbers (x,y,z).

![Untitled](Math%203%20Vectors%20and%20Matrices%206743ebbb50cf45d480ae8b51be899cc2/Untitled.png)

In two-dimensional space, a vector can be represented by a pair of numbers (x,y), where x and y represent the horizontal and vertical components of the vector, respectively. The horizontal component, x, corresponds to the magnitude of the vector in the x direction, and the vertical component, y, corresponds to the magnitude of the vector in the y direction. The vector's magnitude is equal to the square root of the sum of the squares of its components:

$$
\sqrt{(x^2 + y^2)}
$$

![Untitled](Math%203%20Vectors%20and%20Matrices%206743ebbb50cf45d480ae8b51be899cc2/Untitled%201.png)

![Untitled](Math%203%20Vectors%20and%20Matrices%206743ebbb50cf45d480ae8b51be899cc2/Untitled%202.png)

The direction of a vector is given by the angle it makes with the positive x-axis. In two-dimensional space, this angle can be calculated using the formula:

$$

\theta = \arctan\frac{v_1}{v_2}
$$

where v1 and v2 are the horizontal and vertical components of the vector, respectively. In three-dimensional space, the direction of a vector can be given by its direction cosines, which are the cosines of the angles between the vector and the x, y, and z axes.

**Vectors can be added, subtracted, scaled, and multiplied in various ways**. The addition of vectors involves placing the tail of one vector at the head of another vector and connecting the tail of the first vector to the head of the second vector. The result is a new vector that represents the sum of the two original vectors.

![Untitled](Math%203%20Vectors%20and%20Matrices%206743ebbb50cf45d480ae8b51be899cc2/Untitled%203.png)

The subtraction of vectors involves adding the negative of one vector to another vector. The result is a new vector that represents the difference between the two original vectors.

![Untitled](Math%203%20Vectors%20and%20Matrices%206743ebbb50cf45d480ae8b51be899cc2/Untitled%204.png)

Scaling a vector involves multiplying it by a scalar, which is a real number. This results in a new vector that has the same direction as the original vector but a different magnitude.

The dot product of two vectors is a scalar quantity that is equal to the product of the magnitudes of the two vectors and the cosine of the angle between them. The dot product is used to calculate the angle between two vectors and to project one vector onto another vector.

![Untitled](Math%203%20Vectors%20and%20Matrices%206743ebbb50cf45d480ae8b51be899cc2/Untitled%205.png)

The cross product of two vectors is a vector quantity that is perpendicular to both of the original vectors. The magnitude of the cross product is equal to the product of the magnitudes of the two vectors and the sine of the angle between them. The cross product is used to calculate the area of a parallelogram and the moment of a force.

![Untitled](Math%203%20Vectors%20and%20Matrices%206743ebbb50cf45d480ae8b51be899cc2/Untitled%206.png)

<aside>
💡 Vectors and their operations play a crucial role in data science, where they are used to represent data points, features, and observations in high-dimensional spaces. In the context of data science, a vector is an ordered set of numbers that represents a specific data point. By transforming data points into vectors, we can use vector operations to analyze and manipulate the data.

</aside>

**One of the most basic vector operations is vector addition,** which involves adding two or more vectors together to obtain a new vector that represents the sum of the original vectors. In data science, vector addition can be used to combine or separate features of data points. For example, in image processing, vector addition can be used to combine the red, green, and blue color channels of an image into a single vector, which can then be analyzed and manipulated using vector operations.

Another important vector operation is **vector scaling,** which involves multiplying a vector by a scalar, or a real number. In data science, vector scaling can be used to normalize or standardize the data. Normalization involves scaling the data so that it has a mean of zero and a standard deviation of one, while standardization involves scaling the data so that it has a range of values between zero and one.

**The dot product of two vectors** is a scalar quantity that is equal to the product of the magnitudes of the two vectors and the cosine of the angle between them. In data science, the dot product can be used to measure the similarity or dissimilarity between two data points or to project one data point onto another. For example, in text analysis, the dot product can be used to measure the similarity between two documents based on the frequency of the words they contain.

**The cross product of two vectors** is a vector quantity that is perpendicular to both of the original vectors. The magnitude of the cross product is equal to the product of the magnitudes of the two vectors and the sine of the angle between them. In data science, the cross product can be used to calculate the area of a parallelogram in two-dimensional space, which can be useful in visualization and feature engineering.

In addition to these basic vector operations, vectors and their operations can be used in more advanced machine learning algorithms, such as support vector machines and neural networks, to learn patterns and make predictions based on data. Support vector machines use vector operations to find the hyperplane that best separates the data points of different classes, while neural networks use vector operations to perform calculations on large datasets.

Overall, vectors and their operations are essential tools in data science for representing, analyzing, and manipulating high-dimensional data. They provide a powerful framework for understanding the complex relationships between data points and for building advanced machine learning algorithms that can make accurate predictions based on large datasets.

# Matrices

A matrix is a rectangular array of numbers, arranged in rows and columns. Matrices are used to represent a wide variety of mathematical objects, including linear transformations, systems of equations, and graph structures.

A matrix is denoted by a capital letter, such as A, and its elements are denoted by lowercase letters with two subscripts, such as 

$$
 a_{ij} 
$$

where i indicates the row index and j indicates the column index. For example, the matrix A below has three rows and two columns:

$$
A = \begin{bmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22} \\
a_{31} & a_{32}
\end{bmatrix}
$$

The dimensions of a matrix are given by the number of rows and columns it contains. For example, the matrix A above has dimensions 3x2, which means it has three rows and two columns.

**Matrices can be added, subtracted, and multiplied in various ways.** 

**The addition of matrices** involves adding the corresponding elements of the two matrices together. The result is a new matrix that represents the sum of the two original matrices. For example, the sum of two matrices A and B *with the same dimensions* is given by:

$$
A + B = \begin{bmatrix}
a_{11}+b_{11} & a_{12}+b_{12} \\
a_{21}+b_{21} & a_{22}+b_{22} \\
a_{31}+b_{31} & a_{32}+b_{32}
\end{bmatrix}
$$

**The subtraction of matrices** involves subtracting the corresponding elements of one matrix from the corresponding elements of another matrix. The result is a new matrix that represents the difference between the two original matrices. For example, the difference between two matrices A and B *with the same dimension*s is given by:

$$
A - B = \begin{bmatrix}
a_{11}-b_{11} & a_{12}-b_{12} \\
a_{21}-b_{21} & a_{22}-b_{22} \\
a_{31}-b_{31} & a_{32}-b_{32}
\end{bmatrix}
$$

**Multiplying a matrix by a scalar** involves multiplying each element of the matrix by the scalar. The result is a new matrix that has the same dimensions as the original matrix but with each element multiplied by the scalar.

**Matrix multiplication** is a more complex operation that involves multiplying the rows of one matrix by the columns of another matrix. The result is a new matrix that represents the product of the two original matrices. **The dimensions of the two matrices must be compatible for multiplication**, which means that the number of columns in the first matrix must be equal to the number of rows in the second matrix. For example, the product of two matrices A and B with dimensions mxn and nxp, respectively, is given by:

$$
AB = \begin{bmatrix}
a_{11}b_{11}+a_{12}b_{21}+a_{13}b_{31} & \cdots & a_{1n}b_{n1} \\
a_{21}b_{11}+a_{22}b_{21}+a_{23}b_{31} & \cdots & a_{2n}b_{n1} \\
\vdots & \ddots & \vdots \\
a_{m1}b_{11}+a_{m2}b_{21}+a_{m3}b_{31} & \cdots & a_{mn}b_{n1}
\end{bmatrix}
$$

Matrix multiplication is associative, which means that (AB)C = A(BC) for any matrices A, B, and C that are compatible for multiplication. However, it is not generally commutative, which means that AB is not necessarily equal to BA for arbitrary matrices A and B.

**The transpose of a matrix** is another important operation, which involves flipping the matrix over its diagonal. The result is a new matrix that has the same elements as the original matrix but with the rows and columns interchanged. For example, the transpose of the matrix A above is given by:

$$
A^T = \begin{bmatrix}
a_{11} & a_{21} & a_{31} \\
a_{12} & a_{22} & a_{32}
\end{bmatrix}
$$

**The inverse of a matrix** is another important operation, which involves finding a matrix that, when multiplied by the original matrix, gives the identity matrix. The identity matrix is a special matrix that has ones on the diagonal and zeros elsewhere. The inverse of a matrix A is denoted by 

$$
A^{-1}
$$

However, not all matrices have an inverse, and the inverse of a matrix that does have one may not be unique.

<aside>
💡 Matrices and their operations are used extensively in many areas of mathematics, science, and engineering. In data science, matrices are used to represent datasets, where each row represents a data point and each column represents a feature or variable. By applying matrix operations to datasets, we can perform tasks such as clustering, classification, and dimensionality reduction.

</aside>

Overall, matrices are a powerful tool in mathematics and data science for representing complex relationships between variables and for performing advanced calculations on large datasets.