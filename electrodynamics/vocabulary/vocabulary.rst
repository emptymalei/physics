Vocabulary
*******************



Units
=============


Gaussian Units
------------------------


Gaussian unit is very useful in electrodynamics. Back to two equations used in SI unit system to define some standard units,

.. math::
   F_e &= k_e \frac{Q q}{r^2} \\
   F_m &= k_m \frac{2 I_1 I_2 L_2}{\rho},

where we have the two constants defined as :math:`k_e = \frac{1}{4\pi \epsilon_0}` and :math:`k_m = \frac{\mu_0}{4\pi}`.

The idea of Gaussian unit is as simple as setting :math:`k_e=1` and :math:`k_m=1/c^2`. The consequences are, however,

.. math::
   \epsilon_0 & =\frac{1}{4\pi} \\
   \mu_0 &=\frac{4\pi}{c^2}.

These two equalities are the most useful ones to help us switch between SI and Gaussian.



Math
=================



Vector Analysis
----------------------

A lot of vector analysis equations will be deployed in this subject. The way to quickly prove a vector or tensor relation is to write down the component form, mess with the orders and use some specific relations.


One of the most useful symbol involved is Levi Civita symbol, which has a relation with the Kronecker delta,

.. math::
   \epsilon_{ijk}\epsilon_{lmn} = \begin{vmatrix}
   \delta_{il} & \delta_{im} & \delta_{in} \\
   \delta_{jl} & \delta_{jm} & \delta_{jn} \\
   \delta_{kl} & \delta_{km} & \delta_{kn}
   \end{vmatrix}.

As an example, we consider the case :math:`i=l`, the determinant reduces to

.. math::
   \epsilon_{ijk}\epsilon_{imn} = \begin{vmatrix}
   \delta_{jm} & \delta_{jn} \\
   \delta_{km} & \delta_{kn}
   \end{vmatrix} = \delta_{jm}\delta_{kn} - \delta_{jn}\delta_{km} .

This relation is useful in many situations.

.. math::
   \vec a \times (\vec b \times \vec c) &=  \hat e_i \epsilon_{ijk} a_j (\epsilon_{kmn} b_m c_n ) \\
   &=  \hat e_i \epsilon_{kij}\epsilon_{kmn} a_j b_m c_n \\
   &=  \hat e_i ( \delta_{im}\delta_{jn} - \delta_{in}\delta_{jm} )a_j b_m c_n \\
   &=  \hat e_i \delta_{im}\delta_{jn} a_j b_m c_n -  \hat e_i \delta_{in}\delta_{jm} a_j b_m c_n \\
   &=  \hat e_i a_j b_i c_j - \hat e_i a_j b_j c_i \\
   &=  \vec b (\vec a\cdot \vec c) - \vec c (\vec a \cdot \vec b) .



Integrals
----------------------

Gaussian integral is

.. math::
   \int_{-\infty}^\infty e^{-x^2/a^2} dx  =  a\sqrt{\pi}.

To calculate higher orders we can use parity and derivitives.

:math:`x^{2n +1}` are odd function thus 

.. math::
   \int_{-\infty}^\infty x^{2n+1} e^{-x^2/a^2} dx  =  0.


For those :math:`x^{2n}` we can use this derivative trick,

.. math::
   \int_{-\infty}^\infty e^{-x^2/a^2} dx  =  \left( \frac{-\partial}{\partial 1/a^2} \right)^2 \left(a\sqrt{\pi}\right).



E & M
==================


1. Static E field and B field,
2. Scalar potential and vector potential,
3. Multipole expansion,
4. Force of objects in E field and B field, both for arbitary field and each multipoles,
5. Torque of objects in E field and B field, both for arbitary field and each multipoles.


Radiation Pressure
======================

There are many ways to understand the pressure produced by light. In classical electrodynamics, we have the momentum current density, electromagnetic stress tensor, surface current density and quantum as the tools.

These are three different levels of the phenomenon.


Momentum Current Density
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Momentum current density is

.. math::
   \vec g = \frac{1}{8\pi c} \mathrm{Re}( \vec E^* \times \vec H ).


Pressure is force per unit area or momentum change per unit time per unit area. Momentum change, meanwhile, is momentum current density times volume.


To carry out in the language of math, the volume in time :math:`\Delta t` and on area :math:`a` is given by :math:`c \delta t a`, where c is the speed of light. Here we used c because we are basically considering the process in vacuum.

Pressure is given by

.. math::
   P &= \frac{\vec F\cdot \hat n}{a} \\
   & = \frac{\Delta \vec p \hat n }{\Delta t a} \\
   & = \frac{\hat n \cdot (\Delta \langle \vec g \rangle ) \Delta t c a}{\Delta t a} \\
   & = \hat n \cdot (\Delta \langle \vec g \rangle ).


The next step is to plug in the momentu current density and calculate the difference. **Here we calculate an example.**

Suppose we have our incident wave normal to the surface of perfect reflection. The wave has

.. math::
   \langle \vec g_1\rangle = - \langle \vec g_1' \rangle = -\frac{\vert \vec E_0 \vert^2 \hat n}{8\pi c}.

Finally the radiation pressure becomes

.. math::
   P = \frac{\vert \vec E_0 \vert ^2}{4\pi}.



Interaction Between Magnetic Field and Surface Current as Radiation Pressure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


On the surface of metal, electromagnetic waves could induce surface current which in return interacts with the magnetic component in the electromagnetic wave thus producing radiation pressure.


Surface current induced is calculated using 

.. math::
   \hat n \times (\vec B_1 - \vec B_2) = \frac{4\pi}{c} \vec K,

in which :math:`\vec B_2=0` since it is the magnetic field inside the good conductor.


The force is given by

.. math::
   \frac{a}{2} \frac{1}{2} \mathrm{Re}\left( \vec K^* \times \frac{\vec B_1+\vec B_2}{2} \right).

The average of magnetic field is the key point here. The reason behind this 1/2 factor is that infact only half of the magnetic field outside of the conductor is the original part while the other half is induced by the surface current density however the :math:`\vec B_1` includes all the magnetic field outside.

The pressure is

.. math::
   P = \frac{-\hat n \cdot \Delta \vec F}{a} =\frac{\vert \vec E_0 \vert^2}{4\pi}.



The Balance of Mechanic Pressure and Radiation Pressure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Due to conservation law, we have

.. math::
   \frac{d}{dt}(\vec P_{mech}+\vec P_{EM}) = \oint_S d\vec a\cdot \mathbf T,


which says the energy stress tensor integrated over a close surface on the interface of metal is the change in the momentum of mechanical part and electromagnetic part in total.


By using the monochromatic wave expression we can find the pressure.

.. math::
   P = \frac{\vert \vec E_0 \vert ^2}{4\pi}










Refs & Note
=================
