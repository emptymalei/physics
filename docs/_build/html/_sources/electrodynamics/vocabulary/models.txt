Models
*********************


.. _drude-model:

Drude Model
===================


Drude models models the electromagnetic properties of conductors. In this simple model, electromagnetic interaction with the electromagnetic waves comes from the free charges governed by this equation of motion.

.. math::
   m\frac{d \vec v}{d t} = q \vec E - \frac{m \vec v}{\tau},

where :math:`\tau` is the damping term like the one in Brownian motion. In fact this is a Brownian motion like equation since :math:`\vec E` is periodic and averages to 0 in a simple case **except that this external electric force is not random**.

.. admonition:: Math
   :class: note

   Now consider the solution to this equation which is simple using Green's function,

   .. math::
      \vec v(t) &= \vec v(0) e^{-t/\tau} + \frac{q\vec E _0}{m}\int_0^t dt' e^{-(t-t')/\tau} e^{-i \omega t'}\\
      &= \vec v(0) e^{-t/\tau} + \frac{q\vec E_0}{m} e^{-t/\tau} \frac{i\tau (-1 + e^{t(1/2-i\omega)})}{\tau \omega + i}.

   The first term is the damping contribution to the velocity of the charges and the second term is the contribution of electric field.

   As a practice, we can show that the ratio of two contributions is

   .. math::
      M &= \frac{\lvert v_2 \rvert}{\lvert v_1 \rvert} \\
      & = \frac{1}{v(0)} \frac{q E_0}{m}  \frac{i\tau (-1 + e^{t(1/2-i\omega)})}{\tau \omega + i} \\
      & = \frac{q E_0}{m v(0)} \frac{i\tau ( e^{t/\tau (1-i\omega \tau)} - 1)}{i + \omega \tau}.

   It is obvious that in the limit :math:`\omega \tau \gg 1`, and after a long time this ratio becomes 0 which actually comes from the fact that :math:`\omega` is very large.

   This means that in a long run, the damping always takes over the system if we have a very large frequency. Now the next question is what is the energy contribution of electric field after a long time?

   .. math::
      \vec v_2(t) = \frac{q\vec E_0}{m} e^{-t/\tau} \frac{i\tau (-1 + e^{t(1/2-i\omega)})}{\tau \omega + i}

   becomes 0 as :math:`\omega` becomes large enough.

   So in a high frequency limit, the system take no energy from electric field.

   Note that this result is complex. Explain why is a velocity is complex.



In this model, what to calculate is the electromagnetic response of the material like reflection ration etc.



Maxwell Equations
------------------------------------

.. admonition:: Maxwell Equations
   :class: note

   \nabla\cdot \vec D  &= 4\pi \rho ,\\
   \nabla\cdot \vec B & = 0 ,\\
   \nabla \times \vec E & = -\frac{1}{c} \partial_t \vec B ,\\
   \nabla \times \vec H & = \frac{1}{c}\partial_t \vec D + \frac{4\pi}{c} \vec j .


In Drude model, for each mode :math:`\vec E, \vec B \propto e^{i(\vec k \cdot \vec )}`, I can replace :math:`\partial_t` with :math:`-i\omega` and :math:`\vec \nabla` with :math:`i\vec k`. With the help of this, the Maxwell's equation becomes

.. math::
   \vec k \cdot \vec D &= 4\pi \rho, \\
   \vec k \cdot \vec B & = 0, \\
   \vec k \times \vec E & = -\frac{1}{c} (-i\omega) \vec B, \\
   \vec k \times \vec H & = \frac{1}{c} (-i\omega) \vec D + \frac{4\pi}{c} \vec j.


Current Density
--------------------------

The current density is

.. math::
   \vec j = q n_q \langle \vec v \rangle.

Meanwhile, the Drude model tells us the velocity is governed by

.. math::
   m \frac{d \vec v}{dt} = q\vec E - \frac{m \vec v}{\tau},

where :math:`- \frac{m \vec v}{\tau}` is a damping term.

.. admonition:: Damping Term
   :class: note

   This damping term can also be interpreted as the mean free time or some kind of probability.


Plugin the current density we could find the equation for current density.

.. math::
   \vec j &= q n_q \langle \vec v \rangle \\
   & = \vec E \left( \frac{q^2 n_q \tau}{m(1 - i \omega\tau)} \right) \\

Ohm's law tells us that

.. math::
   \vec j = \sigma \vec E.

Now we can have a phenomelogical conductivity from Drude model,

.. math::
   \sigma(\omega) = \frac{q^2 n_q \tau}{m(1 - i \omega\tau)}.




Maxwell's Equation in Neutral Matter
----------------------------------------------------------------

Pluging in the current density we calculated previously, the Maxwell's equation becomes

.. math::
   \vec k \cdot \vec D &= 4\pi \rho, \\
   \vec k \cdot \vec B & = 0, \\
   \vec k \times \vec E & = -\frac{1}{c} (-i\omega) \vec B, \\
   \vec k \times \vec H & = \frac{1}{c} (-i\omega) \epsilon \vec E + \frac{4\pi}{c} \sigma \vec E.

Comparing with the equations in matter without free charge, where the transverse wave satisfies

.. math::
   \vec k \cdot \vec E &= 0, \\
   \vec k \cdot \vec B &=0, \\
   \vec k \times \vec E &= \frac{\omega}{c} \vec B, \\
   \vec k \times \vec H & = -\frac{\omega}{c} \vec D


we can find the expression for permitivity,

.. math::
   \epsilon = 1 + \frac{i \omega_p^2 \tau}{\omega(1- i\omega \tau)}.


since :math:`\mu=1`. In the result I defined

.. math::
   \omega^2 = e^2n_e\tau/m .


The next quantity is to calculate the refractive index with :math:`\mu=1`.

.. math::
   n = \sqrt{\epsilon\mu} = \sqrt{1 + \frac{i \omega_p^2 \tau}{\omega(1- i\omega \tau)} }.


In the limit of :math:`\omega \tau \gg 1`, refractive index becomes

.. math::
   n^2 = 1 - \frac{\omega_p^2}{\omega^2}.




Dispersion Relation
------------------------------




.. math::
   \vec k \times \vec E &= \frac{\omega}{c} \vec B, \\
   \vec k \times \vec H & = -\frac{\omega}{c} \vec D

gives us the dispersion relation. However, we need to make a choice that the field need to be broken into parts that is perpendicular and parallel to wave vector. For the transverse wave, we could write down

.. math::
   k^2 = \frac{\omega}{c}\epsilon.



.. _lorentz-model:


Lorentz Model
===========================


Drude model only considers the damping part of conducting charges. Lorentz model, considers the actually polarization inside medium, using a simple but efficient model.


In models about matter response to electromagnetic waves, we have to get the permitivity out of it and furthure calculate the refractive index.

Suppose we already know how to write down polarization,

.. math::
   \vec P = n \vec p,

which means the polarization is caused by a lot of small dipoles. At this point we are not binded to the calculation of the detailed expression of these small dipoles. Instead we are going to calculate the permitivity first then come back to have a look at the details.

In statics we know,

.. math::
   \vec D  = \vec E + 4\pi  \vec P \equiv \vec E + 4\pi \chi\vec E = \epsilon \vec E.

To find :math:`\epsilon` we need to establish the relation between :math:`\vec P` and :math:`\vec E` which is equivalently setting up the relation between :math:`n \vec p` and :math:`\vec E`.

Here we introduce Lorentz model. In this context, we consider the case that equation of motion for the charges are governed by

.. math::
   m\ddot {\vec x} = - e\vec E -m \omega_0^2 \vec x - \gamma m \dot{\vec x}.


Solve the equation of motion we have the relation between :math:`\vec x` and :math:`\vec E` thus we can write down

.. math::
   \vec P &=  n \vec p \\
   & = - e n \vec x \\
   & = -e n \frac{-e \vec E/m}{\omega_0^2 - \omega^2 - i \gamma \omega}\\
   & = \frac{e^2 n /m}{\omega_0^2 - \omega^2 - i \gamma \omega}\vec E .

Imediately, we have the permitivity

.. math::
   \epsilon &=  \epsilon_0 + 4\pi \chi \\
   & = 1 + 4\pi \frac{e^2 n /m}{\omega_0^2 - \omega^2 - i \gamma \omega}  \\
   & = 1 + \frac{\omega_p^2}{\omega_0^2 - \omega^2 - i \gamma \omega} ,

where we used the definition of plasma frequency

.. math::
   \omega_p^2 = \frac{4\pi n e^2}{m}.




Limits
---------------------------------

We have got three important parameters or arguments in Lorentz model, :math:`\omega_0`, :math:`\omega`, :math:`\gamma` and on overall :math:`\omega_p`. One should notice that in normal matter we would see :math:`\gamma \ll \omega_0\ll \omega_p`.

Three limits can be considered,

1. low frequency, :math:`\omega` is very small like :math:`\omega_0 - \omega \gg \gamma`;
2. critical, :math:`\omega  = \omega_0` where we have only :math:`-i\gamma \omega` appears in denominator;
3. intermediate, :math:`\omega_0 \ll \omega \ll \omega_p`;
4. very high frequency, :math:`\omega \gg \omega _p`.

The interesting thing is that in situation 3, we get back to Drude model.















