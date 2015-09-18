Radiation
===============


Usually, radiation is something that can be propagated to infinity, which means, those wave that drops according to :math:`\frac{1}{r^3}` or even faster won't get propagated to very far away. But we still might be interested in those near fields.

Understand retarded time is something always good for radiation study.

.. math::
   t_{ret} = t - \frac{\lvert  \vec x - \vec x' \rvert}{c},

which means retarded time is the current time minus the travel time of the radiation.

The mathematical reason for this retardation is that the Green's function for electromagnetic wave,

.. math::
   \left( \nabla ^2 - \frac{1}{c^2} \frac{\partial^2}{\partial t^2}  \right)  A = 0 .

This is for the fields in vacuum. For radiation with source, the wave equations gains a source term. To solve the equation, I need to write down the Green's function, which, in this case, has a retarded term in it. In fact all such waves have a retarded time in it even just by looking at the math. Retarded time has a great impact on the solution since it delays the effect of source.

This is also causality.


Radiation In General
------------------------------------------------------------

In general the wave equation with a source is

.. math::
   \left( \nabla^2 - \frac{1}{c^2}\partial_t^2  \right)  A^{\mu} = - s^{\mu}.

By solving that, the retarded solution comes into effect,

.. math::
   A^{\mu} = \int d^3x' \frac{ s^{\mu}(t_{ret}, \vec x') }{\lvert   \vec x - \vec x' \rvert} .


Here the vector potential is

.. math::
   \vec A =  \int \frac{ \vec j (t_{ret}, \vec x')/c }{\lvert   \vec x - \vec x' \rvert},

while the scalar potential is

.. math::
   \phi =  \int \frac{ \rho (t_{ret}, \vec x')}{\lvert   \vec x - \vec x' \rvert}.


.. admonition:: Static Fields
   :class: note

   The static field has similar structure except we have no retardation. Here are the expressions.



The important thing in radiation is the angle depenence of radiation power or total radiation power. To find that, there are many procedures.

One of them is to use the fact that electric field in radiation is always transverse which means

.. math::
   \vec E = -\hat r \times \vec B.

So we only need to find out the magnetic field thus the first thing is to calculate the vector potential.

.. admonition:: Why B field first?
   :class: note

   We can also find out electric field first. But in dynamics,

   .. math::
      \vec E = - \nabla \phi - \partial_t \vec A,

   which means we need to find both :math:`\phi` and :math:`\vec A`.

   While in the procedure stated previously, we only need :math:`\vec A`.

To summarize, here is the procedure.

1. Calculate :math:`\vec A`.
2. Find magnetic field using :math:`\vec B = \nabla \times \vec A`.
3. Find electric field is needed using :math:`\vec E = - \hat r \times \vec B`.
4. Find Poynting vector :math:`\vec S = \frac{c}{4\pi} \vec E \times \vec B`.
5. Find radiation power :math:`\frac{dP}{d\Omega} = r^2 \langle \vec S \rangle \cdot \hat r`, which is angle dependent in general.


.. admonition:: Zangwill's Method
   :class: note

   There is a radiation vector method in Zangwill's *Modern Electrodynamics* book.






Dipole Radiation
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Dipole Radiatioin Can Be Calculated Exactly.





Approximations
~~~~~~~~~~~~~~~~~~~~~~~~~~~


Since we are talking about radiation which is radiated away. Looking at a far zone radiation is good.

Define :math:`r = \lvert \vec x \rvert`. Expanding the vector potential, we have the multipole expansion of the vector potential in the limit that :math:`\lvert \vec x' \rvert \ll \lvert \vec x\rvert` is all true for the whole integral,

.. math::
   \vec A &\approx \frac{1}{cr} \int d^3x' \vec j(t-r/c+ \hat r\cdot \vec x'/c,\vec x') \\
   &\approx \frac{1}{cr} \int d^3 x' \left( \vec j(t-r/c, \vec x') + \frac{\hat r \cdot \vec x'}{c} \partial_t \vec j(t-r/c,\vec x')  \right)


So the vector potential under this degree of approximation can be splited into two terms at this point.

.. math::
   \vec A_{E1} =  \frac{1}{cr} \int d^3 x' \vec j(t-r/c, \vec x'),


