Special Relativity
********************





Conventions
===============


Metric in special relativity

.. math::
   \eta_{\mu\nu}=\begin{pmatrix}
	-1 & 0 & 0 & 0\\
	0 & 1 & 0 & 0\\
	0 & 0 & 1 & 0\\
	0 & 0 & 0 & 1\\
   \end{pmatrix}





Quantities and Operations
--------------------------------------------

d'Alembertian
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

d'Alembert operator, or wave operator, is the Lapace operator in Minkowski space. [1]_

.. math::
   \Box \equiv \partial _ \mu\partial^\nu = \eta _{\mu\nu}\partial^\mu \partial^\nu


In the usual {t,x,y,z} natural orthonormal basis,

.. math::
   \Box & = -\partial_t^2+\partial_x^2+\partial_y^2+\partial_z^2 \\
   & = -\partial_t^2+\Delta^2 \\
   & = -\partial_t^2+\nabla



On wiki [2]_ , they give some applications to it.
	* klein-Gordon equation
	  :math:`(\Box+m^2)\phi=0`
	* wave equation for electromagnetic field in vacuum:
	  For the electromagnetic four-potential $\Box A^\mu=0$\footnote{Gauge}
	* wave equation for small vibrations
	  :math:`\Box_c u(t,x)=0\rightarrow u_{tt}-c^2 u_{xx}=0`





Basics
==================================

.. admonition:: A Coincidence?
   :class: note

   Let's start from this coincidence.

   .. figure:: sr/specialRelativityVelocityAddition.png
      :align: center

      Addition of velocities

   Recall that in special relativity, velocity addition is

   .. math::
      v_S = \frac{u+v_O}{1+ \beta v/c},

   where :math:`v_S` is the velocity measured in moving frame S, :math:`v_O` is the velocity measured in frame O. This :math:`\beta` is the factor :math:`u/c` where u is the velocity of the moving frame measure in frame O.

   At the same time, we have the following hyper trig relation.

   .. math::
      \tanh (\alpha + \beta) = \frac{\tanh \alpha + \tanh \beta}{1 + \tanh \alpha \tanh \beta}.

   Isn't this addition of angles the same as the velocity addition?


The algebra of relativity is mostly based on invariance of a new distance under a new rotation. Here we are not going to repeat the derivation of these transformations from the beginning, instead we would like to have a look at the really amazing part of the theory.


As we define

.. math::
   \tanh \alpha_u = \frac{u}{c},

and any velocity divided by speed of light to be a hyperbolic tangent,

.. math::
   \tanh \alpha_{v_x} = \frac{v_x}{c},

the velocity transformation, as stated in the admonition block, is an addition of angles

.. math::
   v_{S} = \tanh(\alpha_u + \alpha_{v_O}) = \frac{\tanh \alpha_{u} + \tanh \alpha_{v_0}}{1 + \tanh \alpha_{U} \tanh \alpha_{v_O}} = \frac{u/c + v_O/c}{1+ \frac{u}{c} \frac{v_{O}}{c}}.


However, addition of velocity is not that fundamental. We need to look into the relation

.. math::
   \tanh \alpha_{v_x} = \frac{v_x}{c}.


Since we are talking about geometry, space-time diagram will be extremely important.







Footnotes
==========

.. [1] Actually, there are more general definations for Lapacian, which includes this d'Alembertian of course.
.. [2] wiki:D'Alembert\_operator
