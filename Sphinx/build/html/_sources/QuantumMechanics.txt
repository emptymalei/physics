***************************
Quantum Mechanics
***************************

.. .. sectnum::
      :start: 4

Quantum Mechanics Framework
==============================



.. math::
   \newcommand{\ud}[1]{{#1^{\dagger}}}
   \newcommand{\bra}[1]{\left\langle #1\right|}
   \newcommand{\ket}[1]{\left| #1\right\rangle}
   \newcommand\Tr{\mathrm{Tr}}
   \newcommand{\braket}[2]{\langle #1 \mid #2 \rangle}
   \newcommand\d{\mathrm{d}}
   \newcommand\I{\mathbb{I}}




What're the most important tricks in QM calculations?
---------------------------------------------------------

* **Remember what basis we are working in**
* **Identity**


First Three Postulates
-------------------------

* Physical state is described by kets in a Hilbert space. We need to specify a complete basis {:math:`\ket{i}`} to do calculations.
  
  .. math:: \ket{\psi} = \sum_i \ket{i}\bra{i}\ket{\psi} = \sum_i C_i \ket{i}

* Operators are given by Hermitian operators; A measurement of the variable :math:`\hat \Omega` will yield one of the eigenvalues :math:`\omega` with the probability
  
  .. math:: \left|\braket{\omega}{\psi}\right|^2 .

  And the state of the system will change to :math:`\ket{\omega}`.
* The state vector obeys the Schrödinger equation,
  
  .. math:: i\hbar \frac{\d}{\d t}\ket{\psi(t)} = \hat H \ket{\psi(t)} ,

  where :math:`\hat H` is the Hamiltonian operator.


		The logic here is that we first find the way to describe a system, then think about how to find out the information we need from the state vector and also find the evolution of the state vector. Then we need the operator and Schrodinger equation. Finally, we would like to relate the theory to experiments, and it comes the measurement postulate.

		Later we will need the relation between position and momentum, which becomes the fourth postulate.
 
 


* How to solve the evolution of a system?
  We just define a magical operator, propagator

  .. math::
     \hat U \ket{\psi(t_0)} = \ket{\psi(t)} .

  This operator just gives us the evolution of state vector! Wait, can we write down the explicit expression of it?
	
  Let's find out. The only thing we know about the evolution of a state vector is the third postulate up there.
	
  .. math::
  
     \begin{eqnarray}
     i\hbar \frac{\d }{\d t}\ket{\psi(t)} &=& \hat H \ket{\psi(t)} \\\\
     i\hbar \frac{\d }{\d t}\hat U \ket{\psi(t_0)} &=& \hat H \hat U \ket{\psi(t_0)} \\\\
	 i\hbar \frac{\d }{\d t}\hat U &=& \hat H \hat U
	 \end{eqnarray}
 
  
  Looks familiar? This just gives us a exponential result, **if the Hamiltonian is time independent**.
 
  .. math:: \hat U = e^{- i \hat H (t-t_0)/\hbar}
 
  **We can prove that this operator is Unitary because** :math:`\hat H` **is Hermitian.**
 	
  This is just the abstract representation, we work in some basis, and the most convenient basis is the eigenstates of Hamiltonian, { :math:`\ket{\epsilon_i}` },

  .. math::
     \begin{eqnarray}
 	 \hat U \ket{\phi} &=& e^{- i \hat H (t-t_0)/\hbar} \ket{\psi}   \\\\
     \hat U \ket{\phi} &=& \sum_i e^{- i \hat H (t-t_0)/\hbar} \ket{\epsilon_i}\bra{\epsilon_i}  \ket{\psi}  \\\\
	 \hat U \ket{\phi} &=& \sum_i e^{- i \epsilon_i (t-t_0)/\hbar} \ket{\epsilon_i}\bra{\epsilon_i}  \ket{\psi}
     \end{eqnarray}
 	
  And we are going to use 

  .. math:: \hat U = \sum_i e^{- i \epsilon_i (t-t_0)/\hbar} \ket{\epsilon_i}\bra{\epsilon_i}

  from now on. (Well, only on discrete eigenvalues ones.)
 	
  **(See that? Identity does the work again.)**



Position and Momentum Space
-----------------------------


Summarize here.

-----

* Position
    1. Define {:math:`\ket{x}`} basis.
    2. Define :math:`\hat x` operator.
    3. Find wave function in this basis.
    4. Find measurement.
* Evolution
	1. Need propagator :math:`\hat U`.
	2. Propagator needs the solution of Hamiltonian eigensystem.
	3. (Free particles) Hamiltonian needs the solution of momentum eigensystem.
* Momentum
	1. Before we define some arbitrary momentum space, we should check the relation between momentum and position. And it turns out to be related by a commutator.(Postulate IV)
	2. Use the postulate to momentum operator.
	3. Find eigenstates.
	4. (Calculate the propagator.)

-----


Position Space
""""""""""""""""

1. Define :math:`\ket{x}` basis.

	* Orthonormal: 
	  
	  .. math:: \braket{x}{x'}=\delta(x-x')

	* Complete: 

	  .. math:: \int \braket{x'}{x'} \d x' = \mathbb{I} 

2. Define position operator.
	
   .. math:: \hat x \ket{x} = x \ket{x} 

   And in {:math:`\ket{x}`} basis, this operator becomes a function, which is
	 
   .. math::
      \begin{eqnarray}
      &&\bra{x}\hat x \ket{x'}  \\\\
      &=& \left(\bra{x}\hat x\right)\ket{x'} \\\\
      &=& x \braket{x}{x'} \\\\
      &=& x \delta(x-x')
      \end{eqnarray}

3. Find state vector in {:math:`\ket{x}`} basis.
   
   .. math:: \psi(t,x) = \braket{x}{\psi(t)}

   * Normalized: 

   .. math:: \int \left| \psi(t,x) \right|^2 \d x = 1.

   And we are interpreting :math:`\left| \psi(t, x)\right|^2` as probability density.
4. Calculate probability of a measurement. Taking :math:`\hat x` as an example.
   
   .. math::
      \begin{eqnarray}
      &&\bra{\psi} \hat x \ket{\psi} \\\\
      &=& \iint \braket{\psi}{x}\bra{x} \hat x \ket{x'} \braket{x'}{\psi}  \d x \d x' \\\\
      &=& \iint  \psi^ * (t,x) x\delta(x-x') \psi(t,x')  \d x \d x'  \\\\
      &=& \int \left| \psi(t,x) \right|^2 x \d x
      \end{eqnarray}								
	


Momentum Space
"""""""""""""""

To find the momentum operator, we need to check the relation between momentum and position before we just randomly define one. Truth is, we have a fourth postulate states the relation between them.


Postulate IV
^^^^^^^^^^^^^^

The commutator of :math:`\hat x`, :math:`\hat p` is

.. math::

   \left[ \hat x, \hat p \right] = i \hbar

Two comments:
  * Why i ? Eigenvalue of Anti-Hermitian operator.
  * Why :math:`\hbar`? Because people define the dimensions of position and momentum differently before they know this commutator. We would like to assign them the same dimension if we already know this relation.

Momentum Space
^^^^^^^^^^^^^^^^

1. Find momentum operator in position basis {:math:`\ket{x}`}.
   
   .. math:: \bra{x} \left[ \hat x, \hat p\right] \ket{x'} = i\hbar \delta(x-x')

   And write out the commutator and use the relation of delta function :math:`x\delta'(x) = -\delta(x)`, we find out the momentum operator in {:math:`\ket{x}`} basis,
   
   .. math:: \bra{x}\hat p \ket{x'} = -i\hbar \frac{\d }{\d t} \delta(x-x')

   **Let's talk physics.** What does that operator mean? We need to see what the result is when momentum operator is applied to a state. And remember we would work in {:math:`\ket{x}`} basis.

   .. math::

      \begin{eqnarray}
      &&\bra{x} \hat p \ket{\psi} \\\\
      &=& \iint \braket{x}{x'} \bra{x'} \hat p \ket{x''}\braket{x''}{\psi} \d x' \d x''  \\\\
      &=& \int \bra{x}\hat p \ket{x''}\psi(t,x'') \d x'' \\\\
      &=& \int \left( -i\hbar \frac{\d}{\d x} \delta(x-x') \psi(t,x') \right) \d x' \\\\
      &=& \int \left( -i\hbar \frac{\d}{\d x'} \delta(x'-x) \psi(t,x') \right) \d x' 
      \end{eqnarray}
	
   **Integrate by parts, we will find the expression.** (I am having a problem finding the right answer.)
	
   .. math:: \bra{x} \hat p \ket{\psi} = - i\hbar \frac{\d }{\d x}\psi(x) .

2. Eigenfunction for momentum.

   .. math::

      \hat p \ket{p} = p \ket{p} .

   Again, we are going to project it on the {:math:`\ket{x}`} basis, 
   
   .. math:: \bra{x}\hat p\ket{p} = \bra{x} p \ket{p} ,

   where :math:`\braket{x}{p}` is the eigenstates in {:math:`\ket{x}`} basis, we call it :math:`\phi_p(x)`.

   .. math::
      \begin{eqnarray}
      \bra{x}\hat p\ket{p} &=& p \phi_p(x)    \\\\
      \int \bra{x}\hat p \ket{x'}\braket{x'}{p}\d x' &=& p \phi_p(x)    \\\\
      -i\hbar \frac{\d }{\d x} \phi_p(x) &=& p \phi_p(x)
      \end{eqnarray}
	
   The solution is
   
   .. math:: \phi_p(x) = \mathrm{C} e^{i p x/\hbar}

   This constant C is found by the normalization condition, 
   
   .. math:: \braket{p}{p'}=\int \phi_p^*(x)\phi_{p'}(x)\d x = \delta(p-p')

   **The final results should be**
   
   .. math:: \phi_p(x)=\frac{1}{\sqrt{2\pi \hbar}} \exp{(i p x/\hbar)} 
	
3. Find the dynamics of free particles in quantum mechanics.
   **Find the propagator and everything solves.**
   The hamiltonian for a free particle is 

   .. math:: \hat H = \frac{\hat p^2}{2m} .

   We argue here that the eigenvectors of momentum are also the eigenvectors of this hamiltonian. And we can easily guess the eigenvalues are :math:`p^2/2m`. So the propagator is
   
   .. math:: \hat U = \int e^{-i p^2 t/2m\hbar} \ket{p}\bra{p} \d p

   But that is too abstract to use, we can find the expression in {:math:`\ket{x}`} basis.
   
   .. math::
      \begin{eqnarray}
      \bra{x}\hat U\ket{x} &=& \int e^{-i p^2 t/2 m \hbar} \braket{x}{p}\braket{p}{x} \d p    \\\\
      &=& \int e^{-i p^2 t/2 m \hbar} \left| \phi_p \right|^2 \d p    
      \end{eqnarray}








Quantum in 1D
==============


General
----------

Always start with the propagator for time independent Hamiltonian.

.. math:: \ket{\psi(t)} = \hat U \ket{\psi(0)}

For cases that Hamiltonian with discrete eigenvalues,

.. math:: \ket{\psi(t)} = \sum _ n e^{-i \epsilon _ n t/ \hbar } \ket{n}\braket{n}{\psi(0)}

If the initial state is just one of the eigenstates of Hamiltonian, say the mth one (normalized),

.. math:: \ket{\psi(t)} = e^{- i \epsilon _ m t/\hbar} \ket{ m }

Well, that phase factor doesn't have any effect for the topic we discuss. So our time evolution will stay on the same state forever.

The same thing happens for continuous cases.

So our task is simplified to solve the eigensystem of Hamiltonian, which is

.. math:: \hat H \ket{\epsilon} = \epsilon \ket{\epsilon}




Infinite Barriers
""""""""""""""""""

Math
^^^^^

Setup
~~~~~~

* Potential in a box

  .. math::
     \begin{eqnarray}
     V(x)=\cases{
     0, & 0< x <L \\\\
     \infty, & \text{Other}
     }
     \end{eqnarray}

Solve the Problem
~~~~~~~~~~~~~~~~~~~

* Hamiltonian
  
  .. math:: \hat H = \frac{\hat p ^2}{2 m } + V(x)

* Dynamic equation
  
  .. math:: \hat H \ket{\psi(t)} = \epsilon \ket{\psi(t)}

  We are happy to work in {:math:`\ket{x})`} basis, 
  
  .. math:: \bra{x} \hat H \ket{\psi(t)} = \bra{x} \epsilon \ket{\psi(t)} .

  Put the Hamiltonian in, and remember that in position basis
  
  .. math:: \bra{x} \hat p \ket{\psi} = - i \hbar\frac{\d}{\d x} \psi ,

  the equation of motion becomes
  
  .. math:: - \frac{\hbar ^2}{2 m} \frac{\d^2}{\d x^2} \psi(x,t) + V(x) \psi(x,t) = \epsilon \psi(x,t)
  
* Boundary conditions

  .. math::
     
     \psi _ I(0,t) = \psi _ {II}(0,t)

     \psi _ {II}(L, t) = \psi _ {III}(L, t) 

* Guess the Solutions
  
  .. math:: \psi_{II} = \psi = C \sin (k x) + D \cos(kx)

* Find the wavenumber k, by putting the assumed solutions into equation of motion
  
  .. math:: k = \pm \frac{2m \epsilon}{\hbar^2}

  Since we can always merge the negative into the constants, it is fine to use 
  
  .. math:: k = \frac{2m \epsilon}{\hbar^2}

* Use Boundary Condition
    1. At x=0, 

       .. math:: \psi(0,t)=0 .

       This gives us :math:`D = 0` .

    2. At :math:`x=L`, 

       .. math:: \psi(L,t)=0 . 

       This leads to

       .. math:: k L = n \pi .

       Since :math:`n=0` gives us a 0 wave function, we would just drop :math:`n=0`. For the same reason why we drop the negative values of k, we would drop all the negative values of n.
       This BC gives us the possible values of energy because wavenumber k is related to energy, 

       .. math:: \epsilon = \frac{\hbar^2}{2m L^2 } (n\pi)^2 ,

       with 

       .. math:: n=1,2,3, \cdots

* Normalization as the last constraint for the last undetermined parameter,
  
  .. math:: C=\sqrt{\frac{2}{L}}

  
Physics
~~~~~~~~

1. Estimation

	* Find the expression for energy using dimensional analysis.
	* Using uncertainty relation to estimate the expression for energy.

2. Comments

	* Why is the solution quantized?
  		1. Too many constraints. BCs + normalization.
	* Why do the n in the solution goes into the expression for energy?
  		1. Have a look at the kinetic energy term, the derivative does it.
	* What's so weird?
  		1. For :math:`n=2`, no particles found at :math:`x=L/2`. And so on.


Some General Properties
~~~~~~~~~~~~~~~~~~~~~~~~

1. 1D bound states have no degeneracy.
   Prove it by assume that there is a degeneracy state.
2. 1D bound states' wave function can be chosen to be real. (if potential V is real.)




Parity
================


Passive and Active Transformations
---------------------------------------

Generally, there are two ways of interpreting a transformation.

.. image:: QMFig/transformations.png
   :alt: Transformations

Here in QM, passive means transform the operator :math:`\hat \Omega`, while active means change the state :math:`\ket{\psi}`. Suppose we have a system :math:`\ket{\psi}`, an operator :math:`\hat \Omega`, a transformation :math:`\hat U`.

Transformation :math:`\hat U \ket{\psi}` is identical to :math:`\hat U^\dagger \hat \Omega \hat U` because they give the same observation results. The first one is called active, while the second one is called passive.


Parity
------------


Definition
""""""""""""""

.. math:: \hat \Pi \ket{x}= \ket{-x}

Properties
""""""""""""""

1. Act on momentum eigenvectors,

   .. math::
      \hat \Pi \ket{p} = \ket{-p} .

  * Physics: Parity changes the coordinate, so the direction of momentum is also changed.
  * Math: 

    .. math:: \hat \Pi \ket{p} = \int \hat \Pi \ket{x}\braket{x}{p}\d x= \int \ket{-x}\braket{x}{p}\d x 

    Change coordinate from x to -x, 

    .. math:: \hat \Pi \ket{p} = \int \ket{x}\braket{-x}{p}\d x = \int \ket{x}\braket{x}{-p}\d x  = \ket{-p}

2. Hermitian,

   .. math::
      \bra{x}\hat \Pi \ket{x'} = \delta(x+x')
      (\bra{x'}\hat \Pi \ket{x})^\dagger = \bra{x}\hat \Pi^\dagger \ket{x'} =\delta(x+x')

3. Unitary
  
   .. math:: \bra{x}\hat \Pi^\dagger \hat \Pi \ket{x'}= \braket{-x}{-x'}=\delta(-x+x')=\delta(x-x')=\braket{x}{x'} 

4. Inverse of parity
   
   .. math:: \hat \Pi \hat \Pi = \hat \Pi \hat \Pi^\dagger = \hat I 

5. Eigensystem of parity.

   .. math:: \hat \Pi \ket{\pi}=\pi\ket{\pi} 

   Apply another operator

   .. math:: \hat \Pi^2 \ket{\pi} = \pi^2 \ket{\pi}

   So,
   * Eigenvalues: 1, -1;
   * Eigenvactors: Even function, Odd function
6. Parity applied to operators
   a. Apply to position operator,

      .. math:: \hat \Pi^\dagger \hat X \hat \Pi = -\hat X

      Proof:

      .. math:: \bra{x}\hat \Pi ^\dagger \hat X \hat \Pi \ket{x'} = \bra{-x}\hat X \ket{-x'}= -x'\delta(x-x') = \bra{x}(-\hat X)\ket{x'}

   b. Apply to momentum operator,
      
      .. math:: \hat \Pi^\dagger \hat p \hat \Pi = -\hat p 

      Proof: Similar to the previous one, just change x basis to momentum basis.

7. Symmetry related to Hamiltonian.
   
   .. math:: \left[ \hat \Pi , \hat H  \right] = 0
   
   When this happens, parity of Hamiltonian won't change the wave function. Or the wave function should have an specific parity for 1D problem.
















Classical Limit of QM
========================

Ehrenfest's Theorem
---------------------


Schrödinger equation and its adjoint

.. math::
   
   i\hbar \frac{\d }{\d t} \ket{\psi(t)} = \hat H \ket{\psi(t)}

   -i\hbar \frac{\d }{\d t} \bra{\psi(t)} = \bra{\psi(t)} \hat H

For any observable :math:`\hat \Omega`,

.. math::

   \begin{eqnarray}
   \frac{\d }{\d t}\left<\hat \Omega \right > &=& \left( \frac{\d}{\d t}\bra{\psi(t)}\right)  \hat \Omega \ket{\psi(t)} + \bra{\psi(t)} \dot{\hat \Omega} \ket{\psi(t)} + \bra{\psi(t)} \hat \Omega \left( \frac{\d}{\d t}\ket{\psi(t)}\right)  \\\\
   &=& \frac{1}{i\hbar} \left ( - \bra{\psi(t)} \hat H \hat\Omega \ket{\psi(t)} +\bra{\psi(t)} \hat\Omega \hat H \ket{\psi(t)} \right) + \bra{\psi(t)} \dot{\hat \Omega} \ket{\psi(t)} \\\\
   &=& \frac{1}{i\hbar} \bra{\psi(t)}\left[\hat\Omega,\hat H\right] \ket{\psi(t)}+\bra{\psi(t)} \dot{\hat \Omega} \ket{\psi(t)}
   \end{eqnarray}

This is called Ehrenfest's Theorem.

Simple Example of Ehrenfest's Theorem
"""""""""""""""""""""""""""""""""""""""

Suppose we have a system with Hamiltonian

.. math:: \hat H = \frac{\hat p^2}{2m} + V(\hat x)

We need to figure some commutators first.

.. math::
   2m \left[ \hat x, \hat H \right] =\left[\hat x, \hat p^2\right] = \hat x \hat p\hat p - \hat p \hat p \hat x = \hat x \hat p \hat p -\hat p \hat x \hat p + \hat p \hat x \hat p - \hat p \hat p \hat x  = \left[\hat x , \hat p\right]\hat p + \hat p \left[ \hat x,\hat p\right]  = 2 i \hbar \hat p 

.. math::
   \left[\hat p, \hat H\right] = \left[\hat p, V(\hat x) \right] = \left[\hat p, \sum_0^\infty \frac{V^{(n)}}{n!}\hat x^n\right] =\cdots =-i\hbar V'(\hat x)

1. Position average

   .. math::
      \begin{eqnarray}
      \frac{\d }{\d t} \left< \hat x \right> &=& \frac{1}{i\hbar} \bra{\psi(t)} \left[ \hat x, \hat H \right]\ket{\psi(t)} \\\\
      &=&  \frac{\left< \hat p \right>}{m}
      \end{eqnarray}
   
   We are familiar with this in classical mechanics.
2. Momentum average
   
   .. math::
      \begin{eqnarray}
      \frac{\d}{\d t} \left<\hat p\right> &=& \frac{1}{i\hbar} \bra{\psi(t)} \left[\hat p, \hat H\right] \ket{\psi(t)} \\\\
      &=& \frac{1}{i\hbar} \bra{\psi(t)}  (-i\hbar V'(\hat x))  \ket{\psi(t)}  \\\\
      &=& -\left< V'(\hat x) \right>
      \end{eqnarray}

   In classical mechanics, the derivative of potential is force. And the result is just like Newton's 2n Law except the right hand side is not exactly like a force which should be :math:`-\frac{\d}{\d x} \left< V(\hat x) \right>`.


What does :math:`-\left< V'(\hat x)\right>` mean
"""""""""""""""""""""""""""""""""""""""""""""""""""

Suppose the potential area is fairly small and distributed around some coordinate :math:`x_0=\left< \hat x \right>`, we can do Taylor expansion around :math:`x_0`.

.. math::
   \begin{eqnarray}
   < V(\hat x)> &=& V(x_0)   +  V'(x_0) < (x - x_0)> + V''(x_0)<(x-x_0)^2> /2 + \cdots \\\\
   &=& V(x_0) + 0 + V''(x_0) (\Delta x)^2 + \cdots 
   \end{eqnarray}

If the uncertainty is small enough, every term except the first one becomes small. So to the lowest order, average of potential is approximately the potential at :math:`x_0`.

Similarly, the average of first derivative of potential :math:`<V'(\hat x)>` is approximately :math:`V'(x_0)`.

These gives us a hint for the previous result we got for the time evolution of average momentum. The result reduces to classical mechanics one as long as we keep the lowest order of Taylor expansion. Those higher order terms show the quantum effect.



Picture
-----------

We can see deeper into Ehrenfest's Theorem through Heisenberg Picture of quantum mechanics.


Schrödinger & Heisenberg Pictures
""""""""""""""""""""""""""""""""""""

Pictures are the ways we look at the evolution of systems.

Schrödinger Picture
^^^^^^^^^^^^^^^^^^^^

In Schrödinger picture the states are evolving with time.

.. math:: i\hbar \frac{\d}{\d t} \ket{\psi} _ S = \hat H \ket{\psi} _ S
 
And for time independent Hamiltonian, 

.. math:: \ket{\psi}_S = U^\dagger \ket{\psi _ 0} _ S


Heisenberg Picture
^^^^^^^^^^^^^^^^^^^^

In Heisenberg Picture, the states do not change with time.

.. math:: \ket{\psi} _ H = \ket{\psi_0} _ H ,

and of course the initial is the same with Schrödinger Picture,

.. math:: \ket{\psi_0} _ H = \ket{\psi _ 0} _ S .

How do we relate to Heisenberg Picture to Schrödinger Picture? Through investigation of observables. We should have the same observation results in both Pictures.

.. math::
   
   \begin{eqnarray}
   {} _ H \bra{\psi} \hat \Omega _ H \ket{\psi} _ H &=& {} _ S \bra{\psi} \hat \Omega _ S \ket{\psi} _ S \\\\
   {} _ H \bra{\psi} \hat \Omega _ H \ket{\psi} _ H &=& {} _ S \bra{\psi _ 0} \hat U^\dagger \hat \Omega _ S  \hat U \ket{\psi _ 0} _ S \\\\ 
   \hat \Omega _ H &=& \hat U^\dagger \hat \Omega _ S \hat U
   \end{eqnarray}
 
 So the operators change with time in Heisenberg Picture.
 
 
Ehrenfest's Theorem in Heisenberg Picture
""""""""""""""""""""""""""""""""""""""""""""

.. math::
   \frac{\d }{\d t} \hat \Omega _ H = \frac{1}{i\hbar } \left[ \hat \Omega _ H, \hat H \right] + \hat U ^ \dagger \frac{\partial }{\partial t} \Omega _ H \hat U

This can be easily proved by throwing every definition need in to it. We also need the following equations.

.. math:: \frac{\d }{\d t} \hat U = \frac{\d }{\d t} e^{-i\hat H t /\hbar} = \frac{\hat H}{i\hbar} \hat U

And REMEMBER that propagator commute with time independent Hamiltonian, so

.. math::
   \hat H = \hat U^\dagger \hat U \hat H = \hat U^ \dagger \hat U \hat U \equiv \hat H _ H

So this Ehrenfest's Theorem can also be written as

.. math::
   \frac{\d }{\d t} \hat \Omega _ H = \frac{1}{i\hbar } \left[ \hat \Omega _ H, \hat H _ H \right] + \hat U ^ \dagger \frac{\partial }{\partial t} \Omega _ H \hat U

We can **define**

.. math::
   \frac{\partial}{\partial t}\hat  \Omega _ H \equiv \hat U^\dagger  \frac{\partial }{\partial t}\hat  \Omega _ S \hat U  ,

which is the time derivative of operator in Heisenberg Picture.

**Reminder: The time derivative of an observable (average) depends not only the time derivative of itself, but also the commutator of the observable and Hamiltonian.**

Example of Ehrenfest's Theorem in Heisenberg Picture
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

We will show why it is better to work in Heisenberg Picture to show the meanings of Ehrenfest's Theorem.

Suppose we have a Hamiltonian in Heisenberg Picture,

.. math:: \hat H_H = \frac{\hat p _ H^2 }{2m} + V(\hat x _ H) .

Time derivative of position operator

.. math:: \frac{\d}{\d t} \hat x _ H = \frac{1}{i\hbar} \left[\hat x _ H, \hat H _ H \right ] = \frac{\hat p _ H}{m}

Time derivative of momentum operator

.. math:: \frac{\d}{\d t} \hat p_H = \frac{1}{i\hbar } \left[ \hat p _ H, \hat H \right] = - V'(\hat x_H)

So the operator in Heisenberg Picture just have a sense of the physical quantities in classical mechanics. That's why we like it.


Conservation
---------------

We say a observable is conserved if the corresponding operator commutes with Hamiltonian,

.. math:: \left[ \hat \Omega, \hat H \right]=0

1. Energy
Hamiltonian always commutes with itself.

.. math:: \frac{\d}{\d t} \left<\epsilon \right> = \bra{\psi} \left( \frac{\partial }{\partial t} \hat H \right) \ket{\psi}

If Hamiltonian is time independent, then energy is conserved. (If Hamiltonian is tide dependent, energy is not conserved. This is kind of obvious in classical mechanics.)


What is the nature of time dependence
"""""""""""""""""""""""""""""""""""""""

We can see this by looking at a simple example.

Assume we have a system with energy eigenstates :math:`\ket{\epsilon _ n}`, and initially, 

.. math:: \ket{\psi _ 0} = \sum_n C _ n \ket{\epsilon _ n} .

So 

.. math:: \ket{\psi(t)} = \sum _ n C _ n e^{-i\epsilon _ n t/\hbar} \ket{\epsilon _ n} .

We can calculate the expectation value of some operator :math:`\hat \Omega`,

.. math::
   \left< \omega (t) \right> =  \sum _ {n,m} \left( C _ n^ * e^{i\epsilon _ n t/\hbar } \bra{\epsilon _ n} \right)  \hat \Omega \left( C _ m e^{-i \epsilon _ m t/\hbar} \ket{\epsilon _ m} \right) = \sum _ {n,m} C _ n ^* C _ m e^{-i(\epsilon _ m - \epsilon _ n) t/\hbar} \bra{\epsilon _ n} \hat \Omega \ket{\epsilon _ m}

If :math:`\ket{\epsilon _ n}` are also the eigenvectors of :math:`\hat \Omega`, then

.. math:: \bra{\epsilon _ n} \hat \Omega \ket{\epsilon _ m} = \omega _ m \delta _ {n,m}

And the expectation value

.. math:: \left<  \omega (t) \right> = \sum _ {n} C _ n^* C _ n \omega _ n

**The important thing is that the time dependence of this expectation value actually arise from this term**

.. math:: e^{-i(\epsilon _ m - \epsilon _ n)t/\hbar} .

As it is so important, we call 

.. math:: (\epsilon _ m - \epsilon _ n)/\hbar

**Bohr frequency**.
