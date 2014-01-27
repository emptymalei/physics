****************************
Classical Mechanics
****************************

.. .. sectnum::
      :start: 3




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

Phase space


























