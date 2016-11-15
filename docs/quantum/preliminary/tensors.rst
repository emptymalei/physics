Tensors and Groups in Quantum
====================================================





A rank-k tensor :math:`\hat T_k^q` is defined as

.. math::
   \left[\hat J_z, \hat T_k^1 \right] &= q\hbar \hat T_k^q \\
   \left[ \hat J_{\pm}, \hat T_k^q \right] & = \sqrt{(k\mp q)(k\pm q + 1)}\hbar \hat T_{k}^{q\pm 1} .



Wigner-Eckart Theorem
-----------------------

Wigner-Eckart theorem is

.. math::
   \bra{n'j'm'}\hat T_k^q \ket{njm} = \bra{n'j'}\vert \hat T_k \vert \ket{nj} \braket{j'm';kj}{kq;jm},

where :math:`j,j'` are the angular momentum quantum numbers and :math:`n, n'` are quantum numbers which are not related to angular momentum.


It seems that tensor :math:`\hat T_k^q` is a source of angular momentum. The maximum angular momentum it can provide is :math:`k`.
