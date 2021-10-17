Spherical Solutions to Stars
=================================

Static
---------------------------------

Static spacetime is defined as [Schutz]_

1. all metric components are independent of time;
2. geometry is unchanged by time reversal.



Equation of Motion
----------------------------

For spherical configuration, we have the line element of the form

.. math::
   ds^2 = - e^{2\Phi} dt^2 + e^{2\Lambda} dr^2 + r^2 d\Omega^2.


For future reference, we write down some metric elements.

.. math::
   g_{00} &= -e^{2\Phi} \\
   g_{rr} & = e^{2\Lambda}.


Exterior Solutions
-------------------------------------




Interior Solutions
------------------------------------

By defining

.. math::
   m(r) = \frac{1}{2} r ( 1 - e^{-\Lambda(r)} ).

the 00 component of the Einstein equation is basically the mass function

.. math::
   m(r) = \int_0^r dr' 4\pi r'^2 \rho(r').



The other components leads to the famous TOV equation

.. math::
   \frac{dp}{dr} = - \frac{ (\rho+p(r))(m(r) + 4\pi r^3 p(r)) }{ r(r-2m(r)) },
   :label: eqn-tov-equation

where :math:`m(r)` is the mass function.



.. admonition:: Newtonian Limit
   :class: note

   Newtonian limit of the same equation is

   .. math::
      \frac{dp}{dr} = -\frac{ {\color{red}\rho(r)} {\color{blue}m(r)} }{ r^2 },
      :label: eqn-dp-dr-newtonian

   which can be derived by looking at a shell of mass at radius :math:`r`.

   To derive this we need to construct a shell of mass at radius :math:`r`. At this shell gravity is balanced by pressue since we assumed a static star.


.. admonition:: Interpretation of TOV equation
   :class: note

   We can make sense of it and cast it into a more Newtonian form. We know that proper distance

   .. math::
      dl = \sqrt{g_{rr}} dr = e^{-\Lambda} dr = (1-2m/r)^{-1} dr.

   Then we rewrite :eq:`eqn-tov-equation` as

   .. math::
      \frac{dp}{dl} = - \frac{ {\color{red}(\rho+  p(r))} {\color{blue}(m(r) + 4\pi r^3 p(r))} }{ r^2 }.
      :label: eqn-tov-proper-length


   The term :math:`{\color{red}(\rho+  p(r))}` corresponds to the contribution from the shell of mass :math:`{\color{red}\rho(r)}` in Newtonian theory :eq:`eqn-dp-dr-newtonian`. The reason that we obtained a new contribution from pressure is that pressure is also the source of gravity. The second term is the total contribution of mass inside the shell. For a similar reason we pick up a pressure term in relativity.



   The TOV equation with proper length :eq:`eqn-tov-proper-length` has some very interesting implications. Suppose we are at a coordinate radius :math:`r` of a star. We measure the pressure gradient :math:`\frac{dp}{dr}\vert_r`. Then we restrict ourselves on this shell at radius :math:`r`. Then what we experience is basically a Newtonian-like :math:`1/r^2` law.



.. admonition:: However
   :class: warning

   However, the second term in :math:`{\color{blue}(m(r) + 4\pi r^3 p(r))}` is kind of strange. It seems that we need no knowledge of pressure inside the shell to get the pressure gradient. It is not simply the total mass contribution from inside.

   Something is not right.




References and Notes
----------------------------

.. [Schutz] A First Course in General Relativity (Second Edition)
