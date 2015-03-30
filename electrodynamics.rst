**********************************
Electrodynamics
**********************************


At this moment, the update will be done here `Electrodynamics <http://electrodynamics.readthedocs.org/>`_ as a subproject and will be merged to this to this project when it is done.


Basics
=======================

Coulomb Potential Energy for a point charge Q with the appearance of a test charge q at distance r

.. math::
   V(r) = k \frac{q Q}{r}.

The ability to keep storage of charge is called capacitance, which is straight forward to have such a definition as

.. math::
   C = \frac{q}{U},

where :math:`U` is the electric potential (not the potential energy).


Maxwell's equations are

.. math::
   \mathbf{E}\cdot\mathrm{d}\mathbf{S} &= \frac{1}{\varepsilon_0} \iiint_\Omega \rho \,\mathrm{d}V \\
   \mathbf{B}\cdot\mathrm{d}\mathbf{S} &= 0 \\
   \oint_{\partial \Sigma} \mathbf{E} \cdot \mathrm{d}\boldsymbol{\ell} & = - \frac{d}{dt} \iint_{\Sigma} \mathbf{B} \cdot \mathrm{d}\mathbf{S} \\
   \oint_{\partial \Sigma} \mathbf{B} \cdot \mathrm{d}\boldsymbol{\ell} &= \mu_0 \iint_{\Sigma} \mathbf{J} \cdot \mathrm{d}\mathbf{S} + \mu_0 \varepsilon_0 \frac{d}{dt} \iint_{\Sigma} \mathbf{E} \cdot \mathrm{d}\mathbf{S}


or

.. math::
   \nabla \cdot \mathbf{E} &= \frac {\rho} {\varepsilon_0} \\
   \nabla \cdot \mathbf{B} &= 0 \\
   \nabla \times \mathbf{E} &= -\frac{\partial \mathbf{B}} {\partial t} \\
   \nabla \times \mathbf{B} &= \mu_0\left(\mathbf{J} + \varepsilon_0 \frac{\partial \mathbf{E}} {\partial t} \right)








Ref & Notes
=================
