Stars
====================================


.. admonition:: Question
   :class: warning

   What Are The Typical Masses of Stars?


A star is typically formed from a cloud of gas which is contracted and reaches a stable state. Suppose we can find the relation between the temperature and mass of the star, we could use our knowledge of nuclear physics to determine the temperature scale thus the mass of the star could be calculated.

.. admonition:: Typical Pressure
   :class: note

   A star starts from a gas cloud which is divided into inner part and outer shell in order to estimate the typical pressure caused by gravitational force,

   .. math::
      P_G &\sim \frac{F_G}{A} \\
      &\sim  \frac{G \frac{M}{2}  \frac{M}{2}}{ R^2 4\pi r^2} \\
      &\sim \frac{2^{2/3}GM^2}{16\pi R^4} ,

   where :math:`r` is the radius of the inner radius which has a mass of :math:`\frac{M}{2}`, :math:`R` is the radius of the whole gas cloud which has total mass :math:`M`, and the outer shell of the gas also has mass :math:`M- \frac{M}{2} =  \frac{M}{2}`, :math:`A` is the area on the contact of the inner shpere and the outer shell.


The cloud collapses with these gravitational potential energy goes into Fermi energy and kinetic energy of the molecules. It is convinient to calculate the gravitatioinal potential energy per proton (from Hydrogen),

.. math::
   \epsilon_G = \frac{G m_p^2 N^2}{R N},

in which :math:`m_p` is the mass of a proton while :math:`N` is the number of protons. Define number density

.. math::
   n = \frac{N}{\frac{4}{3} \pi R^3},

which helps rewrite the radius

.. math::
   R \sim \left(\frac{N}{n}\right)^{1/3}

so that the gravitational potential energy becomes

.. math::
   \epsilon_G \sim n^{1/3}.

Switching to a microscopic view of the particle we could identify the total potential energy of the particle, which is composed of thermal energy :math:`kT` and Fermi energy :math:`\frac{h^2}{2m_e}( 3\pi^2 n )^{2/3}`. The conservation of energy is, roughly,

.. math::
   kT + \frac{h^2}{m_e} n^{2/3} \sim G m_p^2 N^{2/3} n^{1/3}.

Solve the thermal energy

.. math::
   kT \sim G m_p^2 N^{2/3} n^{1/3} -  \frac{\hbar^2}{m_e} n^{2/3},

which has a maximum value located at :math:`n_\ast`,

.. math::
   \frac{\hbar^2}{m_e} n_\ast^{-1/3} - G m_p^2 N^{2/3} n_\ast^{-2/3} \sim 0.

We find the critical value of number density :math:`n_\ast`

.. math::
   n_\ast &\sim  \left( \frac{G m_p^2 N^{2/3} m_e }{\hbar^2} \right)^3 \\
   &\sim \frac{\alpha_G}{\lambda_e} N^{2/3},

where :math:`\alpha_G` is a dimension quantity related to the gravity between two protons while :math:`\lambda_e` is the Compton wavelength of electron,

.. math::
   \alpha_G &= \frac{G m_p^2}{\hbar c} \\
   \lambda_e & = \frac{\hbar}{m_e c}.

Thus the maximum temperatur is

.. math::
   k T_m \sim \alpha_G N^{4/3} m_e c^2.


As long as we could find a constraint on temperature, the mass of the star could possibily be determined with this relateion. The constraint on temperature comes from the nuclear reaction since the temperature should be able to sustain some kind of nuclear fusion.

The simplest nuclear fusion is Hydrogen to Deuterium which requires the wave packet of two proton to overlap. This overlap distance is related to a Couloumb potential energy.

The overlap distance is de Broglie wavelength of the protons,

.. math::
   \lambda_b \sim \frac{\hbar}{m_p c},

in relativistic limit if the temprature is comparable or higher than the mass of a proton.

The coresponding Coulomb potential using Gaussian unit is

.. math::
   \epsilon_n \sim \frac{e^2}{\lambda_b} \sim \alpha^2 m_p c^2,

where :math:`\alpha` is fine structure constant. In Gaussian unit

.. math::
   \alpha = \frac{e^2}{\hbar c}.


.. admonition:: More Accuracy
   :class: note

   In fact we could put in a factor :math:`\eta \sim 0.1` for the estimation of energy

   .. math::
      \epsilon_n = \eta \alpha^2 m_p c^2.

   This step is not require for an estimation.

