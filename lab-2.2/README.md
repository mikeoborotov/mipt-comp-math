# Computational Math, Lab 2 (2nd semester)

## Contents

- [Task](#task)
- [Calculation method](#calculation-method)
- [Program parameters](#program-parameters)
- [Program output](#program-output)

## Task

The task is to implement a numerical method for solving the Poisson equation:

$$ div(a(x,y) \cdot grad(u(x,y))) = f(x,y) $$

The area of interest:

![alt text](https://github.com/OborotovMikhail/mipt-comp-math/blob/master/lab-2.2/readme-images/image-area.png? "The area of interest")

Right side of the equation is not zero on the square S. Function $a(x,y) = (x^2 + 1)/10$ by default.

[:arrow_up: Back to contents](#Contents)

## Calculation method

Below is a theoretical derivation of the algorithm for compiling the SLE (system of linear equations) matrix for this equation.

![alt text](https://github.com/OborotovMikhail/mipt-comp-math/blob/master/lab-2.2/readme-images/image-theory-1.jpg? "Theory")

![alt text](https://github.com/OborotovMikhail/mipt-comp-math/blob/master/lab-2.2/readme-images/image-theory-2.jpg? "Theory")

![alt text](https://github.com/OborotovMikhail/mipt-comp-math/blob/master/lab-2.2/readme-images/image-theory-3.jpg? "Theory")

With the help of these coefficients of the elements we will compute a matrix form for our SLE.

[:arrow_up: Back to contents](#Contents)

## Program parameters

First few sections of the code is dedicated to the parameters set by the user.

The program is implemented in such a way that in its parameters it is possible to set another area S (however, in the same quarter of the plane). You can specify other functions $f(x,y)$ and $a(x,y)$, but the derivatives of $a(x,y)$ will have to be calculated manually. The possibility of dependence of $a(x,y)$ on $y$ is taken into account (that is, the case of a non-zero derivative with respect to $y$ is taken into account).

[:arrow_up: Back to contents](#Contents)

## Program output

As a result, the program produces graphs. The program does not work with points in the bottom-right quarter of the area, since they are not included in the area.
However, in order to preserve the dimensions of arrays when plotting graphs, these points are added back and just considered to be equal to 0.

Plot of the function $f(x,y)$ defined by the condition:

![alt text](https://github.com/OborotovMikhail/mipt-comp-math/blob/master/lab-2.2/readme-images/image-plot-1.png? "f(x,y) function")

Matrix form of the SLE plots in black-and-white and color versions:

![alt text](https://github.com/OborotovMikhail/mipt-comp-math/blob/master/lab-2.2/readme-images/image-plot-2.1.png? "Matrix form of the SLE")

![alt text](https://github.com/OborotovMikhail/mipt-comp-math/blob/master/lab-2.2/readme-images/image-plot-2.2.png? "Matrix form of the SLE")

Convergence plot of the iterative method used (Jacobi):

![alt text](https://github.com/OborotovMikhail/mipt-comp-math/blob/master/lab-2.2/readme-images/image-plot-3.1.png? "Convergence of the Jacobi method")

Finally, the solution plot:

![alt text](https://github.com/OborotovMikhail/mipt-comp-math/blob/master/lab-2.2/readme-images/image-plot-3.2.png? "Solution")

[:arrow_up: Back to contents](#Contents)
