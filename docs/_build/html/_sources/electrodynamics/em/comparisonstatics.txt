Comparison of E & M
==============================================


Useful Tricks
--------------------------------------


.. math::
   \partial_i(x_k j_i) = j_k + x_k \partial_i j_i

This is useful because we have

.. math::
   \nabla \cdot \vec j = \partial_i j_i = \frac{d}{dt} \rho = 0,

and the LHS can be turned into a surface integral as one wish and disappears.


A similar one is

.. math::
   \partial_i(x_k x_l j_i) .



Statics in Vacuum
----------------------------------


Source of Fields
~~~~~~~~~~~~~~~~~~~~~~~~~~~~


1. Source of Electric Field in Electrostatics

Source of electric field is charge

.. math::
   \nabla \cdot \vec E = 4\pi \rho


2. Source of Maganetic field in Magnetostatics

Current is the source of maganetic field

.. math::
   \nabla \times \vec B = \frac{4\pi}{c} \vec j .




Potentials
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Electric Potential

Electric potential is given by

.. math::
   \vec E = -\nabla \phi.

Imediately, we have the curl of electrical field being 0, i.e.,

.. math::
   \nabla\times \vec E = 0.


By implementing Gauss's law, the equation for potential becomes

.. math::
   \nabla^2 \phi = - 4\pi \rho .

The solution, apply the Green's function to Laplace equation,

.. math::
   \phi(\vec x) = \int d^3x' \frac{\rho(\vec x')}{\lvert \vec x - \vec x'  \rvert}

2. Magnetic Potential

Magnetic potential is given by

.. math::
   \vec B = \nabla \times \vec A .


Applying curl of magnetic field and solving the equation,

.. math::
   \vec A = \frac{1}{c}\int \frac{\vec j}{\lvert \vec x - \vec x' \rvert} d^3 x' .



Gauge of fields
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

By definition, electric potential and maganetic potential are, repectively,

.. math::
   \vec E = -\nabla \phi ,

.. math::
   \vec B = - \nabla \times \vec A .


Electric field is invariant under a transform

.. math::
   \phi' = \phi + \phi_0,

where :math:`\nabla\phi_0=0`.

Similarly, the potential for magnetic field is

.. math::
   \vec A' = \vec A + \nabla \psi,

in which :math:`\psi` can be any scalar fields.


.. admonition:: Gauge
   :class: note

   As expected, these definitions of fields do not determine the potential completely. This is gauge freedom.

   **It might seem strange to talk about such a freedom. As we would ask why we have such freedom for potentials?**

   In class electrodynamics, potentials are merely mathematical tools. So the notion that potental has gauge freedom comes only from the mathematical definition of potentials.

   However, we do expect such a freedom is part of nature as we step into quantum ralm. In quantum world, Aharonov-Bohm effect proves that potentials are actually real existance. In such cases, the gauge freedom do have a very important impact on our theory. Gauge freedom is part of the internal structure of fields and goes deep into group theory, topology and differential geometry.




Multipole Expansion
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. admonition:: Requirement
   :class: warning

   One should be able to derive these multipole expansions of fields without refering to any material.

In the expression for potentials,

.. math::
   \phi(\vec x) = \int d^3x' \frac{\rho(\vec x')}{\lvert \vec x - \vec x'  \rvert},

and

.. math::
   \vec A = \frac{1}{c}\int \frac{\vec j}{\lvert \vec x - \vec x' \rvert} d^3x',

the term

.. math::
   \frac{\vec j}{\lvert \vec x - \vec x' \rvert}

can be Taylor expanded when :math:`\vec x' \ll \vec x`,

.. math::
   &\frac{1}{\lvert \vec x - \vec x' \rvert} \\
   =&  \frac{1}{r} - x'_i \partial_i \frac{1}{r} + \frac{1}{2} x'_i x'_j \partial_i \partial_j \frac{1}{r} + cdots

where :math:`1/r` is :math:`1/\lvert x \rvert` .


Apply this expansion, we can find the dipole and quadrapole of a charge distribution, which are

.. math::
   \vec p = \int \rho(\vec x') \vec x' d^3 x',

.. math::
   Q_{ij} = \frac{1}{2} \int \rho(\vec x') ( 3x'_i x'_j - r'^2 \delta_{ij}) d^3x'.

The corresponding potentials are

.. math::
   \vec \phi_d = \frac{\vec p\cdot \vec x}{r^3},

and

.. math::
   \vec \phi_q = \frac{x_i Q_{ij} x_j }{r^5}.

The electric field can be calculated using :math:`\vec E = -\nabla \phi`.




For magnetic field, a dipole expansion shows that

.. math::
   \vec A = \frac{\mu\times \vec x}{r^3},

where

.. math::
   \vec \mu  = \frac{1}{2c} \int \vec x' \times \vec j(\vec x') d^3 x'.



Force and Torque
~~~~~~~~~~~~~~~~~~~~~~

.. admonition:: Requirement
   :class: warning

   1. Write the most general expression for force and torque.
   2. Derive the expression with dipole and quadrapole approximations.

   Among the tricks, virtual work principle could be a nice one.


Force and torque can be calculated using virtual work principle. However, for dipoles, they can be calculated directly.