**For a star to exist, we require the temperature is higher than this nuclear ignition energy**.

.. math::
   k T > \epsilon_n.

To estimate the mass of the star we find the critical number of protons in this problem by using the condition that :math:`kT_m \sim \epsilon_n`, which results in

.. math::
   N_\ast \sim \left( \frac{m_p}{m_e} \right) \left( \frac{\alpha}{\alpha_G}  \right)^{3/2}.


This is about the value :math:`10^{56}` and the corresponding mass is about :math:`10^{29}\mathrm{kg}` or :math:`0.1 M_\odot`. **We have obtained the lower limit of a star.**







.. admonition:: Question
   :class: warning

   How bright is the Sun?



The Sun has layers callled

1. Corona which goes into the interplanetary medium;
2. Chromosphere;
3. Photosphere which we see in visible light and contains absorption line (Fraunhof lines).


Brightness in a sense can be represented using power. Here we are going to calculate the power of the Sun using the knowledge we know at Earth.

In the Earth atmosphere, the light is partially obsorbed, which requires knowledge of obsorption which is described by

.. math::
   I(\theta,z) = I_0 e^{-kz/cos\theta},

according to which observation on the surface is enough to find out the actually energy arrived at Earth per unit area assuming perpendicular incident.

The result is :math:`S\equiv I(0,0) = I_0 = 1360 \mathrm{W/m^2}`. The fact is only 40 percent of the light reaches the surface and due to the O zone almost no light with wavelength under :math:`1\AA` is coming through.

The total power of the Sun is

.. math::
   L_\odot = 4\pi R_\odot^2 S = 3.8\times 10^{26}\mathrm{W}.


Assuming the Sun emmits black body radiation, the corresponding temperature is :math:`T_\odot = 5760\mathrm{K}`.

.. admonition:: Stefan-Boltzmann Law
   :class: note

   Energy radiated per unit area per unit time of black body radiation is

   .. math::
      j = \sigma_{SB} T^4,

   where :math:`\sigma_{SB} = \frac{2\pi^5 k^4}{15 c^2 h^3} = 5.67\times 10^{-8}\mathrm{W m^{-2} K^{-4}}`.

   As a reference, 100K black body radiation has an energy flux of :math:`5.67\mathrm{W/m^2}`.



.. admonition:: Question
   :class: warning

   What is the composition of the Sun?


Absorption line from photosphere is the tool to identify the elements and abundance in the sun.

1. Identify the absorption lines;
2. Physical conditions related to the source of these lines, such as electron and ion temperature, pressure and density;
3. Atomic physics that is responsible for the strenght of the lines.


We can find out the density for a state of the element which is called "column" density, *N h* where *N* is the number density of the state and *h* is the depth the light is going through.





.. admonition:: Question
   :class: warning

   What is the age of the solar system?


**Before humanbeings actually realized the radioactivity, people did estimations of the Sun by assuming the energy source is GRAVITY which is so wrong.** The way they did it is to calculate the total potential energy contained in a process that a cloud collapses to the size of the Sun. These energy goes to light so we know the upper limit of the age of our Sun since we know the power of it.

A spherical ball has potential energy

.. math::
   V = \frac{k G M^2}{R},

where :math:`k=\frac{3}{5}` for a uniform ball and :math:`k=1.74` for our sun.

Assuming that the Sun is emmitting light constantly, which is :math:`S= 1360\mathrm{W/m^2}` per unit area at surface, we have

.. math::
   4\pi R_\odot^2 S = -\frac{dV}{dt}

we find :math:`t < 55 \mathrm{Myr}`.




Nowadays we find out the age of the solar system by looking into the isotop abundance.

We have a lot of decays that can be used for dating.

The idea behind this method is that since some of the isotopes decay the abundance will decrease and the abundance of the daughter will increase.

Decays is

.. math::
   \frac{dN(t)}{dt} = -\lambda N(t),

which has a solution

.. math::
   N(t) = N(0) e^{-\lambda t}.

We know the half life :math:`\tau` which determines :math:`\lambda` through :math:`\tau = \ln 2/\lambda`.

We don't know :math:`N(0)` so we need to use the abunddance of daughter,

.. math::
   D^*(t) = N(0) - N(t) = N_0(1-e^{-\lambda t}),

then we have

.. math::
   \frac{D^*(t)}{N(t)} = e^{\lambda t} - 1.

As long as we know the initial daughter abundance we can find out the age.












Refs and Notes
------------------------
