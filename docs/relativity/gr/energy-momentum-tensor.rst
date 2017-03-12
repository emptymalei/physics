Energy Momentum Tensor
========================


Energy momentum tensor is an important concept when dealing with continuum media.

In general, what we would like to define is a tensor that contains the energy density.

First of all, energy density obviously is not a conserved quantity. As an example, we consider a number of particles with number density :math:`n` and each with mass :math:`m`. In its comoving frame, we would define the energy density as :math:`\rho=n m` since every single particle is stationary. When we transform to another frame, say :math:`\bar O` frame, :math:`\bar\rho = \gamma^2 n m`, which indicates that this quantity is not a scalar.

So to achieve this goal of an invariant quantity, we need a tensor. Suppose its components are denoted as :math:`T^{\alpha\beta}`, we need to find a definition that carries the following meanings.

1. :math:`T^{00}` is energy density.
2. :math:`T^{0i}` is energy flux.
3. :math:`T^{i0}` is momentum density.
4. :math:`T^{ij}` is momentum flux. In this sense :math:`T{ii}` has the meaning of pressure.

For perfect fluid, the definition that satisfies the requirements is

.. math::
   T^{ab} = (\rho+p) U^a U^b + p g^{ab}.
