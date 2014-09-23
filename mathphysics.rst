Math in Physics
=============



Complex Analysis
--------------------------

Cauchy-Riemann Equation
~~~~~~~~~~~~~~~~~~~~~

A function :math:`f(z) = u(z) + i v(z)` is a function of a complex variable :math:`z=x+i y`.

.. math::
   \frac{\partial}{\partial x} u &= \frac{\partial}{\partial y} v \\
   \frac{\partial}{\partial x} v & = -\frac{\partial}{\partial y} u



Singularities
~~~~~~~~~~~~~~~~~~


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


Integrals
-------------------------

Sometimes a integral on Real plane can be very hard, one of the techniques is to work on Complex plane and use contour integral.

1. Contours: use Ghost Contours so that we don't need to calculate these complicated integrals.
2. Branch Cut: cuts are needed if we have got branch points on the complex plane.
3. Residue Theorem: we can write down the integral by calculating the residue of the integrand,

   .. math::
      \int_C f(z) \mathrm dz = 2\pi i \sum_j \text{Residue}(f(z_j)),

   where :math:`z_j` are the poles.




ODE
------------------------------




The are many methods to solve an ODE,

1. Green's function.
2. Series solution
3. Laplace transform
4. Fourier transform


Green's Function
~~~~~~~~~~~~~~~~~


Suppose we have a differential operator :math:`L_x`, for example :math:`L_x` can be :math:`L_x\equiv \frac{d^2}{dx^2}+1`. The definition of GF is

.. math::
   L_x G(x,z) = \delta(x-z).

with the constrain of boundary condition of the ODE.

In most cases, GF is a stepwised function.

The application of GF to ODE follows the precedure,

1. Find the general form of GF for operator :math:`L_x`;
2. Apply BC to GF;
3. Continuity at :math:`n-2` order of derivatives at point :math:`x=z`, i.e., :math:`G^{(n-2)}(x,z)\vert_{x<z} = G^{(n-2)}(x,z)\vert_{x>z}` at :math:`x=z`;
4. Discontinuity of the first order derivative at :math:`x=z`, i.e., :math:`G^{(n-1)}(x,z)\vert_{x>z} - G^{(n-1)}(x,z)\vert_{x<z} = 1` at point :math:`x=z`;
5. Solve the coefficients to get the GF;
6. The solution to an inhomogeneous ODE :math:`L_x y(x) = f(x)` is given immediately by

   .. math::
      y(x) = \int_{Lower}^{Upper} G(x,z) f(z) dz




Series Solution
~~~~~~~~~~~~~~~~~

A second order ODE,

.. math::
   y''(x)+p(x) y'(x) + q(x)y(x)=0

Wronskian of this is

.. math::
   W(x) = \begin{vmatrix} y_1 & y_2 \\ y_1' & y_2' \end{vmatrix},

where :math:`y_1` and :math:`y_2` are linearly independent solutions, i.e., :math:`c_1 y_1 + c_2 y_2=0` is only satisfied when :math:`c_1=c_2=0`. **Wronskian is NOT zero if they are linearly independent.**

Singularities of an ODE is are defined when :math:`p(x)` or :math:`q(x)` or both of them have singular points. For example, Legendre equation

.. math::
   (1-z^2) y'' - 2 z y' + l(l+1) y = 0


has three singular points which are :math:`z=\pm 1, \infty` while :math:`z=0` is an ordinary point.


Solution at Ordinary Points
```````````````````````````````````

Series expansion of the solution can be as simple as

.. math::
   y(z) = \sum_{n=0}^{\infty} a_n z^n,

which converges in a radius :math:`R` where :math:`R` is the distance from :math:`z=0` to the nearest singular point of our ODE.



Solution at Regular Singular Points
```````````````````````````````````````````````

Frobenius series of the solution

.. math::
   y(z) = z^\sigma \sum_{n=0}^{\infty} a_n z^n.

The next task is to find the indicial equation.

If the roots are not differing by an integer, we just plug the two solutions to :math:`\sigma` in and find two solutions independently.

If the roots differ by an integer, on the other side, we can only plug in the **larger** root and find one solution. As for the second solution, we need some other techniques, such as Wronskian method and derivative method.


**Wronskian method** requires two expression of Wronskian, which are

.. math::
   W(x) = \begin{vmatrix} y_1 & y_2 \\ y_1' & y_2' \end{vmatrix} ,

and

.. math::
   W(z) = C e^{-\int^z p(u) \mathrm du}.

From the first expression, we have

.. math::
   y_2(z) = y_1(z) \int^z \frac{W(u)}{y_1(u)^2} \mathrm d u.

However, we don't know :math:`W(z)` at this point. We should apply the second expression of Wronskian,

.. math::
   y_2(z) = y_1(z) \int^z \frac{C e^{-\int^z p(u) \mathrm du}}{y_1(u)^2} \mathrm d u,

where the constant :math:`C` can be set to 1 as one wish.


.. admonition:: TO DO
   :class: warning

   The **derivative method** is on my to do list.







Refs & Notes
-------------------
