.. index:: doppler-shift

.. _doppler-shift:

Doppler Effect
=======================


Doppler shift in special relativity is always confusing. I'll demonstrate doppler shift in four different ways.



Conservation of Four Momentum
--------------------------------------------------


The special relativistic doppler shift can be derived using the fact that 4-momentum is a vector thus it transforms under Lorentz transformation.


.. image:: assets/doppler-shift-configuration.png
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



Since momentum is a vector, we have the Lorentz transformation which transfrom it in to :math:`O_o` frame,

.. math::
   \frac{E_o}{c} = \gamma \left(\frac{E_e}{c} - \beta p_e^1\right),

where we also have

.. math::
   p_e^1 &= p_e\cos\theta_e,\\
   p_e &= E_e/c.



.. admonition:: Redshift
   :class: note

   Redshift is define as

   .. math::
      z &= \frac{\nu_e - \nu_o}{\nu_o} \\
      & = \frac{\omega_e - \omega_o}{\omega_o} \\
      & = \frac{1/\gamma - 1 + \beta\cos\theta}{1-\beta \cos\theta}.


.. admonition:: Non-relativistic Doppler Shift

   To understand the effect of relativity, we would first recall the non-relativistic doppler shift.

   .. math::
      \omega'_{non-rel} = \omega_{non-rel}(1-v/c \cos\theta).

   where no :math:`\gamma` is relavent. It's obvious that we have only two kinds of shift, redshift due to the source is closing, or blueshift due to the fact that the source is moving away.



Redshift Relation to Angle in Emission Frame
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Combining these equations, the energy of the photons in O' frame is

.. math::
   E_o = E_e \gamma (1 - \beta \cos\theta_e).

In quantum mechanics, energy is related to angular frequency,

.. math::
   E_{o/e} = \hbar \omega_{o/e}.

The angular frequency in O' frame is

.. math::
   \omega_o ' = \omega_e \gamma (1-\beta \cos\theta_e).



Redshift Relation to Angle in Observor Frame
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The problem is, we know that :math:`\theta_e\neq\theta_o`. In many cases, it's more convinient to obtain the angle in observation frame :math:`\theta_o`.

In this case, we Lorentz transform the representation of four momentum in :math:``


Relativistic Effect
~~~~~~~~~~~~~~~~~~~~~~~~~~


Here we have three different kinds, the additional one is the transverse redshift due to the :math:`\gamma` factor or the contraction of time.


An gif from wikipedia shows this explicitly,

.. figure:: ../assets/special-relativity/XYCoordinates.gif
   :align: center

   Image Source: `File:XYCoordinates.gif <https://en.wikipedia.org/wiki/File:XYCoordinates.gif>`_


The change in wavelength is given by

.. math::
   \frac{\lambda_{obs} }{ \lambda_{src}  }= \sqrt{ \frac{1 - \beta}{1 + \beta} } .


Four Vector Language
----------------------------------

From the knowledge of special relativity, we know that

.. math::
   E_o = p^a U_a,

where :math:`U_a` is the four velocity of observer.
