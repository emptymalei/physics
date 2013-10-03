******************
Mathematics
******************



Differential Geometry
=======================



Metric
--------


Definitions
""""""""""""""


Denote the basis in use as :math:`\hat e_\mu`, then the metric can be written as

.. math::
   g_{\mu\nu}=\hat e_\mu \hat \cdot e_\nu

if the basis satisfies

Inversed metric

.. math::
   g_{\mu\lambda}g^{\lambda\nu}=\delta_\mu^\nu = g_\mu^\nu






How to calculate the metric
"""""""""""""""""""""""""""""

Let's check the definition of metric again.

If we choose a basis :math:`\hat e_\mu`, then a vector (at one certain point) in this coordinate system is

.. math::
   x^a=x^\mu \hat e_\mu


Then we can construct the expression of metric of this point under this coordinate system,

.. math::
   g_{\mu\nu}=\hat e_\mu\cdot \hat e_\nu


For example, in spherical coordinate system, 

.. math:: \vec x=r\sin \theta\cos\phi \hat e_x+r\sin\theta\sin\phi \hat e_y+r\cos\theta \hat e_z 
   :label: EQrelativityMetricPoint




Now we have to find the basis under spherical coordinate system. Assume the basis is :math:`\hat e_r, \hat e_\theta, \hat e_\phi`. Choose some scale factors :math:`h_r=1, h_\theta=r, h_\phi=r\sin\theta`. Then the basis is

.. math::
   \hat e_r=\frac{\partial \vec x}{h_r\partial r}=\hat e_x \sin\theta\cos\phi+\hat e_y \sin\theta\sin\phi+\hat e_z \cos\theta,

etc. Then collect the terms in formula :eq:`EQrelativityMetricPoint` is we get :math:`\vec x=r\hat e_r`, this is incomplete. So we check the derivative.

.. math::
   \begin{eqnarray}
     \mathrm d\vec x&=& \hat e_x (\mathrm dr \sin\theta\cos\phi+r\cos\theta\cos\phi\mathrm d\theta-r\sin\theta\sin\phi\mathrm d\phi)\\
     &&\hat e_y (\mathrm dr\sin\theta\sin\phi+r\cos\theta\sin\phi\mathrm d\theta+r\sin\theta\cos\phi\mathrm d\phi) \\
     &&\hat e_z (\mathrm dr\cos\theta-r\sin\theta\mathrm d\theta) \\
     &=&\mathrm dr(\hat e_x\sin\theta\cos\phi +\hat e_y \sin\theta\sin\phi -\hat e_z \cos\theta)  \\
     &&\mathrm d\theta (\hat e_x\cos\theta\cos\phi +\hat e_y \cos\theta\sin\phi - \hat e_z \sin\theta)r \\
     &&\mathrm d\phi (-\hat e_x\sin\phi +\hat e_y \cos\phi)r\sin\theta  \\
     &=&\hat e_r\mathrm dr+\hat e_\theta r\mathrm d\theta +\hat e_\phi r\sin\theta\mathrm d \phi
   \end{eqnarray}

Once we reach here, the component (:math:`e_r ,e_\theta, e_\phi`) of the point under the spherical coordinates system basis (:math:`\hat e_r, \hat e_\theta, \hat e_\phi`) at this point are clear, i.e.,

.. math::
   \begin{eqnarray}
    \mathrm d\vec x&=&\hat e_r\mathrm d r+\hat e_\theta r\mathrm d \theta+\hat e_\phi r\sin\theta \mathrm d\phi \\
    &=&e_r\mathrm d r+e_\theta \mathrm d\theta+e_\phi \mathrm d\phi
   \end{eqnarray}

In this way, the metric tensor for spherical coordinates is 

.. math::
   \begin{equation}
    g_{\mu\nu}=(e_\mu\cdot e_\nu)=\left(\begin{matrix}
    1 &0&0 \\
    0& r^2&0 \\
    0&0& r^2\sin^2\theta \\
    \end{matrix}\right)
   \end{equation}



Connection
-----------

First class connection can be calculated 

.. math::
   \Gamma^\mu_{\phantom{\mu}\nu\lambda}=\hat e^\mu\cdot \hat e_{\mu,\lambda}


Second class connection is\footnote{Kevin E. Cahill}

.. math::
   [\mu\nu,\iota]=g_{\iota\mu}\Gamma^\mu_{\phantom{\mu}\nu\lambda}





Gradient, Curl, Divergence, etc
---------------------------------


Gradient
""""""""""

