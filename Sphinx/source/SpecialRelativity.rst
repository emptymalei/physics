********************
Special Relativity
********************





===============
Conventions
===============


Metric in special relativity

.. math::

   \begin{equation}\eta_{\mu\nu}=\left(\begin{matrix}
	-1 & 0 & 0 & 0\\
	0 & 1 & 0 & 0\\
	0 & 0 & 1 & 0\\
	0 & 0 & 0 & 1\\
   \end{matrix}\right)\end{equation}





Quantities and Operations
=========================

d'Alembertian
"""""""""""""""""""""""""

d'Alembert operator, or wave operator, is the Lapace operator in Minkowski space. [1]_

.. math::

   \Box\equiv \partial _ \mu\partial^\nu = \eta _{\mu\nu}\partial^\mu \partial^\nu


In the usual {t,x,y,z} natural orthonormal basis,

.. math:: 
   \begin{eqnarray}
    \Box&=&-\partial_t^2+\partial_x^2+\partial_y^2+\partial_z^2 \\
    &=&-\partial_t^2+\Delta^2 \\
    &=&-\partial_t^2+\nabla
   \end{eqnarray}


On wiki [2]_ , they give some applications to it.
	* klein-Gordon equation 
	  :math:`(\Box+m^2)\phi=0`
	* wave equation for electromagnetic field in vacuum:
	  For the electromagnetic four-potential $\Box A^\mu=0$\footnote{Gauge}
	* wave equation for small vibrations
	  :math:`\Box_c u(t,x)=0\rightarrow u_{tt}-c^2 u_{xx}=0`



Footnotes
==========

.. [1] Actually, there are more general definations for Lapacian, which includes this d'Alembertian of course.
.. [2] wiki:D'Alembert\_operator



