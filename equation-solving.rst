Equation Solving
*******************




There are so many methods and techniques to solve an equation. Here we will review only some of them.


Ordinary Differential Equations
===================================




There are many important equations in physics.

.. figure:: math/assets/2ndODEs.png
   :align: center

   Taken from Riley's book.



The are many methods to solve an ODE,

1. Green's function.
2. Series solution
3. Laplace transform
4. Fourier transform




Green's Function
---------------------------


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


.. admonition:: An Example
   :class: note
   :name: greenFunctionExample

   Solve equation

   .. math::
      y'' + \frac{1}{4}y = f(x).

   {\bf Green's Function }

   The operator is :math:`\hat L = \partial^2 + 1/4` with boundary condition :math:`y(0)=y(\pi)=0` .

   First step is to find the Green's function of this operator, which is defined as the solution to

   .. math::
      \hat L G(x,x') = \delta(x-x'),

   where :math:`\hat L` only operates on :math:`x` not :math:`x'`.

   The general solutions for :math:`\hat L G(x,x')=0` is

   .. math::
      G(x,x') = A\cos(x/2) + B \sin(x/2).

   Applying the BC, we reach a step function expression for :math:`G(x,x')`,

   .. math::
      G(x,x') =   &B\sin(x/2) , \text{if} 0\leq x \lt x' , \\
      &A\cos(x/2) , \text{if} x'\lt x \leq \pi . 


   {\bf Continuity and Discontinuity }

   It is required by the equation for Green's function that,

   .. math::
      G(x',x') = A \sin(x'/2) = B \cos(x'/2),

   and

   .. math::
      \frac{d G}{d x}\vert_{x'+} - \frac{dG}{dx}\vert_{x'-} = 1 .

   Put the expressions for Green's function in, we can solve the coefficients,

   .. math::
      G(x,x') = & -2 \cos(x'/2)\sin(x/2) , \text{if} 0\leq x \lt x' ,\\ & -2 \sin(x'/2)\cos(x/2) , \text{if} x' \lt x \leq \pi . 


   In one line this can be written as,

   .. math::
      G(x,x') = -2 \sin(x_</2)\cos(x_>/2) .

   The final step is to find the solution to original equaion, which is straightforward.














Series Solution
-------------------------

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
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Series expansion of the solution can be as simple as

.. math::
   y(z) = \sum_{n=0}^{\infty} a_n z^n,

which converges in a radius :math:`R` where :math:`R` is the distance from :math:`z=0` to the nearest singular point of our ODE.



Solution at Regular Singular Points
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

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






Comparing With A General Form
------------------------------------

For equation that take the following form,

.. math::
   y'' + \frac{1 - 2a}{x} y' + \left( (b c x^{c-1})^2 + \frac{a^2 - p^2 c^2}{x^2} \right) y = 0,

where :math:`y\equiv y(x)`, we can write down the solutions immediately,

.. math::
   y(x) = x^a \mathscr {Z}_p (b x^c),

in which :math:`\mathscr {Z}_p` is the solution to Bessel equation, i.e., is one kind of Bessel function with index :math:`p`.


.. admonition:: A Pendulum With A Uniformly Chaning String Length
   :class: note

    As an example, let's consider the case of length changing pendulum,

    .. math::
       \frac{d}{dt} \left( m l^2 \dot{\theta}\right) = - m g l \sin\theta \approx = - m g l \theta.

    Notice that l is a function of time and 

    .. math::
       l = l_0 + v t.

    Then the equation can be rewritten as

    .. math::
       \frac{d^2}{dl^2}\theta  + \frac{2}{l} \frac{d}{dl} \theta + \frac{g/v^2}{l} \theta  = 0.

    Comparing with the general form, we have one of the possible solutions

    .. math::
       a & = -1/2, \\
       pc & = 1/2, \\
       c & = 1/2, \\
       p & = 1, \\
       b & = 2\sqrt{g}/v.

    This solution should be

    .. math::
       \theta  &=  l^a \mathscr{Z}_p(b l^c) \\
       & = \frac{1}{\sqrt{l}} J_1(\frac{2\sqrt{g}}{v} \sqrt{l}).



.. admonition:: Airy Equatioin
   :class: note


    Time-independent Schrödinger equation with a simple potential,

    .. math::
       \ddot{\Psi} + \alpha x \Psi  = 0.

    Comparing it with general form, we should set

    .. math::
       a & = 1/2, \\
       \lvert p c \rvert & = 1/2, \\
       c & = 3/2, \\
       b^2 c^2 & = \alpha^2.

    So the two possible solutions are 

    .. math::
       \Psi_1(x) & = \sqrt{x} \mathscr{Z}_{1/3}(2/3 \alpha x^{3/2}), \\
       \Psi_2(x) & = \sqrt{x} \mathscr{Z}_{-1/3}(2/3 \alpha x^{3/2}).

    The general solution is

    .. math::
       \Psi(x) = a \Psi_1(x) + b \Psi_2(x).




Second Order Differential Equations and Gauss' Equation
------------------------------------------------------------------------------------------------


Gauss' equation has the form

.. math::
   z(z-1)\frac{d^2}{dz^2} u(z) + \left[(a+b+1)z -c \right] \frac{d}{dz} u(z) + a b u(z) =0,

which has a solution of the hypergeometric function form

.. math::
   u(z) = {}_2 F_{1}(a,b;c;z).

The interesting this about this equation is that its Paperitz symbol is 

.. math::
   \begin{amatrix}{3}
  0 & 1 & \infty &  \\  0 & 0 & a & z \\ 1-c & c-a-b & b & 
   \end{amatrix} ,

in which the first three columns are the singularities at points :math:`0,1,\infty` while the last column just points out that the argument of this equation is :math:`z`.

This means, in some sense, the solution to any equation with three singularities can be directly written down by comparing the equation with Gauss' equation. If you care, the actual steps are changing variables, rewriting the equation into Gauss' equation form, writing down the solutions.



Integral Equations
=================================================



Neumann Series AKA WKB
---------------------------


For differential equation, whenever the highest derivative is multiplied by a small parameter, try this. But generally, the formalism is the following.

First of all, we use Hilbert space :math:`\mathscr L[a,b;w]` which means the space is defined on :math:`[a,b]` with a weight :math:`w`, i.e.,

.. math::
   \braket{f}{g} = \int_a^b dx w(x) f(x) g(x).


.. admonition:: Quantum Mechanics Books
   :class: note

   **Notice that this is very different from the notation we used in most QM books.**

   What is the catch? Try to write down :math:`\braket{x}{u}`. It's not that different because one can alway go back to the QM notation anyway.


With the help of Hilbert space, one can alway write down the vector form of some operators. Suppose we have an equation

.. math::
   \hat L u(x) = f(x),

where :math:`\hat L=\hat I + \hat M`. So the solution is simply

.. math::
   u(x) &= {\hat L}^{-1} f(x)\\
   &=(\hat I + \hat M)^{-1} f(x) .

However, it's not a solution until we find the inverse. A most general approach is the Neumann series method. We require that

.. math::
   \| \hat M u \| < \gamma \| u \|,

where :math:`\gamma\in (0,1)` and should be independent of :math:`x`.

As long as this is satisfied, the equation can be solved using Neumann series, which is an iteration method with

.. math::
   u(x)&=u_0(x)+ \delta u_1(x) + \delta^2 u_2(x) +\cdots \\
   u_0(x) & = f(x).

As an example, we can solve this equation

.. math::
   (\hat I + \ket{t}\bra{\lambda}) u(t) = f(t).

We define :math:`\hat M = \ket{t}\bra{\lambda}` and check the convergence condition for :math:`\lambda`.

Step one is always checking condition of convergence.

Step two is to write down the series and zeroth order. Then we reach the key point. The iteration relation is

.. math::
   u_n(t) + \int_0^1 ds su_{n-1}(s) = 0.

One can write down :math:`u_1` imediately

.. math::
   u_1(t) = -\int_0^1 ds s u_0(s).

Keep on going.



Using Dyads in Vector Space
-----------------------------


For the same example,

.. math::
   \hat L u(x) = f(x),

where :math:`\hat L=\hat I + \hat M`, we can solve it using vector space because if operator is linear.

Suppose we have a :math:`\hat M=\ket{a}\bra{b}`, the equation, in some Hilbert space, is

.. math::
   \ket{u} + \ket{a}\braket{b}{u} = \ket{f}.

Multiplying through by :math:`\bra{b}`, we have

.. math::
   \braket{b}{u} + \braket{b}{a}\braket{b}{u} = \braket{b}{f},

which reduces to a linear equation. We only need to solve out :math:`\braket{b}{u}` then plug it back into the original equation.
