.. math::
   T^b_{\phantom bc;a}= \nabla_aT^b_{\phantom bc}=T^b_{\phantom bc,a}+\Gamma^b_{ad}T^d_{\phantom dc}-\Gamma^d_{ac}T^b_{\phantom bd}



Curl
"""""""

For an anti-symmetric tensor, :math:`a_{\mu\nu}=-a_{\nu\mu}`

.. math::
   \begin{eqnarray}
      \mathrm{Curl}_{\mu\nu\tau}(a_{\mu\nu})&\equiv& a_{\mu\nu;\tau}+a_{\nu\tau;\mu}+a_{\tau\mu;\nu} \\
      &=&a_{\mu\nu,\tau}+a_{\nu\tau,\mu}+a_{\tau\mu,\nu}
   \end{eqnarray}


Divergence
"""""""""""""

.. math::
   \begin{eqnarray}
    \mathrm{div}_\nu(a^{\mu\nu})&\equiv& a^{\mu\nu}_{\phantom{\mu\nu};\nu}=\frac{\partial a^{\mu\nu}}{\partial x^\nu}+\Gamma^\mu_{\nu\tau}a^{\tau\nu}+\Gamma^\nu_{\nu\tau}a^{\mu\tau} \\
    &=&\frac1{\sqrt{-g}}\frac{\partial}{\partial x^\nu}(\sqrt{-g}a^{\mu\nu})+\Gamma^\mu_{\nu\lambda}a^{\nu\lambda}
   \end{eqnarray}

For an anti-symmetric tensor

.. math::
   \mathrm {div}(a^{\mu\nu})=\frac1{\sqrt{-g}}\frac{\partial}{\partial x^\nu}(\sqrt{-g}a^{\mu\nu})


**Annotation** Using the relation :math:`g=g_{\mu\nu}A_{\mu\nu}`, :math:`A_{\mu\nu}` is the algebraic complement, we can prove the following two equalities.

.. math::
   \Gamma^\mu_{\mu\nu}=\partial_\nu\ln{\sqrt{-g}}


.. math::
   V^\mu_{\phantom\mu;\mu}=\frac1{\sqrt{-g}}\frac{\partial}{\partial x^\mu}(\sqrt{-g}V^\mu)


In some simple case, all the three kind of operation can be demonstrated by different applications of the del operator, which :math:`\nabla\equiv \hat x\partial_x+\hat y\partial_y+\hat z \partial_z`.

* Gradient,  :math:`\nabla f`, in which :math:`f` is a scalar.
* Divergence, :math:`\nabla\cdot \vec v`
* Curl, :math:`\nabla \times \vec v`
* Laplacian, :math:`\Delta\equiv \nabla\cdot\nabla\equiv \nabla^2`


Linear Algebra
=================

Basic Concepts
------------------


Trace
""""""""

Trace should be calculated using the metric. An example is the trace of Ricci tensor,

.. math::
   R=g^{ab}R_{ab}


Einstein equation is 

.. math::
   R_{ab}-\frac{1}{2}g_{ab}R=8\pi G T_{ab}

The trace is 

.. math::
   \begin{eqnarray}
   g^{ab}R_{ab}-\frac{1}{2}g^{ab}g_{ab}R&=&8\pi G g^{ab}T_{ab} \\
   \Rightarrow R-\frac{1}{2} 4 R &=& 8\pi G T \\
   \Rightarrow -R&=&8\pi GT
   \end{eqnarray}


Technique
------------

Inverse of a matrix
""""""""""""""""""""

Many methods to get the inverse of a matrix. Check wikipedia for Invertible matrix.

Adjugate matrix method for example is here.

.. math::
   A^{-1} = \frac{A^*}{|A|}

in which, :math:`A^*` is the adjugate matrix of :math:`A`.




Differential Equations
=======================

Standard Procedure
--------------------

Tricky
------------

WKB Approximation
""""""""""""""""""""

When the highest derivative is multiplied by a small parameter, try this.
