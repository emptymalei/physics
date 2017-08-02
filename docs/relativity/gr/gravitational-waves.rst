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

To solve the equation we introduce a solution of the form :math:`\har h^{\alpha\beta} = A^{\alpha\beta}e^{i k_\mu x^\mu }`, which simiplifies the equation

.. math::
   \eta^{\mu\nu} k_{\mu}k_\nu \bar h^{\alpha\beta} = 0.

To solve the amplitude :math:`A^{\alpha}` we need constraints on it.

The first one we can think of is a transverse condition,

.. math::
   A_{\alpha\beta} k^\beta = 0,

which removes 4 degrees of freedom.

The other conditions requires a gauge transformation. In any case, we have the second 
