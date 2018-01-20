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

The Kerr metric has very nice symmetries.

1. Reflection symmetry with respect to :math:`\theta=\pi/2`;
2. Axial symmetry around the :math:`z` axis so that the angular momentum :math:`L_\phi=p_\phi` is conserved;
3. Stationary metric so that energy of test particles is conserved, :math:`E = -p_0` is conserved.

Frame Dragging
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

We would be very interested in how the rotation of black holes drag the spacetime. Due to the symmetries, the equatorial plane is easier to think about. So we set :math:`\theta=\pi/2`. For frame dragging, we have a guy riding a rocket so that :math:`p_r=0`. The frame dragging is best described by a observor that is staying stationary with frame, that is a zero angular momentum observor (ZAMO), that :math:`p_\phi=0`. Frame dragging angular velocity is

.. math::
   \omega = \frac{d\phi}{dt} = \frac{ d\phi/d\tau }{ dt/d\tau }.

It can be derived that the frame dragging angular velocity at radius :math:`r` is

.. math::
   \omega = - \frac{ g_{t\phi} }{g_{\phi\phi} } = \frac{ 2M r a }{ (r^2+a^2)^2 - a^2 \Delta \sin^2\theta }.



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



Ergospheres, Horizons
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In Schwarzschild black holes, the surface that :math:`g_{tt}=0` and :math:`g_{rr}\to\infty` are the same surface that is defined as the horizon. However, :math:`g_{tt}=0` gives us the ergospheres and :math:`g_{rr}\to\infty` gives us the horizons.

.. admonition:: Why?
   :class: note

   The ergospheres are the regions that even light can not travel in the counter-rotation direction. That being said, :math:`p^\phi` can only be positive for light. To prove this, we set :math:`ds^2=0` and neglect :math:`p_r`,

   .. math::
      g_{tt} dt^2 + g_{\phi\phi} d\phi^2 + 2 g_{t\phi} dt d\phi = 0,

   which shows that,

   .. math::
      p^\phi = \frac{ -g_{t\phi} \pm \sqrt{ g_{t\phi} - g_{tt}g_{\phi\phi} } }{ g_{\phi\phi} }.

   We can show that :math:`p^\phi` can only be negative if :math:`g_{tt}>0`, while it can be negative or positive if :math:`g_{tt}<0`. What we found is that for :math:`g_{tt}>0`, we are entering a region where even light can not travel against the direction of the rotation. This is why we define the condition :math:`g_{tt}=0` to be the surface of the ergospheres.

   As for :math:`g_{rr}\to\infty`, it is the condition for :math:`p^r` being always negative, which means we are always travelling inward. It proven by similar techniques.


**We have two ergospheres and horizons!** Solving :math:`g_{tt}=0` gives us

.. math::
   r_{e,\pm} = M \pm \sqrt{M^2-a^2\cos^2\theta},

which defines the two surfaces of ergospheres.

Meanwhile, :math:`g_{rr}\to\infty` indicates that :math:`\Delta=0`, which proves to be

.. math::
   r_{h,\pm} = M\pm\sqrt{ M^2 - a^2 },

which shows us the two horizons.

.. figure:: assets/black-holes/gtt-grr-as-function-of-r-kerr-bh.jpg
   :align: center

   :math:`g_{tt}` and :math:`g_{rr}` as function of coordinate :math:`r`.

.. admonition:: Mathematica (11) Code
   :class: toggle

   .. code-block:: mma

      gtt[r_,a_,mass_:1,theta_:Pi/2]:=Module[{deltaM,rhosquareM},
      deltaM=r^2-2mass r+a^2;
      rhosquareM=r^2+a^2Cos[theta]^2;
      -(deltaM-a^2Sin[theta]^2)/rhosquareM
      ]
      grr[r_,a_,mass_:1,theta_:Pi/2]:=Module[{deltaM,rhosquareM},
      deltaM=r^2-2mass r+a^2;
      rhosquareM=r^2+a^2Cos[theta]^2;
      rhosquareM/deltaM
      ]
      Manipulate[
      Plot[{gtt[r,a,mass,theta],grr[r,a,mass,theta]},{r,0,5},Frame->True,FrameLabel->{"r","Subscript[g, tt] or Subscript[g, rr]"},ImageSize->Large,PlotRange->Automatic,PlotStyle->{Black,Red},GridLines->{{ {mass+Sqrt[mass^2-a^2],Directive[Red,Thick]},{mass+Sqrt[mass^2-a^2Cos[theta]^2],Directive[Gray,Thick]},{mass-Sqrt[mass^2-a^2],Directive[Red,Thick]},{mass-Sqrt[mass^2-a^2Cos[theta]^2],Directive[Gray,Thick]}},None},PlotLabel->"Angular Velocity of Frame Dragging \[Omega] (with a="<>ToString@a<>", M="<>ToString@mass<>", \[Theta]="<>ToString@TraditionalForm@theta<>")",PlotLegends->Placed[{"Subscript[g, tt]","Subscript[g, rr]"},{Right,Top}]],
      {{a,0.7,"Spin Angular Momentum of Black Hole"},0,1},{{mass,1,"Mass of Black Hole"},0.1,10},{{theta,Pi/3,"\[Theta]"},0,Pi}
      ]


In fact we can prove that

1. Within region :math:`r>r_{e,+}`, :math:`g_{tt}<0`, :math:`g_{rr}>0`;
2. Within region :math:`r_{h,+}<r<r_{e,+}`, :math:`g_{tt}>0`, :math:`g_{rr}>0`;
3. Within region :math:`r_{h,-}<r<r_{h,+}`, :math:`g_{tt}<0`, :math:`g_{rr}<0`;
4. Within region :math:`r_{e,-}<r<r_{h,-}`, :math:`g_{tt}<0`, :math:`g_{rr}>0`;
5. Within region :math:`r<r_{e,-}`, :math:`g_{tt}<0`, :math:`g_{rr}>0`.

.. figure:: assets/black-holes/gtt-grr-regions-kerr-bh.png
   :align: center

   Regions of Kerr black holes. :math:`r_{e,\pm}` are the two surfaces of ergospheres, :math:`r_{h,\pm}` are the two horizons, as calculated previously.



.. figure:: assets/black-holes/kerr-surfaces.png
   :align: center

   A Kerr black hole is nicely visualized by `Simon Tyran <http://kerr.newman.yukterez.net/>`_, whose work is licensed with CC BY-SA.


.. admonition:: What are the significances of the surfaces?
   :class: warning

   For the outer horizon and outer ergosphere, their properties are discussed. What are the properties of the inner surfaces?


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

Suppose we have a particle falling inside a black hole, starting with 0 energy at infty. It falls through the ergosphere, and decays into two particles, A and B. Particle A obtains a negative energy, meanwhile having negative angular momentum, so that it stays in ergosphere or falls through the horizon. The other particle obtains positive energy, and managed to escape. Energy conservation tells us that the escaped particle will have energy at infty that is larger than the initial energy 0.

This though experiment relies on the effective potential :math:`V(r)` of the ergosphere. For positive angular momentum, we always fall through the
