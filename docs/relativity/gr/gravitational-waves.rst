Gravitational Waves
==========================

In the weak field regime of sourceless Einstein's equation (:math:`T^{\mu\nu}=0`), the equation for metric with perturbations is reduced to a wave equation,

.. math::
   \left( - \frac{\partial^2}{ \partial t^2 } + \nabla^2 \right) \bar h^{\alpha\beta} = 0,

where :math:`\bar h^{\alpha\beta}` is the trace-reversed perturbation of the metric on top of Minkowski metric background, i.e.,

.. math::
   \bar h^{\alpha\beta} = h^{\alpha\beta} - \frac{1}{2} \eta^{\alpha\beta} h,

where :math:`h^{\alpha\beta} = g^{\alpha\beta} - \eta^{\alpha\beta}` and :math:`h` is the trace of metric perturbation :math:`h^{\alpha\beta}`.

.. admonition:: Trace Reverse
   :class: toggle

   The tensor :math:`\bar h^{\alpha\beta}` is called trace reverse of :math:`h^{\alpha\beta}` for its trace is :math:`-h`.


Gauge
---------------------

To solve the equation we introduce a solution of the form :math:`\hat h^{\alpha\beta} = A^{\alpha\beta}e^{i k_\mu x^\mu }`, which simiplifies the equation

.. math::
   \eta^{\mu\nu} k_{\mu}k_\nu \bar h^{\alpha\beta} = 0.

To solve the amplitude :math:`A^{\alpha}` we need constraints on it. We can derive that gravitational waves are always null, that is :math:`k^\mu k_\mu=0`.


Some of the conditions requires a gauge transformation. In any case, we have the second gauge condition as

.. math::
   A_{\alpha\beta} U^{\beta} = 0,

which specifies that :math:`A_{\alpha\beta}` is orthogonal to the vector we chose :math:`U^{\beta}`. A practical choice of :math:`U^\beta` is a four velocity. This removes another **four degrees of freedom**. For illustration purpose, we choose :math:`U^{\beta} \to ( 1, 0, 0, 0 )` since it's a null vector. The degrees of freedom removed can be visualized as the first rwo and column.

The second one we can think of is a transverse condition,

.. math::
   A_{\alpha\beta} k^\beta = 0,

which removes **another three degrees of freedom**. This specifies that the wave is transverse, i.e., :math:`A_{\alpha\beta}` can not have elements that is in the direction of four wavevector. We specify a wavevector :math:`k^\beta \to (\omega, 0, 0, \omega )`, which leads to the removal of the remaining elements of the fourth row and column.

The matrix we have now becomes

.. math::
   A_{\alpha\beta} \to \begin{pmatrix}
   0 & 0 & 0 & 0 \\
   0 & A_{xx} & A_{xy} & 0 \\
   0 & A_{yx} & A_{yy} & 0 \\
   0 & 0 & 0 & 0
   \end{pmatrix}.

The last gauge condition is traceless condition :math:`A^\alpha_\alpha = 0` which also requires the gauge transformation. This condition fixes the phase relations between different spatial directions, that is $A_{xx} = e^{i\pi} A_{yy} = - A_{yy}$. This conditions insists that the two directions of distance oscillations should be quadrupole-like, i.e., contracts in one direction (say x) while extend in the other direction (say y).
