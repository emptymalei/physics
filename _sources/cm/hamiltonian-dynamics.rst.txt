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
