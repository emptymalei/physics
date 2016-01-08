****************************
Classical Mechanics
****************************

.. .. sectnum::
      :start: 3



Regid Body
==================================


Center of mass $\vec R$ is defined as

.. math::
   \int \rho(\vec r) \vec r d^3 \vec r = \int \rho(\vec r) \vec R d^3 \vec r .

Equivalently,

.. math::
   \int \rho(\vec r) \left( \vec r - \vec R \right) d^3 \vec r = 0.



Lagrangian and Equation of Motion
======================================================


Euler-Lagrangian equation is

.. math::
   \frac{d}{dt} \left(  \frac{\partial L}{\partial \dot{\boldsymbol r}} \right) - \frac{\partial L}{\partial \boldsymbol r} = 0.




Central Force Fields
=======================================


Central force fields are widely used in physics and they have simple yet important properties.

In general, central force is described using

.. math::
   \vec F(\vec r) = f(r)\hat r.

The Lagrangian for an object of mass :math:`m` in a central force field is

.. math::
   L &= \frac{1}{2} m \dot \boldsymbol{r} ^2 - V(r) \\
   & = \frac{1}{2} m ( \dot r^2 + r^2 \theta^2 ) - V(r) .


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








Oscillators
==========================


In general, the Lagragian for a system with n general coordinates can be

.. math::
   L = \frac{1}{2} m _ {jk} \dot q_j \dot q_k - V(q_1, \cdots, q_n)


To write down equation of motion, we need the following terms,

.. math::
   \frac{\partial L}{\partial \dot q_j} = m_{jk} \dot q_k
   \frac{\partial L}{\partial q_j} = \frac{1}{2} \frac{\partial m_{kl}}{\partial q_j} \dot q_k \dot q_l - \frac{\partial V}{\partial q_j}


Then equation of motion is

.. math::
   m_{jk} \ddot q_{k} + \frac{\partial m_{jk}}{\partial q_l} \dot q_k \dot q_l - \frac{1}{2} \frac{\partial m_{kl}}{\partial q_j} \dot q_k \dot q_l = - \frac{\partial V}{\partial q_j}

Generally, we can't solve this system. But there is an interesting limit. The system may have equilibrium points. We can study systems oscillating around equilibrium points.

At equilibrium, the system can stay steady, i.e., :math:`\dot q_j^0 = 0`. This gives us

.. math::
   \frac{\partial V}{\partial q_j} = 0 ,

for all j.

Now for small deviations, we can expand the system around equilibrium points.

.. math::
   q_j = q_j^0 + \eta _j

Then

.. math::
   T = \frac{1}{2} m_{jk} \vert _ 0 \dot \eta _ j \dot \eta_k \equiv \frac{1}{2} T_{jk} \dot \eta _ j \dot \eta _k

.. math::
   V = V\vert _0 + \frac{\partial V}{\partial q_j}\vert _ 0 \eta_j + \frac{1}{2} \frac{\partial ^ 2 V}{\partial q_j \partial q_k} \vert _ 0 \eta _ j \eta _ k + \cdots \equiv \frac{1}{2} V_{jk}\eta _ j\eta _ k

So we have the Lagrangian for small oscillations,

.. math::
   L = \frac{1}{2} T _ {jk} \dot \eta_j \dot \eta_k - \frac{1}{2} V_{jk}\eta_j \eta_k


Typing indices using LaTeX is so annoying. So we'll use matrix notations and Lagragian becomes

.. math::
   L = \frac{1}{2} \dot {\tilde \eta} T \dot \eta - \frac{1}{2} \tilde \eta V \eta ,

in which :math:`T` and :math:`V` matrices are n by n real and symmetric.

(We need to diagonalize T and V. First question comes to us is:

** Is is possible to diagonalize both T and V at the same time? **

We can have a look at the surface :math:`\tilde p T p = C`, which is a elliptical surface with coordinates :math:`p`.)

Use the following transformation

.. math::
   \xi = T^{1/2}\eta

Then transpose

.. math::
   \tilde \xi = \tilde \eta T^{1/2}

.. math::
   \dot{\tilde \xi} \dot \xi = \dot {\tilde \eta} T \dot \eta

So we have the new Lagragian

.. math::
   L = \frac{1}{2} \dot{\tilde \xi} \dot \xi - \frac{1}{2} \tilde \xi T^{-1/2} V T^{-1/2} \xi

Define :math:`T^{-1/2} V T^{-1/2} \equiv V'`.

Next we need to diagonalize V' by using its eigen vectors.

.. math::
   V' b = \lambda b

is equivalent to

.. math::
   V a = \lambda T a

with :math:`b = T^{1/2} a`. So we have

.. math::
   \det(V' - \lambda \mathbf I) = 0

is same as

.. math::
   \det(V - \lambda T) = 0

in which :math:`\lambda` is the eigen value of this function.









Hamiltonian Dynamics
=====================

Hamiltonian equations are

.. math::
   \dot q_i &= \frac{\partial H}{\partial p_i} \\
   \dot p_i &= -\frac{\partial H}{\partial q_i}.

Some constant of motion can be read out from the equations by recogonizing the fact that the time derivative of a constant of motion, $q_i$ or $p_i$, is zero. For example, if the Hamiltonian doesn't explicitly depend on $p_k$, we have $\frac{\partial H}{\partial p_k} = 0 = \dot q_k$, which means that $q_k$ is a constant of motion.


The evolution of the system in phase space obeys the Liouville's theorem, which describes the motion of phase space density $\rho(\{q_i\}, \{p_i\}, t)$,

.. math::
   \frac{d\rho}{dt} = 0.


.. admonition:: Phase Space Density
   :class: notes

   The probability that the system will be found in a phase space interval $d^n p d^n q$ is given by $\rho(\{q_i\},\{ p_i\},t) d^n p d^n q$.





Oscillators
========================


Harmonic oscillators are described by

.. math::
   -k x = m \ddot x,

which has solution

.. math::
   x = x(t=0) e^{i\omega x},

where $\omega = \pm \sqrt{ \frac{k}{m} }$ and the final solution is determined by the second initial condition, i.e., the first order derivative of displacement.






Refs & Notes
==================
