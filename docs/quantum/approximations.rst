Quantum Approximation Methods
==================================


Variational Method
-------------------

Trial functions
~~~~~~~~~~~~~~~~~

Some of the calculable trial functions:

1. :math:`\psi(x) = \cos\alpha x`, for :math:`|\alpha x|<\pi/2`, otherwise 0.
2. :math:`\psi(x) = \alpha^2 - x^2`, for :math:`|x|<\alpha`, otherwise 0.
3. :math:`\psi(x) = C \exp(-\alpha x^2/2)`.
4. :math:`\psi(x) = C(\alpha - |x|)`, for :math:`|x|<\alpha`, otherwise 0.
5. :math:`\psi(x) = C\sin\alpha x`, for :math:`|\alpha x|<\pi`, otherwise 0.





Procedure
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

1. Pick a trial function.

   .. note::
      How to pick a trial function? For ground state energy, we should pick a function that has the same property as the real ground state. This requires some understanding of the problem we are dealing with.

      Things to consider:

      a. The new problem is just a modification of a known solved problem. Then we can easily find out what really is different and interprete the new problem in terms of the old one.

      b. If the Hamiltonian have definite parity, the ground state wave function should pick up some parity which is usually even to make it the lowest energy.

      c. Continious function? A :math:`C^\infty` Hamiltonian can only have continious functions as solutions for a finite system.

      d. Nodes deteremines the kinetic energy so check the nodes for ground state wave function.

      e. Check the behivior of the wave function at different limits. In most cases, the Shrödinger equation can be reduced to something solvable at some limits.

      f. **One more thing, the trial function should make the problem calculable.**




Why Not General Viriational Method
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Why don't we just use a most general variational method to find out the ground state? Because we will eventually come back to the time-independent Shrödinger equation.

Suppose we have a functional form

.. math::
   E(\psi^*, \psi, \lambda) = \int dx \psi^* H \psi - \lambda \left( \int dx \psi^* \psi - 1 \right)

The reason we have this Lagrange multiplier method is that the wave function should be normalized and this multiplier provides the degree of freedom. We would only get a wrong result if we don't include this DoF.

Variation of :math:`\psi^*`,

.. math::
   \delta E = \int dx \delta \psi^* H \psi - \int dx \delta \psi^* \psi = 0

Now what?

.. math::
   H \psi - \lambda \psi = 0

Not helpful.



Variational Method and Virial Theorem
---------------------------------------

For a potential :math:`V(x)=b x^n`, we can prove that virial theorem is valid for ground state if we use Gaussian trial function :math:`e^{- \alpha x^2/2}`.

A MMA proof is `here <assets/mma/variational.nb>`_.


Virial theorem is pretty interesting. It shares the same math with equipartition theorem.



WKB
----------------


This is a semi-classical method. It is semi classical because we will use the classical momentum

.. math::
   \hbar k(x) = \sqrt{2m (E - V(x))}


The following points are important for this method.

0. WKB start from a classical estimation of wave number at a certain energy :math:`E` which is later quantified by the Bohr-Sommerfeld quantization rule.

1. Conservation law:

   .. math::
      \frac{\partial}{\partial t}\rho + \nabla \cdot \vec j = 0

   where :math:`\rho = \psi^* \psi`, :math:`\vec j = -\frac{\hbar}{2 m i} \left( \psi \nabla \psi^* - \psi^* \nabla \psi \right)`. This can be derived from Shrödinger equation easily.


2. Phase:
   Wave function is generally :math:`A(x)\exp(\phi(x))`. However, :math:`\phi(x)` should be the area of the phase function starting from some initial point. For example in WKB, :math:`k(x) = \phi'(x)` and :math:`\phi(x) = \int \phi'(x')d x' = \int k(x') d x'`.

   Using this general wave function and conservation law we find out that :math:`A(x) ~ \frac{1}{\sqrt{k(x)}}`. Then we can apply the two boundary conditions. However we will find two different wave functions given by two boundary conditions. Now we should connect them because :math:`\psi(a) = \psi(b)` exactly. By comparing the two wave functions we can find something like Bohr-Sommerfeld quantization rule.

3. Correction at bouldary:
   However, this method requires that the potential varies slowly or equivalently the wave number varies slowly. Basicly we are just using the following approximation:

   .. math::
      A'(x) = 0, k'(x) = 0


   For example when taking the derivative of wave function,

   .. math::
      \psi'(x) = A'(x) e^{i\int \cdots} + A(x) k(x) e^{i\int \cdots} \approx A(x) k(x) e^{i\int \cdots}

   where we drop the term with :math:`A'(x)`. That is to say

   .. math::
      |A'|\ll |A k| \Rightarrow |k'| \ll k^2

   But at boundary where :math:`E = V`, this is obviously not valid because :math:`k=0`. So we need to fix this problem.

   The solution is to use first order of the potential in a Taylor expansion. Then solve the problem exactly. Finally we connect regions that is far out from the boundary, need the boundary and between the boundary.


If we can have a good boundary condition, then the energy spectrum given by WKB can be very good. Even we don't have a good boundary condtion, the excited states given by this method are always close to the exact ones.



How does it work
~~~~~~~~~~~~~~~~~~~
