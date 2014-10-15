******************
Mathematics
******************

.. .. sectnum::
      :start: 2



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


Calculus
============



.. figure:: math/assets/DifferentialANDIntegralOnOnePage.png
   :align: center

   LaTeX source of this image is `here <math/assets/DifferentialANDIntegralOnOnePage.tex>`_ .




Differential of Functions
-------------------------------




Integrals
--------------

Sometimes a integral on Real plane can be very hard, one of the techniques is to work on Complex plane and use contour integral.

1. Contours: use Ghost Contours so that we don't need to calculate these complicated integrals.
2. Branch Cut: cuts are needed if we have got branch points on the complex plane.
3. Residue Theorem: we can write down the integral by calculating the residue of the integrand,

   .. math::
      \int_C f(z) \mathrm dz = 2\pi i \sum_j \text{Residue}(f(z_j)),

   where :math:`z_j` are the poles.








Linear Algebra
====================



.. _TensorProductSpace:

Tensor Product Space
-----------------------




:math:`\ket{\phi}_1` and :math:`\ket{\phi}_2` are elements of Hilbert space :math:`H_1` and :math:`H_2`. **Tensor Product** of :math:`\ket{\phi}_1` and :math:`\ket{\phi}_2` is denoted as :math:`\ket{\phi}_1\otimes \ket{\phi}_2`. This operation is linear and distributive.

**Tensor product space** :math:`H_1\otimes H_2` is composed of all the linear combinations of all possible tensor products of elements in :math:`H_1` and :math:`H_2`.


Inner Product
~~~~~~~~~~~~~

Inner product of two tensor products

.. math::
   (\bra{\phi}_1\otimes \bra{\phi}_2)(\ket{\psi}_1\otimes \ket{\psi}_2) = ( {} _ 1 \braket{\phi}{\psi}_1)({}_2\braket{\phi}{\psi}_2)


Operators Applied to Tensor Product
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Two operators :math:`\hat O_1` and :math:`\hat O_2` works on :math:`H_1` and :math:`H_2` respectively applied to tensor product

.. math::
   (\hat O_1 \otimes \hat O_2 )( \ket{\phi}_1\otimes \ket{\phi}_2 ) = (\hat O_1 \ket{\phi}_1) \otimes (\hat O_2 \ket{\phi}_2)





Ordinary Differential Equations
==========================




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
~~~~~~~~~~~~~~~~~~~~~~~~~~

Series expansion of the solution can be as simple as

.. math::
   y(z) = \sum_{n=0}^{\infty} a_n z^n,

which converges in a radius :math:`R` where :math:`R` is the distance from :math:`z=0` to the nearest singular point of our ODE.



Solution at Regular Singular Points
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

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






Tricks
------------



WKB Approximation
~~~~~~~~~~~~~~~~~~~~

When the highest derivative is multiplied by a small parameter, try this.





Differential Geometry
=======================



Metric
--------


Definitions
~~~~~~~~~~~~


Denote the basis in use as :math:`\hat e_\mu`, then the metric can be written as

.. math::
   g_{\mu\nu}=\hat e_\mu \hat \cdot e_\nu

if the basis satisfies

Inversed metric

.. math::
   g_{\mu\lambda}g^{\lambda\nu}=\delta_\mu^\nu = g_\mu^\nu






How to calculate the metric
~~~~~~~~~~~~~~~~~~~~~~~~

Let's check the definition of metric again.

If we choose a basis :math:`\hat e_\mu`, then a vector (at one certain point) in this coordinate system is

.. math::
   x^a=x^\mu \hat e_\mu


Then we can construct the expression of metric of this point under this coordinate system,

.. math::
   g_{\mu\nu}=\hat e_\mu\cdot \hat e_\nu


For example, in spherical coordinate system,

.. math:: \vec x=r\sin \theta\cos\phi \hat e_x+r\sin\theta\sin\phi \hat e_y+r\cos\theta \hat e_z
   :label: EQrelativityMetricPoint




Now we have to find the basis under spherical coordinate system. Assume the basis is :math:`\hat e_r, \hat e_\theta, \hat e_\phi`. Choose some scale factors :math:`h_r=1, h_\theta=r, h_\phi=r\sin\theta`. Then the basis is

.. math::
   \hat e_r=\frac{\partial \vec x}{h_r\partial r}=\hat e_x \sin\theta\cos\phi+\hat e_y \sin\theta\sin\phi+\hat e_z \cos\theta,

etc. Then collect the terms in formula :eq:`EQrelativityMetricPoint` is we get :math:`\vec x=r\hat e_r`, this is incomplete. So we check the derivative.

.. math::
     \mathrm d\vec x =  \hat e_x (\mathrm dr \sin\theta\cos\phi+r\cos\theta\cos\phi\mathrm d\theta-r\sin\theta\sin\phi\mathrm d\phi)

     \hat e_y (\mathrm dr\sin\theta\sin\phi+r\cos\theta\sin\phi\mathrm d\theta+r\sin\theta\cos\phi\mathrm d\phi)

     \hat e_z (\mathrm dr\cos\theta-r\sin\theta\mathrm d\theta)

      = \mathrm dr(\hat e_x\sin\theta\cos\phi +\hat e_y \sin\theta\sin\phi -\hat e_z \cos\theta)

     \mathrm d\theta (\hat e_x\cos\theta\cos\phi +\hat e_y \cos\theta\sin\phi - \hat e_z \sin\theta)r

     \mathrm d\phi (-\hat e_x\sin\phi +\hat e_y \cos\phi)r\sin\theta

     =\hat e_r\mathrm dr+\hat e_\theta r\mathrm d\theta +\hat e_\phi r\sin\theta\mathrm d \phi

