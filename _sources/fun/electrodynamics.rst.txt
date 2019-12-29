Electrodynamics
***********************

Electrodynamics in 2+1 Spacetime
======================================================




Maxwell's equations are mostly experiment determined, except for one term by Maxwell involves the induced current. The only hope to write down a real 2+1 electrodynamcs formalism is to really understand the most fundamental properties of electrodynamics which I don't have at this moment.

So I turned to another approach. First of all we need to reach some basic agreement that which is not changed from our 3+1 theory to a 2+1 theory. As this being said, there could be a bunch of different versions of 2+1 theory.

To make sure we have a consistant theory, the following terms should be applied.

1. Something should be unchanged which will act as a connection between our 2+1 theory and 3+1 theory.



.. admonition:: Maxwell's Theory
   :class: note

   The equations could be written as

   .. math::
      \partial_\mu F^{\mu\nu} = 0,

   where :math:`F_{\mu\nu} = \partial_\mu A_\nu -\partial_\nu A_\mu`.

   However we would like to check the four laws independently since we really need to look into the meaning of the equations.

   .. math::
      \partial_i E_i & = 4\pi \rho\\
      \partial_i B_i & = 0 \\
      \epsilon_{ijk} \partial_j E_k  &= -\frac{1}{c} \partial_t B_i \\
      \epsilon_{ijk} \partial_j B_k & = \frac{4\pi}{c} J_i + \frac{1}{c} \partial_t E_i .


   Here we write down the component form because the cross product doesn't have a clear meaning as we move to different dimensions.







The first naive version
--------------------------


.. admonition:: Assumptions
   :class: note

   1. The dimension of energy is not changed.
   2. The dimension of length and time are kept.



Gauss's Law
~~~~~~~~~~~~~~~~~~~~~~~~~~


**Gauss's law** shows the source of the electric field, which should be in the form

.. math::
   \oint \vec E\cdot \vec {dl} = 2\pi \int \rho dS.

We have :math:`2\pi` instead of :math:`4\pi` is because we have only a integral of a closed loop not a closed surface.




.. admonition:: Applying Stokes Theorem?
   :class: note

   At first thought, we need to math the integral on the two sides thus Stokes theorem should be applied.

   Surprisingly, we don't really get to the familiar Gauss's law of differential form. Instead, we have

   .. math::
      \iint \nabla \times \vec E \cdot \vec{dS} = 2\pi \int \rho dS.



   BUT think about this. Is this really true? We DO NOT have a third dimension! How could we define a curl? Back to the component form,

   .. math::
      \nabla \times \vec E = \hat{e_i} \epsilon_{ijk} \partial_j E_k.

   As a reminder,

   .. math::
      \epsilon_{ijk} = \begin{cases}
      +1 & \text{if } (i,j,k) \text{ is } (1,2,3), (2,3,1) \text{ or } (3,1,2), \\
      -1 & \text{if } (i,j,k) \text{ is } (3,2,1), (1,3,2) \text{ or } (2,1,3), \\
      \;\;\,0 & \text{if }i=j \text{ or } j=k \text{ or } k=i
      \end{cases}


   Now the problem is we have all the elements of this Levi-Civita symbol 0 because only 2 dimensions can be used in this theory.

   That means we have no Gaussian theorem or no charge as a naive interpretation if we follow our idea that charge is source of static curl free electric field and followed up by using Stokes theorem.

   **This argument is WRONG. We need to reconsider the meaning of equations. This is 2D we don't have a third dimension to use Stokes theorem. We need divergence theorem.**


Two match up the dimensions we do need to apply the divergence theorem, in 2D.

.. math::
   \oint \vec E\cdot \vec {dl} = \iint \partial_i E_i dS,

from which we are able to determine the differential form

.. math::
   \partial_i E_i = 2\pi\rho,

in which we have :math:`i=1,2`.

.. admonition:: Vectors in 2D
   :class: note

   TBD











Faraday's Law
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The change of magnetic flux generate electric field,

.. math::
   \oint \vec E \cdot \vec{dl}  =  -\frac{1}{c} \frac{d}{dt} \int \vec B \vec{dS}.











Wave
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


We still have a wave solution.













Refs
------------------------


1. `Electrodynamics in 2D by Kirk T. McDonald @ Princeton <http://www.hep.princeton.edu/~mcdonald/examples/2dem.pdf>`_
