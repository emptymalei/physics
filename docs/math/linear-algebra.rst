Linear Algebra
====================


Basic Concepts
------------------




Trace
~~~~~~~~

Trace should be calculated using the metric. An example is the trace of Ricci tensor,

.. math::
   R=g^{ab}R_{ab}


Einstein equation is

.. math::
   R_{ab}-\frac{1}{2}g_{ab}R=8\pi G T_{ab}

The trace is

.. math::
   g^{ab}R_{ab}-\frac{1}{2}g^{ab}g_{ab}R &= 8\pi G g^{ab}T_{ab} \\
   \Rightarrow R-\frac{1}{2} 4 R  &=  8\pi G T \\
   \Rightarrow -R &= 8\pi GT



Technique
------------

Inverse of a matrix
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Many methods to get the inverse of a matrix. Check wikipedia for Invertible matrix.

Adjugate matrix method for example is here.

.. math::
   A^{-1} = \frac{A^*}{|A|}

in which, :math:`A^*` is the adjugate matrix of :math:`A`.


Eigenvalues of :math:`A^\dagger A`
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

One can prove that the eigenvalues of any matrix :math:`B` that can be written as :math:`A^\dagger A` are positive semidefinite.

.. admonition:: Proof
	:class: toggle

	Suppose the eigenvectors are :math:`V_i` with corresponding eigenvalues :math:`\lambda_i`, i.e.,

	.. math::
		B V_i = \lambda_i V_i.

	We now construct a number 

	.. math::
		V_i^\dagger B V_i.

	On one hand, we have

	.. math::
		V_i^\dagger B V_i = V_i^\dagger \lambda_i V_i = \lambda_i  V_i^\dagger V_i,

	where :math:`V_i^\dagger V_i \geq 0`.

	On the other hand, 

	.. math::
		V_i^\dagger B V_i = V_i^\dagger A\dagger A V_i = (A V_i)^\dagger A V_i \geq 0.

	As long as :math:`V_i^\dagger V_i \neq 0`, we have

	.. math::
		\lambda_i = (A V_i)^\dagger A V_i  / V_i^\dagger V_i \geq 0.
	





.. _TensorProductSpace:

Tensor Product Space
-----------------------




:math:`\ket{\phi}_1` and :math:`\ket{\phi}_2` are elements of Hilbert space :math:`H_1` and :math:`H_2`. **Tensor Product** of :math:`\ket{\phi}_1` and :math:`\ket{\phi}_2` is denoted as :math:`\ket{\phi}_1\otimes \ket{\phi}_2`. This operation is linear and distributive.

**Tensor product space** :math:`H_1\otimes H_2` is composed of all the linear combinations of all possible tensor products of elements in :math:`H_1` and :math:`H_2`.


Inner Product
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Inner product of two tensor products

.. math::
   (\bra{\phi}_1\otimes \bra{\phi}_2)(\ket{\psi}_1\otimes \ket{\psi}_2) = ( {} _ 1 \braket{\phi}{\psi}_1)({}_2\braket{\phi}{\psi}_2)


Operators Applied to Tensor Product
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Two operators :math:`\hat O_1` and :math:`\hat O_2` works on :math:`H_1` and :math:`H_2` respectively applied to tensor product

.. math::
   (\hat O_1 \otimes \hat O_2 )( \ket{\phi}_1\otimes \ket{\phi}_2 ) = (\hat O_1 \ket{\phi}_1) \otimes (\hat O_2 \ket{\phi}_2)





Solving Linear Equations
------------------------------

First of all, write down the augmented matrix for the equation set.

Elementary row operations are allowed on the augmented matrix. Operate on the matrix until one can read out the solutions.