Once we reach here, the component (:math:`e_r ,e_\theta, e_\phi`) of the point under the spherical coordinates system basis (:math:`\hat e_r, \hat e_\theta, \hat e_\phi`) at this point are clear, i.e.,

.. math::
    \mathrm d\vec x = \hat e_r\mathrm d r+\hat e_\theta r\mathrm d \theta+\hat e_\phi r\sin\theta \mathrm d\phi \\
     = e_r\mathrm d r+e_\theta \mathrm d\theta+e_\phi \mathrm d\phi


In this way, the metric tensor for spherical coordinates is





.. math::
   g_{\mu\nu}=(e_\mu\cdot e_\nu) = \begin{pmatrix}
   1 & 0 & 0 \\
   0 & r^2 &  0 \\
   0 & 0 & r^2 \sin^2\theta \end{pmatrix}




Connection
-----------

First class connection can be calculated

.. math::
   \Gamma^\mu_{\phantom{\mu}\nu\lambda}=\hat e^\mu\cdot \hat e_{\mu,\lambda}


Second class connection is\footnote{Kevin E. Cahill}

.. math::
   [\mu\nu,\iota]=g_{\iota\mu}\Gamma^\mu_{\phantom{\mu}\nu\lambda}





Gradient, Curl, Divergence, etc
---------------------------------


Gradient
~~~~~~~~~~~

.. math::
   T^b_{\phantom bc;a}= \nabla_aT^b_{\phantom bc}=T^b_{\phantom bc,a}+\Gamma^b_{ad}T^d_{\phantom dc}-\Gamma^d_{ac}T^b_{\phantom bd}



Curl
~~~~~~~~~~~~~~

For an anti-symmetric tensor, :math:`a_{\mu\nu}=-a_{\nu\mu}`

.. math::
      \mathrm{Curl}_{\mu\nu\tau}(a_{\mu\nu})  \equiv  a_{\mu\nu;\tau}+a_{\nu\tau;\mu}+a_{\tau\mu;\nu} \\
       = a_{\mu\nu,\tau}+a_{\nu\tau,\mu}+a_{\tau\mu,\nu}



Divergence
~~~~~~~~~~~~~

.. math::
    \mathrm{div}_\nu(a^{\mu\nu})&\equiv   a^{\mu\nu}_{\phantom{\mu\nu};\nu} \\
    & = \frac{\partial a^{\mu\nu}}{\partial x^\nu}+\Gamma^\mu_{\nu\tau}a^{\tau\nu}+\Gamma^\nu_{\nu\tau}a^{\mu\tau} \\
    & = \frac1{\sqrt{-g}}\frac{\partial}{\partial x^\nu}(\sqrt{-g}a^{\mu\nu})+\Gamma^\mu_{\nu\lambda}a^{\nu\lambda}


For an anti-symmetric tensor

.. math::
   \mathrm {div}(a^{\mu\nu})=\frac1{\sqrt{-g}}\frac{\partial}{\partial x^\nu}(\sqrt{-g}a^{\mu\nu})


**Annotation** Using the relation :math:`g=g_{\mu\nu}A_{\mu\nu}`, :math:`A_{\mu\nu}` is the algebraic complement, we can prove the following two equalities.

.. math::
   \Gamma^\mu_{\mu\nu}=\partial_\nu\ln{\sqrt{-g}}


.. math::
   V^\mu_{\phantom\mu;\mu}=\frac1{\sqrt{-g}}\frac{\partial}{\partial x^\mu}(\sqrt{-g}V^\mu)


In some simple case, all the three kind of operation can be demonstrated by different applications of the del operator, which :math:`\nabla\equiv \hat x\partial_x+\hat y\partial_y+\hat z \partial_z`.

* Gradient,  :math:`\nabla f`, in which :math:`f` is a scalar.
* Divergence, :math:`\nabla\cdot \vec v`
* Curl, :math:`\nabla \times \vec v`
* Laplacian, :math:`\Delta\equiv \nabla\cdot\nabla\equiv \nabla^2`


Linear Algebra
=================

Basic Concepts
------------------


Trace
~~~~~~~~

Trace should be calculated using the metric. An example is the trace of Ricci tensor,

.. math::
   R=g^{ab}R_{ab}


Einstein equation is

.. math::
   R_{ab}-\frac{1}{2}g_{ab}R=8\pi G T_{ab}

The trace is

.. math::
   g^{ab}R_{ab}-\frac{1}{2}g^{ab}g_{ab}R &= 8\pi G g^{ab}T_{ab} \\
   \Rightarrow R-\frac{1}{2} 4 R  &=  8\pi G T \\
   \Rightarrow -R &= 8\pi GT



Technique
------------

Inverse of a matrix
~~~~~~~~~~~~~~~~~

Many methods to get the inverse of a matrix. Check wikipedia for Invertible matrix.

Adjugate matrix method for example is here.

.. math::
   A^{-1} = \frac{A^*}{|A|}

in which, :math:`A^*` is the adjugate matrix of :math:`A`.










Refs & Notes
============

..  [1] `A handout note by Finly <http://physics.unm.edu/Courses/Finley/p466F2014/Homework/hw1.pdf>`_
