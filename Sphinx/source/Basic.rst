******
Basic
******

=========
Dimension
=========

How to find the relationship between two quantities? For example, what is the dimensional relationship between length and mass.

| Plank constant: :math:`\mathrm{ \hbar \sim [Energy]\cdot [Time] \sim [Mass]\cdot [Length]^2 \cdot [Time]^{-1} }`
| * Speed of light in vacuum: :math:`\mathrm{ c\sim [Length]\cdot [Time]^{-1} }`
| * Gravitational constant: :math:`\mathrm{  G \sim [Length]^3\cdot [Mass]^{-1} \cdot [Time]^{-2} }`


Then it is easy to find that a combination of :math:`c/\hbar` cancels the dimension of mass and leaves the inverse of length. That is

.. math::

   [\mathrm{Length}]^2 = \frac{\hbar G}{c^3}




Most Wonderful Equations That Should Never Be Forgotten
=========================================================

Electrodynamics
----------------


Maxwell Equations
^^^^^^^^^^^^^^^^^^

.. math::

   \nabla\times\vec E&=&-\partial_t \vec B \\
   \nabla\times\vec H&=&\vec J+\partial_t \vec D \\
   \nabla\cdot \vec D&=&\rho \\
   \nabla\cdot \vec B&=&0


For linear meterials, 

.. math::
   
   \begin{eqnarray}
      \vec D&=&\epsilon \vec E \\
      \vec B&=&\mu \vec H \\
      \vec J&=& \sigma \vec E
   \end{eqnarray}


Dynamics
-----------

Hamilton conanical equations

.. math::
   \begin{eqnarray}
   \dot q_i &=& \frac{\partial H}{\partial p_i}  \\
   \dot p_i &=& - \frac{\partial H}{\partial q_i}
   \end{eqnarray}


Thermodynamics and Statistical Physics
----------------------------------------

Liouville's Law

.. math::
   \begin{eqnarray}
   \frac{\mathrm d \rho}{\mathrm d t}\equiv \frac{\partial \rho}{\partial t} + \sum_i \left[ \frac{\partial \rho}{\partial q_i}\dot q_i + \frac{\partial \rho}{\partial p_i}\dot p_i \right] = 0
   \end{eqnarray}





