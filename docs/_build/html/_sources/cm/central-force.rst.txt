Central Force Fields
=======================================


Central force fields are widely used in physics and they have simple yet important properties.

In general, central force is described using

.. math::
   \vec F(\vec r) = f(r)\hat r.

The Lagrangian for an object of mass :math:`m` in a central force field is

.. math::
   L &= \frac{1}{2} m  \mathbf{ \dot r} ^2 - V(r) \\
   & = \frac{1}{2} m ( \mathbf{\dot r}^2 + r^2 \theta^2 ) - V(r) .


The interesting thing for such a system is that there is always a conserved quantity since the Lagrangian has no explicit :math:`\theta` dependence. It is obvious that

.. math::
   \frac{\partial L}{\partial \theta} = 0.

Now we have

.. math::
   \frac{d}{dt} \left(  \frac{\partial L}{\partial \dot{\theta}} \right) = 0,

which leads to the conservation of angular momentum as the first equation of motion,

.. math::
   \dot l \equiv \dot p_\theta = \frac{d}{dt} \left(  m r^2 \dot\theta  \right) = 0


The second equation of motion is given by

.. math::
   \frac{d}{dt} \left(  \frac{\partial L}{\partial \dot{r}} \right) - \frac{\partial L}{\partial r}  = 0,


which simplifies to

.. math::
   \frac{d}{dt} (m \dot r) - m r {\dot \theta}^2  + \frac{\partial V(r)}{\partial r} = 0.

Applying the conserved quantity, we find an effective potential

.. math::
   V_{eff} (r) = V(r) + \frac{1}{2} \frac{ l^2 }{ m r^2 }.
