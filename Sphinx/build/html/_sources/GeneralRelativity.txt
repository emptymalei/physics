

*******************
General Relativity
*******************





Description of Space-time Manifold
===================================


How to describe space-time manifold?

* Metric (with a set of local coordinates), connection (Christoffel symbols).
* Metric (in the form of tetrads), connection (Ricci rotation coefficients).
* 1+3 covariantly defined variables.




Description of Space-time Manifold - Coordinates
====================================================


Description of Space-time Manifold - Tetrads
=============================================



Description of Space-time Manifold - 1+3 Covariant Description
=================================================================

Physics in description is easier to understand.


Definations
-------------

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
   \begin{equation}
   \epsilon_{a_1\cdots a_n} = \pm \sqrt{|g|} (e^1)_{a_1}\wedge \cdots \wedge (e^n)_{a_n}
   \end{equation}

Alternatively, this can be expressed in the way Ellis used in arXiv:gr-qc/9812046v5.

.. math::
   \begin{equation}
   \eta_{abcd} = \eta_{[abcd]}, \quad \mathrm{with} \eta_{0123} = \sqrt{|\mathrm {det} g_{ab}|}
   \end{equation}

Induced volume element $\hat \epsilon_{a_1\cdots a_{n-1}}$ is defined use the normal vector $u^a$ of the hypersurface,

.. math::
   \begin{equation}
   \hat \epsilon_{a_1\cdots a_{n-1}} = u^b \epsilon_{b a_1 \cdots a_{n-1}}
   \end{equation}


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
   \begin{eqnarray}
   U^a_{\phantom a b} &=& -u^a u_b \\
   h_{ab} &=& g_{ab} + u_a u_b, \qquad \text{induced metric from $g_{ab}$}
   \end{eqnarray}

Some properties of the  two projections.

.. math::
   \begin{eqnarray}
   && U^a_{\phantom a b} U^b_{\phantom bc} = U^a_{\phantom a c}  ,  U^a_{\phantom a a} = 1  , U_{ab}=g_{ac} U^c_{\phantom cb}  , U_{ab} u^b = - g_{ac} u^c u_b u^b = u_a \\
   && h^a_{\phantom ab} = g^{ac} h_{cb} = \delta^a_{\phantom ab} + u^a u_b = \delta^a_{\phantom ab} - U^a_{\phantom ab} \\
   && h^a_{\phantom a c}h^c_{\phantom c b} = (\delta^a_{\phantom ac} - U^a_{\phantom ac})(\delta^c_{\phantom cb} - U^c_{\phantom cb}) = \delta^a_{\phantom ab} - U^a_{\phantom ab} = h^a_{\phantom ab} \\
   && h^a_{\phantom aa} = 4-1 = 3  ,   h_{ab}u^b = 0
   \end{eqnarray}





Covariant time derivative (:math:`\dot \quad`)
""""""""""""""""""""""""""""""""""""""""""""""""

This is the derivative along the fundamental worldlines (projection on the worldlines),

.. math::
   \begin{equation}
   \dot T^{ab}_{\phantom{ab}cd} = u^e \nabla_e T^{ab}_{\phantom{ab}cd}
   \end{equation}


Fully orthogonally projected covariant derivative (:math:`\tilde \nabla`)
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

This derivative is the project orghogonal to the normal vector of the hyperspace or orthogonal to the observer's 4-velocity or along the tagent of the hyperspace.

.. math::
   \begin{equation}
	\tilde\nabla_e T^{ab}_{\phantom{ab}cd} = h^a_f h^b_gh^p_ch^q_dh^r_e \nabla_r T^{fg}_{\phantom{fg}pq}
   \end{equation}



Orthogonal projections of vectors
""""""""""""""""""""""""""""""""""

Orthogonal projection of vectors

.. math::
   \begin{equation}
   v^{<a>}	= h^a_{\phantom a b} v^b
   \end{equation}

And the orthogonally projected symmetric trace-free part of tensors

.. math::
   \begin{equation}
	T^{<ab>} = [h^{(a}_{\phantom {(a} c} h^{b)}_{\phantom{b)}d} - \frac{1}{3} h^{ab} h_{cd} ] T^{cd}
   \end{equation}



Othogonal projected covariant time derivatives along $u^a$
"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""

.. math::

	\dot v^{<a>} = h^a_{\phantom a b} \dot v^b

	\dot T^{<ab>} = [ h^{(a}_{\phantom{(a}b} h^{b)}_{\phantom{b)} d} - \frac 1 3 h^{ab}h_{cd} ]\dot T^{cd}





Properties
------------


* Projected time and space derivatives of :math:`U_{ab}`, :math:`h_{ab}` and :math:`\eta_{abc}` vanish.













Fields and Particles
======================


Energy-Momentum Tensor for Particles
-------------------------------------

.. math::
   \begin{equation}
   S_p \equiv -m c \int \int \mathrm d s\mathrm d\tau \sqrt{-\dot x ^\mu g_{\mu\nu} \dot x^\nu} \delta^4(x^\mu - x^\mu (s))    ,
   \end{equation}

in which :math:`x^\mu(s)` is the trajectory of the particle. Then the energy density $\rho$ corresponds to :math:`m\delta^4(x^\mu- x^\mu(s))`.

The Largrange density

.. math::

   \mathcal L = -\int\mathrm ds mc \sqrt{-\dot x^\mu g_{\mu\nu}\dot x^\nu}\delta^4(x^\mu - x^\mu(s))


Energy-momentum density is :math:`\mathcal T^{\mu\nu} = \sqrt{-g}T^{\mu\nu}` is

.. math::
   \mathcal T^{\mu\nu} = -2 \frac{\partial \mathcal L}{\partial g_{\mu\nu}}


Finally,

.. math::
   \begin{eqnarray}
   \mathcal T^{\mu\nu} &=& \int \mathrm ds \frac{mc\dot x^\mu \dot x^\nu}{\sqrt{-\dot x^\mu g_{\mu\nu} \dot x^\nu}} \delta(t-t(s))\delta^3(\vec x - \vec x(t)) \\
   &=& m\dot x^\mu \dot x^\nu \frac{\mathrm d s}{\mathrm d t} \delta^3(\vec x - \vec x(s(t)))
   \end{eqnarray}





Theorems
=========


Killing Vector Related
------------------------


:math:`\xi^a` is Killing vector field, :math:`T^a` is the tangent vector of geodesic line. Then :math:`T^a\nabla_a(T^b\xi_b)=0`, that is :math:`T^b\xi_b` is a constant on geodesics.






Specific Topics
=================

Redshift
---------

In geometrical optics limit, the angular frequency :math:`\omega` of a photon with a 4-vector :math:`K^a`, measured by a observer with a 4-velocity :math:`Z^a`, is :math:`\omega=-K_aZ^a`.


Stationary vs Static
---------------------

Stationay
""""""""""""""""""""""

"A stationary spacetime admits a timelike Killing vector field. That a stationary spacetime is one in which you can find a family of observers who observe no changes in the gravitational field (or sources such as matter or electromagnetic fields) over time."

When we say a field is stationary, we only mean the field is time-independent.


Static
"""""""""""""

"A static spacetime is a stationary spacetime in which the timelike Killing vector field has vanishing vorticity, or equivalently (by the Frobenius theorem) is hypersurface orthogonal. A static spacetime is one which admits a slicing into spacelike hypersurfaces which are everywhere orthogonal to the world lines of our 'bored observers'"

When we say a field is static, the field is both time-independent and symmetric in a time reversal process.


