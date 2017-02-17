Mathematics in General Relativity
************************************

Vectors and Tensors
==========================

.. admonition:: Two Systems of Notations
   :class: note

   **Come back to this when the index fearing syndrome becomes too strong.**

   There are many different systems of notations for vectors.

   One of them is to use a tilde on top of the letter to denote a co-vector, i.e.,

   .. math::
      \tilde v, \qquad \text{dual vector, one-form, co-vector}

   The other notation that is widely used is abstract index notation where we use latin superscript to denote vector and latin subscript to denote co-vector, i.e.,

   .. math::
      v^a, & \qquad\text{vector}\\
      v_a, & \qquad \text{co-vector}.

   That is to say, :math:`v_a` is basically :math:`\tilde v`.

   The question is, obviously, how the components of vectors is denoted. In the first notation, we use subscript (components of vector) and superscript (components of co-vector) for the components,

   .. math::
      v_\mu \equiv \tilde v (e_\mu), \qquad \text{$\mu$ component of dual vector},

   where :math:`e_\mu` is the :math:`\mu` basis.


   However, the abstract index notation is using greek superscript for co-vector component and greek subscript for vector component.

   .. math::
      v^a_\mu, & \qquad\text{$\mu$ component of vector}\\
      v_a^\mu, & \qquad\text{$\mu$ component of co-vector}.

   For basis vectors, we usually denote them as :math:`\{e_\mu\}`. The dual space, which are basis of dual vectors are denoted as :math:`\{\tilde e^\mu\}`, with

   .. math::
      \tilde e^\mu e_\nu = \delta^\mu_\nu.



Whenever a vector is mentioned, it is composed of its components and basis, which should be written as

.. math::
   \alpha^a = \alpha^\mu e^a_{\phantom{a}\mu},

where $\{ \alpha^\mu \}$ are the components and $\{ e^a_{\phantom{a}\mu} \}$ are the basis.

Then we define its dual $w_b$

.. math::
   w_a \alpha^a = \mathscr{C},

where the left hand side can be expanded

.. math::
   w_a \alpha^a = w_\lambda f_a^{\phantom{a}\lambda} \alpha^\mu e^a_{\phantom{a}\mu} = w_\lambda \alpha^\mu f_a^{\phantom{a}\lambda} e^a_{\phantom{a}\mu}.

For orthonormal basis, we have

.. math::
   f_a^{\phantom{a}\lambda} e^a_{\phantom{a}\mu} = \delta^\lambda _\mu,

which gives us the contraction of $w_a$ and $\alpha^a$

.. math::
   w_a \alpha^a = w_\lambda \alpha^\mu \delta^\lambda _\mu = w _ \mu \alpha^\mu.

Usually the vector basis could be $\{ dx^\mu \}$ and we could derive the basis for the dual vector $\{ \frac{d}{dx^\mu} \}$.


Metric
-------------------------------


We define a scalar product in this way

.. math::
   \beta^a \cdot w^a = \beta^a g_{ab} \cdot w^b ,

where $g_{ab}$ is the metric and can be related to the basis.

The expression will be simplified using basis formalism,

.. math::
   \beta^a \cdot w^a = \beta^a g_{ab} \cdot w^b = \beta^\mu e^a_{\phantom{a}\mu} g_{ab} w^\lambda f^b_{\phantom{b}\lambda} = \beta^\mu w^\lambda g_{\mu\lambda} .






Description of Space-time Manifold
======================================================================


How to describe space-time manifold?

* Metric (with a set of local coordinates), connection (Christoffel symbols).
* Metric (in the form of tetrads), connection (Ricci rotation coefficients).
* 1+3 covariantly defined variables.




Description of Space-time Manifold - Coordinates
------------------------------------------------------


Description of Space-time Manifold - Tetrads
---------------------------------------------------------------------------



Description of Space-time Manifold - 1+3 Covariant Description
---------------------------------------------------------------------------

Physics in description is easier to understand.


Definations
~~~~~~~~~~~~~~~~~~

Definations of some physical quantities and operators are listed below.

Here we have

1. **geometrical variables**: Volume
2. **Kinematical variables**: Velocity, Expansion rate, Shear rate
3. **Thermaldynanmical variables**: Energy density, Momentum density, Pressure, Equation of state




Volume
""""""""

To calculate volume, the volume element should be defined first in order to integrate. Before that, orientation on manifolds is to be figured out.

