Response of Matter
=================================



.. admonition:: Maxwell's Equations and Transfer of Momentum and Energy
   :class: note

   .. math::
      \nabla \cdot \vec D & = 4\pi \rho \\
      \nabla \cdot \vec B & = 0 \\
      \nabla \times \vec E & = -\frac{1}{c}\partial_t \vec B \\
      \nabla \times \vec H & = \frac{1}{c}\partial_t \vec D + \frac{4\pi}{c} \vec j .



Energy and Momentum
-----------------------



Energy transfer can be described through Poynting vector which in the simplist plane wave case is basically :math:`\langle \vec S \rangle = u_{EM}\vec v` where :math:`u_{EM}` is the energy density. Obviously Poynting vector is the energy transfer rate. 

Momentum density is :math:`\vec g = \frac{u_{EM}}{c}` in the same plane wave.


Let's start from conservation of charge. Taking the divergence of the following equation,

.. math:：
   \nabla \times \vec H = \frac{4\pi}{c} + \frac{1}{c} \partial_t \vec D,

I get the conservation law,

.. math::
   \partial_t \rho + \nabla \cdot \vec j = 0.


On the next step we find energy density of the wave. The starting point is the interaction of charge and electric field, e.g., :math:`\vec j \cdot \vec E`, :math:`q\vec E \cdot d`.

.. math::
   u_{EM} = \frac{1}{8\pi} (\vec D \cdot \vec E + \vec B \cdot \vec H).


Upon this we can find :math:`\vec S` which is

.. math::
   \vec S = \frac{c}{4\pi} \vec E \times \vec H.

As for momentum, we have 

.. math::
   \vec F_{EM} = \oint d\vec a \cdot \mathbf{T} - \frac{d}{dt}\int \vec g(\vec x) d^3x,

where 

.. math::
   \vec g =  \frac{\vec S}{c^2} = \frac{\vec E \times \vec B}{4\pi c}.





Response of Matter
-------------------------

The equation for monochromatic wave,

.. math::
   \vec k \cdot \vec D &= 4\pi \rho \\
   \vec k \cdot \vec B & = 0 \\
   \vec k \times \vec E & = i \omega \vec B \\
   \vec k \times \vec H & = - \frac{i\omega}{c} \vec D + \frac{4\pi}{c} \vec j.


In the case of :math:`\rho=0` (no free charge) and :math:`\vec j=0` no free current,

.. math::
   \vec k \cdot \vec E &= 0 \\
   \vec k \cdot \vec B & = 0 \\
   \vec k \times \vec E & = i \omega \vec B \\
   \vec k \times \vec B & = - \frac{i\omega}{c}\epsilon \mu \vec E.


The important relation is dispersion relation which is the relation between wave number and frequency. In this context,

.. math::
   \vec k \cdot \vec k = \frac{\omega^2}{c^2} \mu \epsilon,

which reduces to

.. math::
   k = \frac{\omega}{c/n}

as now we can define a new velocity which stands for the phase velocity by

.. math::
   v_{ph} = c/n.


Impedance
~~~~~~~~~~~~~~~~~~~~
   
Since :math:`\vec E` corresponds to the magnetic part :math:`\vec H`, we would like to rewrite one of the equation to

.. math::
   Z \vec H = \vec k \times \vec E.

where 

.. math::
   Z = \sqrt{\frac{\mu}{\epsilon}}.


If :math:`\mu=1`, we have

.. math::
   Z = \frac{1}{n}.



Matching Condition
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Matching conditions are not just something written down on the textbook. They all have meanings.

