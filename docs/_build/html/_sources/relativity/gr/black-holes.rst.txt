Black Holes
=================================

.. admonition:: Glossaries
   :class: note

   1. ZAMO: zero angular-momentum observer


Observations of Black Holes
--------------------------------

LIGO!

There are several ways of detecting black holes, directly or indirectly.

1. Gravitational effects: such as lensing, binary systems, gravitational waves.
2. Matter around it: orbit of stars around black holes, emission of accretion discs, final stage of Hawking radition.


Several astronomical tips:

1. As for accretions, pulsars are steady because of the magnetic field they are holding. Black holes do not hold magnetic field like that so it can not be a steady pulsation.
2. There is a star orbiting the center of our galaxy at an orbit of 120AU, which helps us determing the mass of the center object.
3. First generatioin of stars (population III stars) might form supermassive black holes, and might still be around since Hawking radiation of massive black holes is low.
4. Black hole collisions are studied using computers numerically. Such simulations have intrinsic instability due to the fact that GR has coordinate freedom and singularities.
5. Simulations found kicks of black holes. Black hole mergers starting with asymmetries will develop asymmetric emission of gravitational waves thus kicking the system in the opposite direction.



Schwarzschild Metric
-------------------------

The line element for Schwarzschild metric is

.. math::
   ds^2 &= -(1-\frac{2M}{r}) dt^2 + (1-\frac{2M}{r})^{-1} dr^2 + r^2 ( d\theta^2 + \sin^2\theta d\phi^2 ) \\
   &= g_{tt}dt^2 + g_{rr}dr^2 + g_{\theta\theta} d\theta^2 + g_{\phi\phi}d\phi^2.

The inverse of metric elements :math:`g^{\alpha\beta}` are easily obtained since the metric is diagonal in this basis.



Kerr Metric
--------------------

To begin with, Kerr spacetime around a Kerr black hole of mass :math:`M`, spin angular momentum :math:`J`, is described as the line element

.. math::
   ds^2 = - \frac{\Delta- a^2\sin^2\theta}{\rho^2} dt^2 - 2 a \frac{2Mr \sin^2 \theta}{ \rho^2} dt d\phi + \frac{ (r^2 + a^2)^2 - a^2 \Delta \sin^2 \theta }{\rho^2} \sin^2\theta d\phi^2 + \frac{\rho^2}{\Delta^2}dr^2 + \rho^2 d\theta^2,

where

.. math::
   a &= J/M \\
   \Delta &= r^2 - 2M r + a^2 \\
   \rho^2 &= r^2 + a^2 \cos^2\theta.


It can be derived that the frame dragging angular velocity at radius :math:`r` is

.. math::
   \omega = - \frac{ g_{t\phi} }{g_{\phi\phi} }.

.. figure:: assets/black-holes/kerr-metric-frame-dragging-angular-velocity.jpg
   :align: center

   Angular velocity of the frame dragging for a Kerr black hole. Everything is scaled by the mass of black hole. It drops as :math:`1/r^3` for large :math:`r`.


.. admonition:: Mathematica (11) Code for the Plot
   :class: toggle

   .. code-block:: mma
      :linenos:

      In[1]:= omega[r_,a_:0.2,mass_:1,theta_:0]:=Module[{deltaM},
      deltaM=r^2-2mass r+a^2;
      2mass r/( (r^2+a^2)^2-a^2 deltaM Sin[theta]^2 )
      ]
      In[2]:= Solve[D[omega[r,a],r]==0,r]
      Out[2]= {{r->-(a/Sqrt[3])},{r->a/Sqrt[3]}}
      In[3]:= Manipulate[
      Plot[omega[r,a],{r,0,5},
      Frame->True,FrameLabel->{"r","\[Omega]"},
      ImageSize->Large,PlotRange->Full,PlotStyle->Black,
      GridLines->{{ {a/Sqrt[3],
      Directive[Gray,Thick]},{1+Sqrt[1-a^2],Directive[Red,Thick]}},{1}},
      Epilog->{Inset[Style["Horizon",13,Red],{(1+Sqrt[1-a^2]),0},{0,0}],
      Inset[Style["Max",13,Gray],{a/Sqrt[3],0},{0,0}]},
      PlotLabel->"Angular Velocity of Frame Dragging \[Omega] (with a="<>ToString@a<>")"],
      {{a,0.5,"Spin Angular Momentum of Black Hole"},0,1}
      ]


Photons Travelling on Equatorial Plane
-----------------------------------------------

The elements of the metric :math:`g_{\alpha\beta}` as well as :math:`g^{\alpha\beta}` are frequently used. It is essential to find them, which involves some matrix inversion.

.. admonition:: Inverse of Block Diagonal Matrix
   :class: note

   For a given matrix

   .. math::
      A = \begin{pmatrix}
      A_1 & 0 \\
      0 & A_2
      \end{pmatrix},

   the inverse of it :math:`A^{-1}` is

   .. math::
      A^{-1} = \begin{pmatrix}
      A_1^{-1} & 0 \\
      0 & A_2^{-1}
      \end{pmatrix}.

   This result works for arbitrary dimensions.

.. admonition:: Inverse of 2 by 2 Matrix
   :class: note

   For a 2 by 2 matrix

   .. math::
      B = \begin{pmatrix}
      B_{11} & B_{12}\\
      B_{21} & B_{22}
      \end{pmatrix},

   the inverse is

   .. math::
      B^{-1} = \frac{1}{D} \begin{pmatrix}
      B_{22} & - B_{21}\\
      -B_{12} & B_{11}
      \end{pmatrix}.



Penrose Process
---------------------------

Suppose we have a particle falling inside a black hole, starting with 0 energy at infinity. It falls through the ergosphere, and decays into two particles, A and B. Particle A obtains a negative energy, meanwhile having negative angular momentum, so that it stays in ergosphere or falls through the horizon. The other particle obtains positive energy, and managed to escape. Energy conservation tells us that the escaped particle will have energy at infinity that is larger than the initial energy 0.

This though experiment relies on the effective potential :math:`V(r)` of the ergosphere. For positive angular momentum, we always fall through the
