***************************
Quantum Mechanics 2
***************************






Tensor Product Space
==============================

This part has been moved to :ref:`TensorProductSpace`




Density Matrix
==============================






Angular Momentum
==============================






Angular Momentum
-----------------

For an new operator, we would like to know

1. Commutation relation: with their own components, with other operators;
2. Eigenvalues and their properties;
3. Eigenstates and their properties;
4. Expectation and classical limit.


Definition of Angular Momentum
""""""""""""""""""""""""""""""""

In classical mechanics, angular momentum is defined as

.. math:: \vec L = \vec X \times \vec P .

One way of defining operator is to change position and momentum into operators and check if the operator is working properly in QM. So we just define

.. math:: \hat {\vec L} = \hat {\vec X}\times \hat{\vec P}.

It is Hermitian. So it can be an operator. We also find

.. math:: \hat{\vec L}\times \hat{\vec L} = i \hbar \hat{\vec L}

.. math:: \left[\hat L_i,\hat L_j\right] = \sum_k i\epsilon_{ijk}\hat L_k    .

**More generally, we can define angular momentum as**

.. math:: \left[\hat J_i, \hat J_j\right] = i\hbar \sum_k \epsilon_{ijk} \hat J_k

We can prove that

.. math:: \left[ \hat J^2,\hat J_z \right] = 0.

So they can have the same eigenstates

.. math:: \hat J_z \ket{\lambda m} = m\hbar \ket{\lambda m}

.. math:: \hat J^2 \ket{\lambda m} = \lambda^2 \hbar^2 \ket{\lambda m}

To find the constraints on these eigenvalues, we can use positive definite condition of certain inner porducts, such as,

.. math:: \bra{\psi} \hat J_+ \hat J_- \ket{\psi} \geq 0

.. math:: \bra{\psi} \hat J_- \hat J_+ \ket{\psi} \geq 0

where

.. math:: \hat J_{\pm} = \hat J_x \pm i \hat J_y

and we have

.. math:: \left[\hat J_+, \hat J_-\right] = 2 \hbar \hat J_z

.. math:: \left[\hat J_z, \hat J_{\pm} \right] = \pm \hbar \hat J_{\pm}.

It's easy to find out that

.. math:: \hat J_z (\hat J_{\pm}\ket{\lambda m}) = (m\pm 1) \hbar (\hat J_{\pm} \ket{\lambda m})

i.e., :math:`\hat J_{\pm}\ket{\lambda m}` is eigenstate of :math:`\hat J_z`.

Follow the plan of finding out the bounds through these positive inner products, we can prove that

.. math:: \hat J^2\ket{jm} = j(j+1)\hbar^2 \ket{jm}

.. math:: \hat J_{\pm}\ket{jm} = \sqrt{j(j+1)-m(m\pm 1)} \hbar \ket{j,m\pm 1}




Eigenstates of Angular Momentum
""""""""""""""""""""""""""""""""


As we have proposed, the eigenstates of both :math:`\hat J_z` and :math:`\hat{\vec J}^2` are :math:`\ket{j,m}`, where :math:`j=0,1,2,\cdots` and :math:`m=-j,-j+1,\cdots, j-1,j`.

We can also find out the wave function in :math:`{\ket{\theta,\phi } }` basis. Before we do that, the definition of this basis should be made clear. This basis spans the surface of a 3D sphere in Euclidean space and satisfies the following orthonormal and complete condition.

.. math::
   \int \mathrm d \Omega \braket{\theta',\phi'}{\theta,\phi} = \delta(\cos\theta'-\cos\theta,\phi'-\phi)
   \int \mathrm d \Omega \ket{\theta',\phi'}\bra{\theta,\phi} = 1

Now we have an arbitary state :math:`\ket{\psi}`,

.. math::
   \ket{\psi} &= \sum _ {l,m} \psi _ {lm}\ket{l,m} \\
              &= \sum _ {l,m} \int \mathrm d \Omega \ket{\theta',\phi'}\bra{\theta,\phi} \psi _ {lm}\ket{l,m} \\
              &= \sum _ {l,m} \int \mathrm d \Omega \ket{\theta',\phi'} (\braket{\theta,\phi}{l,m} ) \psi _ {lm} \\

Then we define

.. math:: \braket{\theta,\phi}{l,m}=Y_l^m(\theta,\phi)

which is the spherical harmonic function.

Then 

.. math::
   \ket{\psi} &= \sum _ {l,m} \psi _ {lm} \int \mathrm d \Omega   Y_l^m(\theta,\phi) \ket{\theta',\phi'}  \\

So as long as we find out what :math:`\psi _ {lm}` is, any problem is done.
