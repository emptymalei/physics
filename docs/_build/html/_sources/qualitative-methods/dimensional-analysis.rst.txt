Dimensional Analysis
===========================


.. admonition:: Reference Books
   :class: toggle

   1. Dimensional Analysis and Group Theory in Astrophysics, by Rudolf Kurth



Notations
------------------------


I find the Kurth notation being convinient. Kurth used :math:`l^a, t^b, m^c` to denote length to the ath power, time to the bth powe and mass to the cth power.


Useful Physical Constants
----------------------------


1. Newton's gravitational constant: :math:`[G] \to l^3 t^{-2} m^{-1}`. The quick derivation is :math:`-GM/r^2 = F/m = a`.




Nondegenerate Case
--------------------------------

1. We find all the physical quantities and relevant physical constants.
2. Check if the combination is unique.


.. admonition:: Deflection of Light by Sun
   :class: toggle

   The example given in Kurth's book is the deflection of light by gravitational field. The relevant quantities are

   1. deflection angle: :math:`\theta` which is dimensionless, :math:`[\theta]\to l^0 t^0 m^0`,
   2. the mass of the Sun: :math:`M` which has dimension :math:`[M]\to l^0 t^0 m^1`,
   3. the distance from the center of the Sun at the point of closest contact, :math:`[r]\to l^1 t^0 m^0`.

   The physical constant we can think of in the first place is :math:`G`, which has dimension :math:`[G]\to l^3 t^{-2} m^{-1}`. However, we now combine :math:`G` and :math:`M` and :math:`r` to produce :math:`\theta`, which is identical to solving the equation

   .. math::
      \theta^a = G^b M^c r^d,

   or the system of equations

   .. math::
      0 =& 3b + d & \qquad \text{for l}\\
      0 =& -2b & \qquad \text{for t}\\
      0 =& (-b)+ c & \qquad \text{for m}.

   The system of equations has no nontrivial solutions. Where to find the other physical constant? We are dealing with light, thus one of the choices is the speed of light, :math:`c`. Add in :math:`[c^e]\to l^e t^{-e} m^0`, we have the equations


   .. math::
      0 =& 3b + d + e & \qquad \text{for l}\\
      0 =& (-2b) + (-e) & \qquad \text{for t}\\
      0 =& (-b)+ c & \qquad \text{for m},

   which has unique nontrivial set of solutions

   .. math::
      c =& b \\
      d =& -b\\
      e =& -2b.

   Now we find that

   .. math::
      \theta^a = \left( \frac{G M}{r c^2} \right)^b.

   In general, since :math:`\frac{G M}{r c^2}` is dimensionless, the general form is

   .. math::
      \theta = f( \frac{G M}{r c^2} ).

   This result is already satisfactory.

   Is there more we can conclude from here? Kurth took a step further and **used limits**. We expect :math:`\theta\to 0` for small mass since we do not observe this effect in daily life. :math:`M\to 0` leads to :math:`\frac{G M}{r c^2}\to 0`. We can even use the simplest form

   .. math::
      \theta \propto \frac{G M}{r c^2} .

   This is identical to the fact that the Taylor expansion of function :math:`f(x)` at :math:`x\to 0` has a neglectable zeroth order.



   To summarize, we used the following techniques.

   1. Dimensions.
   2. Limits of physical problems compared with observations.


   If GR is part of the knowledge pool, we notice that the radius :math:`R` of the celestial body is not consider in this analysis. When we add in this, we find three dimensionless quantities,

   .. math::
      &\frac{G M}{r c^2}\\
      &\frac{GM}{R c^2}\\
      &\frac{R}{r}.

   They are not linearly independent. We choose two of them,

   .. math::
      &\frac{G M}{r c^2}\\
      &\frac{R}{r}.
