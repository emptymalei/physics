.. index:: doppler-shift

Doppler Effect
=======================


Doppler shift in special relativity is always confusing. I'll demonstrate doppler shift in four different ways.



Conservation of Four Momentum
--------------------------------------------------


The special relativistic doppler shift can be derived using the fact that 4-momentum is a vector thus it transforms under Lorentz transformation.


.. figure:: assets/doppler-shift-configuration.png
   :align: center

   The observer frame is moving in x direction only.


The observer is fixed in observer frame and source of emission is in emission frame.

The observer detects an angle of light ray :math:`\theta_o`. However, the emission angle :math:`\theta_e` is different from this angle, i.e., :math:`\theta_e \neq \theta_0`.

.. admonition:: Which Angle to Use
   :class: warning

   Which angle to use then? In theory, we can derive the Doppler shift in terms of either angles. We present both of the analysis. The redshift expressions looks different because they are measuring different events.

Components of four momentum in observer frame is

.. math::
   p_o^\mu = \begin{pmatrix} E_o & E_o \cos\theta_o & E_o\sin\theta_o & 0 \end{pmatrix}.

The components in the emission frame is

.. math::
   p_e^\mu = \begin{pmatrix} E_e & E_e \cos\theta_e & E_e\sin\theta_e & 0 \end{pmatrix}.



.. admonition:: Redshift
   :class: note

   Redshift is define as

   .. math::
      z &= \frac{\nu_e - \nu_o}{\nu_o} \\
      & = \frac{\omega_e - \omega_o}{\omega_o}.


.. admonition:: Non-relativistic Doppler Shift

   To understand the effect of relativity, we would first recall the non-relativistic doppler shift.

   .. math::
      \omega_{o,non-rel} = \omega_{e,non-rel}(1-v/c \cos\theta).
      :label: eqn-non-relativistic-redshift-angular-frequency

   where no :math:`\gamma` is relavent. It's obvious that we have only two kinds of shift, redshift due to the source is closing, or blueshift due to the fact that the source is moving away.



Redshift Relation to Angle in Emission Frame
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Since momentum is a vector, we have the Lorentz transformation which transfrom it in to :math:`O_o` frame,

.. math::
   \frac{E_o}{c} = \gamma \left(\frac{E_e}{c} - \beta p_e^1\right),

where we also have

.. math::
   p_e^1 &= p_e^0\cos\theta_e,\\
   p_e^0 &= E_e/c.


Combining these equations, the energy of the photons in :math:`O_e` frame is

.. math::
   E_o = E_e \gamma (1 - \beta \cos\theta_e).

In quantum mechanics, energy is related to angular frequency,

.. math::
   E_{o/e} = \hbar \omega_{o/e}.

The angular frequency in O' frame is

.. math::
   \omega_o = \omega_e \gamma (1-\beta \cos\theta_e).
   :label: eqn-angular-frequency-emission-angle

In fact, :math:`\beta=v` if we choose :math:`c=1`.


Redshift Relation to Angle in Observor Frame
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The problem is, we know that :math:`\theta_e\neq\theta_o`. In many cases, it's more convinient to obtain the angle in observation frame :math:`\theta_o`.

In this case, we Lorentz transform the representation of four momentum in observer frame (:math:`p_o^\mu`) to emission frame (:math:`p_e^\mu`).

.. math::
   \frac{E_e}{c} = \gamma(\frac{E_o}{c}+\beta p_o^1),

where

.. math::
   p_o^1 &= p_o^0 \cos \theta_o \\
   p_o^0 &= E_o/c.

We solve the angular frequency for photons in observer's frame

.. math::
   \omega_o &= \frac{\omega_e}{\gamma(1+\beta \cos \theta_o)}\\
   &= \omega_e\frac{\sqrt{1-\beta^2}}{(1+\beta \cos \theta_o)},
   :label: eqn-angular-frequency-observation-angle

where in the last step we applied

.. math::
   \gamma = 1/\sqrt{1-\beta^2}.

Eq. :eq:`eqn-angular-frequency-observation-angle` seems to be very different from :eq:`eqn-angular-frequency-emission-angle`. The reason is that we are measuring different events, due to the difference between :math:`\theta_e` and :math:`\theta_o`.

Eq. :eq:`eqn-angular-frequency-observation-angle` is what usually used in discussion of relativistic Doppler effect.