.. math::
   \hat n \cdot (\vec D_1 + \vec D_1' - \vec D_2) &= 0, \\
   \hat n \cdot (\vec B_1 + \vec B_1' - \vec B_2) &= 0, \\
   \hat n\times (\vec E_1 + \vec E_1' - \vec E_2) &= 0, \\
   \hat n \times (\vec H_1 +\vec H_1' - \vec H_2) &=0.



In order to satisfy these matching conditions, the phase of all fields should be the same. Thus leading to the Snell's law

.. math::
   \theta_1 &= \theta_1' \\
   n_1 \sin\theta_1 &= n_2 \sin\theta_2 \qquad \text{perpendicular part}.


The parallel parts of the fields give us the other relation,

.. math::
   E_1\cos\theta_1 - E_1'\cos\theta_1 - E_2 \cos\theta_2 &= 0 \\
   H_1 + H_1' = H_2 .





Reflected and Transmitted Wave
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Recall that impedance is :math:`Z = \sqrt{\frac{\mu}{\epsilon} }` which leads to or corresponds to 

.. math::
   \lvert E \rvert = Z \lvert H \rvert.

**Impedance shows the scaling between the magnetic field and the electric field.** In fact for monochromatic TEM,

.. math::
   \vec k \times \vec E =  Z \vec H.


Then we derive the ratios,

.. math::
   \frac{E_1'}{E_1} &= \frac{Z_1\cos\theta_1 - Z_2\cos\theta_2}{Z_1\cos\theta_1 + Z_2\cos\theta_2}, \\
   \frac{E_2}{E_1} &= \frac{2Z_2 \cos\theta_1}{Z_1\cos\theta_1 + Z_2\cos\theta_2} .


By definition, impedance becomes :math:`Z = 1/n` when :math:`\mu=1`. In this limit,

.. math::
   \frac{E_1'}{E_1} &= \frac{n_2\cos\theta_1 - n_1\cos\theta_2}{n_2\cos\theta_1 + n_1\cos\theta_2}, \\
   \frac{E_2}{E_1} &= \frac{2n_1 \cos\theta_1}{n_2\cos\theta_1 + n_1\cos\theta_2} .


Now what I need to be careful is that in this derivation, I used the geometry to project the fields on to the surface where the polarization of the wave matters. For the result above, they are only valid for waves with polarization parallel to the surface.


Using similar tricks, I can write down the result for waves with polarization perpendicular to surface. The matching conditions are

.. math::
   E_1 + E_1' &=  E_2 \\
   H_1 \cos\theta_1 - H_1'\cos\theta_1 = H_2\cos\theta_2.

This can be abtained by just draw a graph of the incident wave, reflected wave and refracted wave.

Solving the equations

.. math::
   \frac{E_1'}{E_1} &= \frac{n_1\cos\theta_1 - n_2\cos\theta_2}{n_1\cos\theta_1 + n_2\cos\theta_2}, \\
   \frac{E_2}{E_1} &= \frac{2n_1 \cos\theta_1}{n_1\cos\theta_1 + n_2\cos\theta_2} .






Reflection, Refraction, Transparent, Dissipative
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Reflection coefficient and transmission coefficient find the energy reflected and transmitted.

.. math::
   R & = \frac{\langle \vec S_1' \rangle \cdot \hat n}{\langle \vec S_1 \rangle \cdot \hat n} \\
   & = \frac{\frac{c}{4\pi}\frac{1}{2} Re( \vec E_1'^* \times \vec H_1' )   }{ \frac{c}{4\pi} \frac{1}{2} Re( \vec E_1^* \times \vec H_1 ) } \\
   & = \cdots \\
   T& =  \frac{\langle \vec S_2 \rangle \cdot \hat n}{\langle \vec S_1 \rangle \cdot \hat n} \\
   & = \cdots


For normal incident, these becomes easier to calculate because all thetas becomes 0. The result is

.. math::
   R &= \frac{( n_1-n_2)^2 }{ (n_1+n_2)^2 } \\
   T &= \frac{ 4n_1 n_2 }{  (n_1+n_2)^2 }.



Evanescent wave is the case when the wave vector becomes imaginary and the wave tenuates to 0 quickly. In the situation of total reflection, the transmitted wave can be calculated. To find out the evanescent wave one need to calculate the condition for total reflection then plug in the condition for a assumed wave in medium 2.


Evanescent wave doesn't mean energy lose in reflection, it only proves that wave can not go deep into the material and all waves are reflected. The material does NOT nessarily obsorbe all the energy of the wave. One can show that in total reflection, energy flowing in all flows out, i.e.,

.. math::
   R=1.


The question is, what is dissipative material? They are those with complex wave vectors such that wave dissipates as they passing through the bulk material.



Ohmic Matter
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


A term of current

.. math::
   \frac{4\pi}{c}\vec j

is added to the equations so that it describes matter which supports current.

Ohm's law shows the relations between current and field,

.. math::
   \vec j = \sigma \vec E.

By plug in this to the Maxwell's equations, we can have a new permitivity. For monochromatic wave,

.. math::
   \epsilon = \epsilon_R + i\frac{4\pi\sigma}{\omega}.

Using dispersion relation derived, we can define the complex refractive index.


Given the dispersion relation we could also find the waves and calculate Poynting vector

.. math::
   \langle \vec S \rangle \propto e^{−2(\omega n_i/c)\hat k\cdot x}.

This is our anticipation since the wave vector has a length of :math:`k=\frac{\omega}{c/(n_R+i n_I)}` due to dispersion relation :math:`\vec k=\frac{\omega}{c/n}\hat k`. Plug this into the expression for plane wave, we have the spatial part proportional to

.. math::
   e^{\vec k \cdot \vec x} & = e^{i(n_R+i n_I)\omega/c \hat k \cdot \vec x}\\.

We can directly see the damping part. This is how one finds the skin depth which means the Poynting vector drops to :math:`1/e` of that of the incident wave,

.. math::
   \delta = \frac{c}{2\omega n_i}.

If the imaginary part becomes very large, i.e.,

.. math::
   \frac{4\pi\sigma}{\omega} \gg 1,

the atenuation becomes significant or both real part and imaginary part of refractive index becomes much larger than 1. This is equivalent to good conductor. We can see the skin depth

.. math::
   \delta \ll \frac{c}{\omega}.


Refrective index also becomes 1. 


Remember surface current is defined as

.. math::
   \vec K = \int\vec j dz.

We could use this to find a effective surface current. Current density is

.. math::
   \vec j &= \sigma \vec E \\
   & = \sigma \vec E_0 e^{i (\vec k \cdot \vec x - \omega t)}.

Using dispersion relation, and suppose we have wave vector in z direction. We can write down the incident wave

.. math::
   \vec E_1 = \vec E_0 e^{i \omega (n z/c - t)} .

Fresnel's relation tells us the refracted wave, which is

.. math::
   \vec E_2 &= \frac{2\vec E_1}{n+1} \\
   &\approx \frac{2\vec E_1}{n} \\
   &= \frac{2\vec E_1}{(1+i)n_R}.

The last step is true for good conductor. The current density is therefore clear so is the surface current.



In summary, good conductor has a

1. small skin depth;
2. large n for both real and imaginary part;
3. almost 1 as the reflection coefficient.



Dispersive Media
~~~~~~~~~~~~~~~~~~~~~~~~~


Dispersive media can be modeled using Drude model, Lorentz model and many other. Read :ref:`drude-model` and :ref:`lorentz-model` in vocabulary part.

By definition, group velocity is the result of dispersion relation,

.. math::
   v_g = \frac{d \omega}{dk}\vert_{k=k_0},


while phase velocity is always :math:`v_{phase} = nc` where n can be larger than 1.


Read `chapte 5 of Kevin Cahill's book <http://www.cambridge.org/us/academic/subjects/physics/mathematical-methods/physical-mathematics>`_ for knowledge of complex dispersion relation and more. Notice that both group velocity and phase velocity can be larger than the vacuum speed of light.












