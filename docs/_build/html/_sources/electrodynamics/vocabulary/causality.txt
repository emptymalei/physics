Causality
*********************


Field theory shows a lot of casality conditions. Here is a collection of them.



Radiation
=======================



Maxwell's equations in vacuum are 

.. math::
   \nabla\cdot \vec E &= 4\pi \rho, \\
   \nabla \cdot \vec B &  = 0, \\
   \nabla \times \vec E & = -\frac{1}{c}\partial_t \vec B, \\
   \nabla \times \vec B & = \frac{1}{c}\partial_t E + \frac{4\pi}{c}\vec j.


To write down the wave equation, we could switch to the scalar potential :math:`\phi` and vector potential :math:`\vec A`.

Divergence free means that we can always have

.. math::
   \vec B = \nabla \times \vec A.

By using the above relation, I could rewrite this to

.. math::
   \nabla \times \vec E &= -\frac{1}{c} \partial_t (\nabla \times \vec A),\\
   \nabla \times ( \vec E + \frac{1}{c} \partial_t  \vec A ) &= 0.


This means I can write all inside divergance written as a gradient of a scalar function or a constant time the gradient of some scalar function.

.. math::
   \vec E= -\nabla \phi - \frac{1}{c} \partial_t \vec A.


With the definition of scalar and vector potentials, we could plug them in and find the wave equations. However, since the values of these potential are gauge dependent, I should choose a convinient gauge. Hereby, I use Lorenz gauge.

.. math::
   \frac{1}{c} \partial_t \phi + \nabla \cdot \vec A = 0.

The importance of this gauge is that it is Lorentz invariant.

Using this gauge the two other Maxwell's equations, I have the wave equations,

.. math::
   (\frac{1}{c^2} \partial_t^2 -\nabla^2) \phi &= 4\pi \rho ,\\
   (\frac{1}{c^2} \partial_t^2 -\nabla^2) \vec A &= \frac{4\pi}{c} \vec j .


Solving these Helmholtz equations, I get the solution as a function of retarted time :math:`t_{ret}=t-\frac{R}{c}`, where :math:`R=\vert \vec x - \vec x' \vert`.


.. math::
   \phi(t,\vec x) &= \int d^3x' \frac{\rho(t_{ret},\vec x')}{R}, \\
   \vec A(t,\vec x) & = \int d^3 x' \frac{\vec j(t_{ret},\vec x')}{R}.

Here it clearly shows that the observation depends on the history :math:`R/c` ago. This is the signal propagation time.



Response of Matter
====================


.. math::
   \vec P = \int \chi(t,t') \vec E(t') dt'.














