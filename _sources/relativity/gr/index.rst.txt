General Relativity
*******************

General relativity is a theory of gravity. The idea is to find a set of "proper" coordinate system to describe physics on a curved space and make connection between these "proper" coordinate systems.


.. toctree::
   :maxdepth: 2

   geometrized-unit.rst
   gr-principles.rst
   gr-math.rst
   curved-spacetime.rst
   energy-momentum-tensor.rst
   gravitational-waves.rst
   general-relativity-revisted.rst
   spherical-solutions.rst
   black-holes.rst







Fields and Particles
============================================


Energy-Momentum Tensor for Particles
-------------------------------------

.. math::
   S_p \equiv -m c \int \int \mathrm d s\mathrm d\tau \sqrt{-\dot x ^\mu g_{\mu\nu} \dot x^\nu} \delta^4(x^\mu - x^\mu (s))    ,


in which :math:`x^\mu(s)` is the trajectory of the particle. Then the energy density $\rho$ corresponds to :math:`m\delta^4(x^\mu- x^\mu(s))`.

The Largrange density

.. math::

   \mathcal L = -\int\mathrm ds mc \sqrt{-\dot x^\mu g_{\mu\nu}\dot x^\nu}\delta^4(x^\mu - x^\mu(s))


Energy-momentum density is :math:`\mathcal T^{\mu\nu} = \sqrt{-g}T^{\mu\nu}` is

.. math::
   \mathcal T^{\mu\nu} = -2 \frac{\partial \mathcal L}{\partial g_{\mu\nu}}


Finally,

.. math::
   \mathcal T^{\mu\nu} &= \int \mathrm ds \frac{mc\dot x^\mu \dot x^\nu}{\sqrt{-\dot x^\mu g_{\mu\nu} \dot x^\nu}} \delta(t-t(s))\delta^3(\vec x - \vec x(t)) \\
   &= m\dot x^\mu \dot x^\nu \frac{\mathrm d s}{\mathrm d t} \delta^3(\vec x - \vec x(s(t)))






Theorems
=========


Killing Vector Related
------------------------


:math:`\xi^a` is Killing vector field, :math:`T^a` is the tangent vector of geodesic line. Then :math:`T^a\nabla_a(T^b\xi_b)=0`, that is :math:`T^b\xi_b` is a constant on geodesics.






Specific Topics
=================

Redshift
---------

In geometrical optics limit, the angular frequency :math:`\omega` of a photon with a 4-vector :math:`K^a`, measured by a observer with a 4-velocity :math:`Z^a`, is :math:`\omega=-K_aZ^a`.


Stationary vs Static
---------------------

Stationay
~~~~~~~~~~~~~

"A stationary spacetime admits a timelike Killing vector field. That a stationary spacetime is one in which you can find a family of observers who observe no changes in the gravitational field (or sources such as matter or electromagnetic fields) over time."

When we say a field is stationary, we only mean the field is time-independent.


Static
~~~~~~~~~~~

"A static spacetime is a stationary spacetime in which the timelike Killing vector field has vanishing vorticity, or equivalently (by the Frobenius theorem) is hypersurface orthogonal. A static spacetime is one which admits a slicing into spacelike hypersurfaces which are everywhere orthogonal to the world lines of our 'bored observers'"

When we say a field is static, the field is both time-independent and symmetric in a time reversal process.
