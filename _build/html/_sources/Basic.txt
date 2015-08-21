******
Basic
******

.. .. sectnum::
      :start: 1

=========
Dimension
=========

How to find the relationship between two quantities? For example, what is the dimensional relationship between length and mass.

| * Plank constant: :math:`\mathrm{ \hbar \sim [Energy]\cdot [Time] \sim [Mass]\cdot [Length]^2 \cdot [Time]^{-1} }` 
| * Speed of light in vacuum: :math:`\mathrm{ c\sim [Length]\cdot [Time]^{-1} }`
| * Gravitational constant: :math:`\mathrm{  G \sim [Length]^3\cdot [Mass]^{-1} \cdot [Time]^{-2} }`


Then it is easy to find that a combination of :math:`c/\hbar` cancels the dimension of mass and leaves the inverse of length. That is

.. math::
   [ L ]^2 =\left[ \frac{\hbar G}{c^3} \right]


.. math::
   [ M ]^2 = \left [ \frac{\hbar c}{ G } \right]

.. math::
   [T]^2 = \left[ \frac{ \hbar G }{ c^5 }  \right]


As we can see, it is possible to use :math:`c=1, \hbar = 1, G =1` because we can always restore the units in a deterministic way. :math:`c, \hbar, G` are function of mass, length, time, and with :math:`c = \hbar = G=1` give us only one solution of mass, length and time: three equations + three variables.
 


Planck Scales
----------------------

As we have seen, the three constant can make up a length scale, a mass scale, a time scale. Then what are they?

Planck length:

.. math::
   l_P = \sqrt{ \frac{ \hbar G }{ c^3 } }

Planck mass:

.. math::
   m_P = \sqrt{ \frac{ \hbar c }{ G } }

Planck time:

.. math::
   t_P = \sqrt{ \frac{\hbar G}{ c^5 } }




Equations and Dimensions
------------------------

Before solving equations, it is good to reform them in to dimensionless ones.

To make the equation dimensionless doesn't mean we can just divide arbitary terms on both sides. We need to find out the characteristic quantity of the system. For example, we can divide by :math:`\hbar\omega` on both sides of Schrodinger equation for Harmonic Oscillators. This is a good step because :math:`\hbar\omega` is the characteristic energy scale of system. At the same time, we can make the length terms dimensionless using the characteristic length. DO NOT use an arbitary length!





Most Wonderful Equations That Should Never Be Forgotten
=========================================================

Electrodynamics
----------------


Maxwell Equations
^^^^^^^^^^^^^^^^^^

.. math::
   \nabla\times\vec E=-\partial_t \vec B 
   
.. math::
   \nabla\times\vec H=\vec J+\partial_t \vec D 
   
.. math::
   \nabla\cdot \vec D=\rho 
   
.. math::
   \nabla\cdot \vec B=0


For linear meterials, 

.. math::
   \vec D=\epsilon \vec E 

.. math::
   \vec B=\mu \vec H

.. math::
   \vec J= \sigma \vec E



Dynamics
-----------

Hamilton conanical equations

.. math::
   \dot q_i = \frac{\partial H}{\partial p_i}  
   
.. math::
   \dot p_i = - \frac{\partial H}{\partial q_i}


Thermodynamics and Statistical Physics
----------------------------------------

Liouville's Law

.. math::
   \frac{\mathrm d \rho}{\mathrm d t}\equiv \frac{\partial \rho}{\partial t} + \sum_i \left[ \frac{\partial \rho}{\partial q_i}\dot q_i + \frac{\partial \rho}{\partial p_i}\dot p_i \right] = 0
   