is the electric dipole. 

.. admonition:: Electric Dipole Radiation
   :class: note

   The reason is the conservation of charge. Consider this relation,

   .. math::
      \nabla \cdot \vec j + \partial_t \rho = 0.

   Combine this with the following trick,

   .. math::
      \partial_i (j_i x_k ) = x_k \partial_i j_i + j_k,

   and the fact that 

   .. math::
      \oint j_i x_k \d\Sigma_i =0,

   for any surface that is large enough.

   We have the following relation

   .. math::
      \int d^3x ( j_k - x_k \partial_t \rho) = 0.

   Then we know that

   .. math::
      \int \vec j d^3 x = \dot{\vec p}.



    






.. math::
   \vec A_2 &=  \frac{1}{cr} \int d^3 x' \frac{\hat r \cdot \vec x'}{c} \partial_t \vec j(t-r/c,\vec x') \\
   & = \frac{1}{c^2r} \int d^3x' \hat r \cdot \vec x' \partial_t \vec j(t-r/c,
   \vec x').


A trick can be applied to this expression,

.. math::
   \frac{1}{2}\hat r \times (\vec x ' \times \vec j) = \frac{1}{2} (\hat r \cdot \vec x' ) \vec j - \frac{1}{2} (\hat r \cdot \vec j) \vec x' .

Recall that magnetic dipole is by definition

.. math::
   \vec \mu = \frac{1}{2c} \int d^3x' \vec x' \times \vec j.

We would like to have a term similar to the electric dipole, but we have a term like :math:`\hat r \times 2c \vec \mu` in :math:`\vec A_2`. So we take one step furthur.

.. math::
   \frac{1}{2}\hat r \times (\vec x ' \times \vec j) & = (\hat r\cdot \vec x') \vec j - \frac{1}{2} (\hat r\cdot \vec x') \vec j - \frac{1}{2} (\hat r \cdot \vec j) \vec x' \\
   & = (\hat r\cdot \vec x') \vec j - \frac{1}{2} \left( (\hat r\cdot \vec x') \vec j - (\hat r \cdot \vec j) \vec x' \right).

So the term :math:`\vec A_2` becomes

.. math::
   \vec A_2 & = \frac{1}{c^2r} \int d^3x' \left(    \frac{1}{2}\hat r \times (\vec x ' \times \vec j) +  \frac{1}{2} \left( (\hat r\cdot \vec x') \vec j + (\hat r \cdot \vec j) \vec x' \right)  \right) \\
   & = \frac{1}{c^2r} \partial_t \left(   c \hat r\times \vec \mu_{ret}   \right)  + \frac{1}{c^2r} \partial_t \int d^3x' \left(   \frac{1}{2} \left( (\hat r\cdot \vec x') \vec j + (\hat r \cdot \vec j) \vec x' \right)   \right)  \\
   & =\vec A_{M1} + \vec A_{E2}.


Back to the procedure to find radiation power, we can find the radiation power for a specific case.





Lamor's Formula
------------------------------------------------------------


Charge Moving in Gravity Feilds
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


A charge q is moving in a constant gravity field.

Vector potential for a charge moving in gravitational field is

.. math::
   \vec A &\approx \frac{1}{c r} \int d^3x'  \vec j_{ret} \\
   & \approx \frac{1}{cr} q g (t - \frac{r}{c} ) \hat e_z.

The magnetic field is

.. math::
   \vec B &= \nabla \times \vec A \\
   & \approx \nabla t_{ret} \times \hat e_z \frac{q g }{cr} \\
   & \approx \frac{qg}{c^2r} (-\hat e_r \times \hat e_z) \\

Go on with the calculation,

.. math::
   \vec S \cdot \hat e_r &= \frac{c}{4\pi} \vec E\times \vec B \\
   & = \frac{q^2g^2}{4\pi c^3r^2}  \sin^2\theta

Then we have the radiation power

.. math::
   \frac{dP}{d\Omega} =  \frac{q^2 g^2}{4\pi c^3}\sin^2\theta.

   















.. end of file
