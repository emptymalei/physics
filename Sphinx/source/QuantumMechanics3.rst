***************************
Quantum Mechanics 3
***************************






Approximations
==============================



.. math::
   \newcommand{\ud}[1]{{#1^{\dagger}}}
   \newcommand{\bra}[1]{\left\langle #1\right|}
   \newcommand{\ket}[1]{\left| #1\right\rangle}
   \newcommand\Tr{\mathrm{Tr}}
   \newcommand{\braket}[2]{\langle #1 \mid #2 \rangle}
   \newcommand\d{\mathrm{d}}
   \newcommand\I{\mathbb{I}}
   \newcommand{\avg}[1]{\left< #1 \right>}


Variational Method
-------------------


The idea comes from that

.. math::
   \avg{E} = \frac{\bra{\psi}\hat H\ket{\psi}}{\braket{\psi}{\psi}} = \frac{\sum_n \left| \braket{n}{\psi}  \right|^2}{\sum_n \left| \braket{n}{\psi} \right|^2} \geq E_n

if :math:`\ket{\psi}` is composed only with :math:`\ket{i}` (:math:`i\geq n`).




WKB Approximation
------------------

