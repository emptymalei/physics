Complex Analysis
================



Some useful concepts: [1]_

* Representation of a complex number and its conjugate
* Complex functions
* curves, closed curves, simple curves
* Ininity point
* Analytic functions: depends only on z not its complex conjugate
* Entire function: single-valued analytic all over C
* Liouville theorem
* Pole
* Singularity, Essential Singularity
* Meromorphic function

For multi-valued functions,

* A branch of a function
* Analyticity of multi-valued function
* Branch point
* Cut


Operations

* Contour integral of a continuous function arround some simple curve
* Cauchy's Integral Theorem




Cauchy-Riemann Equation
-----------------------------------

A function :math:`f(z) = u(z) + i v(z)` is a function of a complex variable :math:`z=x+i y`.

.. math::
   \frac{\partial}{\partial x} u &= \frac{\partial}{\partial y} v \\
   \frac{\partial}{\partial x} v & = -\frac{\partial}{\partial y} u



Singularities
--------------------


There are 3 common singularities,

1. Pole
2. Branch point
3. Essential singularity


Pole is very useful since it's related to the Residue Theorem. Thus one of the task in physics is to calculate the residue of a function.

The residue at a simple pole is given by

.. math::
   \text{Residue}(f(z_0)) = \lim_{z\to z_0}\left( (z-z_0)f(z) \right).

Meanwhile, the residue at a pole of nth order is

.. math::
   \text{Residue}(f(z_0)) =  \frac{1}{(n-1)!} \lim_{z\to z_0} \frac{\mathrm d ^ {n-1}}{\mathrm d z^{n-1}}  \left( (z-z_0)^n f(z) \right).


Branch points are points when we go around it in circles the values of our function would change. Examples of such points are :math:`z=0` for :math:`f(z)=ln(z)` and :math:`z=1` for :math:`f(z)=(z-1)^{1/2}`.




Refs & Notes
============

..  [1] `A handout note by Finly <http://physics.unm.edu/Courses/Finley/p466F2014/Homework/hw1.pdf>`_