.. admonition:: Line-of-sight Direction Same as Relative Velocity Direction
   :class: note

   :math:`\theta_o=\theta_e=0` gives us the most used Doppler shift

   .. math::
      \omega_o=\omega_e\sqrt{ \frac{1-\beta}{1+\beta} }.
      :label: eqn-line-of-sight-motion-doppler-angular-frequency


:math:`\beta=v` if we choose :math:`c=1`.


Relativistic Effect
~~~~~~~~~~~~~~~~~~~~~~~~~~

Nonrelativistic Doppler shift :eq:`eqn-non-relativistic-redshift-angular-frequency` contains only the effect of line-of-sight relocity.

Relativistic Doppler shift :eq:`eqn-angular-frequency-observation-angle` we have new contributions from relative velocity, which is the transverse redshift due to the :math:`\gamma` factor or the contraction of time.

If the motion is in line-of-sight, Eq. :eq:`eqn-line-of-sight-motion-doppler-angular-frequency` is reduced to the nonrelativistic Doppler shift for slow velocity :math:`v` as we take only first order of its Tayler series.

For motion that is not along the line-of-sight, angle difference becomes important, since we have to choose the equal time surface.

An gif from wikipedia shows this explicitly,

.. figure:: ../assets/special-relativity/XYCoordinates.gif
   :align: center

   Image Source: `File:XYCoordinates.gif <https://en.wikipedia.org/wiki/File:XYCoordinates.gif>`_


The change in wavelength is given by

.. math::
   \frac{\lambda_{obs} }{ \lambda_{src}  }= \sqrt{ \frac{1 - \beta}{1 + \beta} } .


Four Vector Language
----------------------------------

Doppler shift can be solve using abstract four vectors without going into a coordinate system [CBLiang]_.

First of all we associate the emission frame and observation frame with its own four velocities, :math:`V^a` and :math:`U^a`.

From the knowledge of special relativity, we know that

.. math::
   E_o/c = -p^a U_a\vert_{obs},

where :math:`U^a` is the four velocity of observer, subscript :math:`{}_{obs}` indicates this is the measurement at observation point.

The photon energy in emission frame is

.. math::
   E_e/c = - p^a V_a\vert_{em},
   :label: eqn-energy-emission-v-frame

which is calculated at the point of emission. :math:`V^a` is the four velocity of the emission frame.

Since inner product is independent of the physical point in special relativity, we can calculate the both energy at the same physical point.

We also know that

.. math::
   \gamma = -V^a U_a,

which associates the four velcoities

.. math::
   U_a = \gamma V_a + \gamma u_a,
   :label: eqn-u-a-decomposition-to-v

where :math:`\gamma u_a` is the three velocity component viewed by :math:`V_a`.

.. admonition:: The Instataneous Frame Decomposition
   :class: toggle

   We always have to define our equal time surface first. Here we can see that :math:`\gamma u_a` is indeed a decomposition onto our spatial surface.

   Multiply on both sides of Eq. :eq:`eqn-u-a-decomposition-to-v` by :math:`V^a`,

   .. math::
      V^a u_a =0.


We also know from Eq. :eq:`eqn-energy-emission-v-frame`

.. math::
   p^a = \omega V^a + k^a.

To collect our thoughts, we have obtained from the four momentum and our velocities :math:`u^a` and :math:`k^a`, which are the quantities we would like to work on in 3D space.

Finally, we calculate the frequency in observer's frame,

.. math::
   \omega_o &= -p^a U_a \\
   &=-(\omega V^a + k^a)(\gamma V_a + \gamma u_a) \\
   & = \gamma (\omega - k^a u_a),

where

.. math::
   k^a u_a = v \omega \cos \theta_e.

Then we obtain the Doppler shift equation

.. math::
   \omega_o = \omega_e \gamma (1-v\cos\theta_e).


We can work out this using another projection of spatial dimensions, which is give us the frequency relation in terms of observation angle :math:`\theta_o`.


.. [CBLiang] 梁灿彬，周彬，《微分几何与广义相对论入门》



Spacetime Diagram
-----------------------

Needless to say, it can be explained using spacetime diagram. The only caveat is to pay attention to the equal time surface.

I am just too lazy to make a spacetime diagram with six axes here. You get the idea.