On an oriented manifold with metric, the defined volume element (a n-form) should be compatible with the orientation and also determined by the metric. [1]_

Introducing those requirements, a compatible volume element is

.. math::
   \epsilon_{a_1\cdots a_n} = \pm \sqrt{|g|} (e^1)_{a_1}\wedge \cdots \wedge (e^n)_{a_n}


Alternatively, this can be expressed in the way Ellis used in arXiv:gr-qc/9812046v5.

.. math::
   \eta_{abcd} = \eta_{[abcd]}, \quad \mathrm{with} \eta_{0123} = \sqrt{|\mathrm {det} g_{ab}|}


Induced volume element $\hat \epsilon_{a_1\cdots a_{n-1}}$ is defined use the normal vector $u^a$ of the hypersurface,

.. math::
   \hat \epsilon_{a_1\cdots a_{n-1}} = u^b \epsilon_{b a_1 \cdots a_{n-1}}



.. [1] For more information, check out Canbin Liang's book. Volume 1, page 115.



4-velocity
"""""""""""

4-velocity of observed matter is

.. math::
   u^\alpha = \frac{\mathrm d x^\alpha}{\mathrm d \tau}

with :math:`u^\alpha u_\alpha =-1`, $\tau$ is the proper time along the worldlines of investaged matter.

Projection Tensors
""""""""""""""""""""

We can use 4-velocity to project variables to parts that is parallel to $u^\alpha$ and parts that is orthogonal to :math:`u^\alpha`.

.. math::
   U^a_{\phantom a b} &= -u^a u_b \\
   h_{ab} &= g_{ab} + u_a u_b, \qquad \text{induced metric from } g _{ab}


Some properties of the  two projections.

.. math::
   & U^a_{\phantom a b} U^b_{\phantom bc} = U^a_{\phantom a c}  ,  U^a_{\phantom a a} = 1  , U_{ab}=g_{ac} U^c_{\phantom cb}  , U_{ab} u^b = - g_{ac} u^c u_b u^b = u_a \\
   & h^a_{\phantom ab} = g^{ac} h_{cb} = \delta^a_{\phantom ab} + u^a u_b = \delta^a_{\phantom ab} - U^a_{\phantom ab} \\
   & h^a_{\phantom a c}h^c_{\phantom c b} = (\delta^a_{\phantom ac} - U^a_{\phantom ac})(\delta^c_{\phantom cb} - U^c_{\phantom cb}) = \delta^a_{\phantom ab} - U^a_{\phantom ab} = h^a_{\phantom ab} \\
   & h^a_{\phantom aa} = 4-1 = 3  ,   h_{ab}u^b = 0






Covariant time derivative (:math:`\dot \quad`)
""""""""""""""""""""""""""""""""""""""""""""""""

This is the derivative along the fundamental worldlines (projection on the worldlines),

.. math::
   \dot T^{ab}_{\phantom{ab}cd} = u^e \nabla_e T^{ab}_{\phantom{ab}cd}



Fully orthogonally projected covariant derivative (:math:`\tilde \nabla`)
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

This derivative is the project orghogonal to the normal vector of the hyperspace or orthogonal to the observer's 4-velocity or along the tagent of the hyperspace.

.. math::
	\tilde\nabla_e T^{ab}_{\phantom{ab}cd} = h^a_f h^b_gh^p_ch^q_dh^r_e \nabla_r T^{fg}_{\phantom{fg}pq}




Orthogonal projections of vectors
""""""""""""""""""""""""""""""""""

Orthogonal projection of vectors

.. math::
   v^{<a>}	= h^a_{\phantom a b} v^b


And the orthogonally projected symmetric trace-free part of tensors

.. math::
	T^{<ab>} = [h^{(a}_{\phantom {(a} c} h^{b)}_{\phantom{b)}d} - \frac{1}{3} h^{ab} h_{cd} ] T^{cd}




Othogonal projected covariant time derivatives along $u^a$
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

.. math::

	\dot v^{<a>} = h^a_{\phantom a b} \dot v^b

	\dot T^{<ab>} = [ h^{(a}_{\phantom{(a}b} h^{b)}_{\phantom{b)} d} - \frac 1 3 h^{ab}h_{cd} ]\dot T^{cd}





Properties
------------


* Projected time and space derivatives of :math:`U_{ab}`, :math:`h_{ab}` and :math:`\eta_{abc}` vanish.
