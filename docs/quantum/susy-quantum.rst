Super-Symmetric Quantum Mechanics
==================================================

`Here is a note on this. <http://arxiv.org/abs/hep-ph/9907295>`_

The idea of supersymmetric quantum mechanics is to introduce a hamiltonian related to supercharge, which is defined through

.. math::
   [H,Q_i] = 0,

for all charges :math:`Q_i` and

.. math::
   {Q_i,Q_j} = \delta_{ij} H.

In the 2 charge case, I can define two charges,

.. math::
   Q_1 & = \frac{1}{2} (\sigma_1 p + \sigma_2 W(x) )\\
   Q_2 & = \frac{1}{2} (\sigma_2 p - \sigma_1 W(x) ).



.. admonition:: Harmonic Oscillators
   :class: note

   The harmonic oscillators can be solved using ladder operators,

   .. math::
      a &= \sqrt{i/2\hbar}(\hat p/\sqrt{m\omega}  -i\sqrt{m\omega}\hat x) \\
      a^\dagger & = \sqrt{-i/2\hbar}(\hat p/\sqrt{m\omega}  + i\sqrt{m\omega}\hat x).

   This is a hint why we define the charges in that way.


With these charges, we can solve the state that is annihlated by :math:`Q_1`.

.. math::
   Q\psi_0 = 0,

which is the ground state.

The result is

.. math::
   \psi_0(x) = exp(\int_0^x dy W(y)\sigma_3/\hbar) \psi_0(0).



