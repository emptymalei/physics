Electrodynamics
=============================



Note for electrodynamics course.


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





Books & Acknowledgement
==================================









Introduction
============


I am not expecting myself to typeset all the essential notes here but the key ideas that drive me somewhere.




ToC
======================


.. toctree::
    :maxdepth: 3

    vocabulary/main.rst
    em/main.rst
    matter.rst
    radiation.rst
    scattering.rst
    special_relativity.rst






------

------

.. figure:: _static/images/cc_byncsa.png
   :target: http://creativecommons.org/licenses/by-nc-sa/3.0/us/





-----

This open source project is hosted on GitHub: `electrodynamics <https://github.com/emptymalei/electrodynamics>`_ .


Read online: `Electrodynamics Notes <http://emptymalei.github.io/electrodynamics>`_ .

Download the `Latest PDF Version <https://github.com/emptymalei/electrodynamics/raw/master/_build/latex/electrodynamics.pdf>`_ .




Many thanks to open source project `Sphinx <http://sphinx-doc.org>`_ for it saves me a lot of time.

------

RST cheat sheet from `ralsina <https://github.com/ralsina/rst-cheatsheet>`_ .

`Page One <_static/images/rst-cheatsheet-1.png>`_

`Page Two <_static/images/rst-cheatsheet-2.png>`_
