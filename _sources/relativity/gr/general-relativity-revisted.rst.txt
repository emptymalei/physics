*******************************
General Relativity Revisited
*******************************


This section lists the experiments which are used to test gravity theories
carried out on the earth.


The test of gravity theories can be viewed as test of the fundations of
gravity theories and the the theories themselves, say test of equivalent
principle and general relativity or f(R) gravity theory. Thus we should
break down general relativity theory into several stages. Here, we use
the following table to do so.

-  **Physical Fundations: Hyperthesis**:

+----------+-----------+-------+-------+-------+------+---------+
| Theory   | Mach      | WEP   | EEP   | SEP   | GC   | Notes   |
+==========+===========+=======+=======+=======+======+=========+
| GR       | Partial   | Y     | Y     | Y     | Y    |         |
+----------+-----------+-------+-------+-------+------+---------+

-  **Mathematical Description**:

+----------+-------------+------------+--------------+---------------------------------+
| Theory   | Topoplogy   | Manifold   | Connection   | Metric                          |
+==========+=============+============+==============+=================================+
| GR       |             |            | No torsion   | Non-metricity tensor vanishes   |
+----------+-------------+------------+--------------+---------------------------------+

-  **Theoretical Implifications**:

+--------+---------------------+-----------------+----------+-------+
| Theory | Gravitational Waves | Newtonian Limit | GR Limit | Notes |
+========+=====================+=================+==========+=======+
| GR     |          Y          |        Y        |          |       |
+--------+---------------------+-----------------+----------+-------+

Most items in mathematics are the same in different theories.

Hyperthesis
-----------

-  **WEP**: weak equivalence principle
-  **EEP**: Einstein equivalence principle
-  **SEP**: strong equivalence principle
-  **GC**, General Covariance
-  **Mach Principle**: gravity coupled to matter


Derivation of Field Equation
----------------------------

From postulations
~~~~~~~~~~~~~~~~~

1. General covirance
2. Linear approximation should be compatible with Newton’s thoery/Weak
   field and slow motion limit is Newton’s thoery of gravity
3. In theory regarding the metric, no higher than second derivative is
   envolved and the terms of second derivative is linear.

The first point is for the invariance of frames/coordinates. The second
point is for the success of Newtonian’s theory on our earth.

Why do we believe the third point? The answer is that we don’t have to.
Here we propose it is because the simplicity of such quasilinear
equations, i.e.,

.. math::
   F(\phi, \partial \phi) \partial^2\phi + G(\phi, \partial\phi) = 0

We have a bunch of theorems on this system, including its existance of
solutions, Couchy problem, wave propagation etc.

We can use both 1&2 and 1&3 to derive Einstein’s equation. That is 2 and
3 are identical when 1 is considered.

From Action
~~~~~~~~~~~

This is an application of stationary principal and Hilbert action or
Hilbert action plus a :math:`\Lambda`.

Lovelock’s Theorem
~~~~~~~~~~~~~~~~~~~~~

**The only possible second-order Euler-Lagrange expression obtainable in
a four dimensional space from a scalar density of the form**
:math:`\scr L = \scr L(g_{\mu\nu})` **is**

.. math::
   E^{\mu\nu} = \alpha \sqrt{-g} [ R^{\mu\nu} - \frac{1}{2} g^{\mu\nu}R ] +\lambda \sqrt{-g} g^{\mu\nu}

Thus modification could be

-  Metric tensor not a fundamental tensor
-  Higher than second order derivatives of the metric in the field
   equations
-  Not a four dimension space
-  Not rank (2,0) tensor field equations, non-symmetry of field
   equations under exchange of indices, or divergence field equations
-  non-locality

Birkhoff’s Theorem
~~~~~~~~~~~~~~~~~~~~~

**All spherically symmetric solutions of Einstein’s equations in vacuum
must be static and asymptotically flat, without** :math:`\Lambda`.

Actually, this can be extended to a :math:`\Lambda` space only keeping
the static result.

No-hair Theorems
~~~~~~~~~~~~~~~~~~~~~

**The generic final state of gravitational collapse is a Kerr-Newman
black hole, fully specified by its mass, angular momentum and charge**

Also, “in the context of General Relativity with a cosmological constant
all expanding universe solutions should evolve towards de Sitter
space.” [1]_ This is only valid in some situation.


.. [1] **R. M. Wald**. Asymptotic behavior of homogeneous cosmological models in the presence of a positive cosmological constant. Phys. Rev. D, 28(8):2118–2120, Oct 1983.


Vacuum Solutions
-------------------------------------------

The vacuum Einstein equation

.. math::
   R^{\mu\nu} - \frac{1}{2} g^{\mu\nu} R = 0,

which indicates that all constant metrics are solutions to vacuum Einstein equation.

Physically this doesn't make any sense, unless we impose that our universe is Minkowski like. From this point of view, vacuum Einstein equation is more general than our universe.



Perturbation Theory of General Relativity
--------------------------------------------

Gauge freedom is the freedom of choosing a coordinate system. Fixing a
gauge means choosing a particular coordinate system.

Gauge tranformation is Lie derivative along some arbitary vector here.

Line element

.. math::
   \tilde g _ {00} &=& -a^2(1+2 A Y) \\
   \tilde g _ {0j} &=& -a^2 B Y _ j \\
   \tilde g _ {ij} &=& a^2(\gamma _ {ij} +2 H _ L Y \gamma _ {ij} +2 H _ T Y _ {ij} )

Energy momentum tensor is

.. math::
   \tilde T^0 _ {\phantom{0}0} = -\rho (1+\delta Y) \\
   \tilde T^0 _ {\phantom{0} j} = (\rho + p)(v - B) Y \\
   \tilde T^j _ {\phantom{j}0 } = -(\rho + p)v Y^{j}


For a infinitesimal gauge transformation along some vector
(:math:`X = T \partial_t + L^i \partial_i`), gauge
variables are

+----------------------------+-----------+------------------------+--------+
| Symbol                     | Physics   | Gauge Transformation   | Note   |
+============================+===========+========================+========+
| :math:`\tilde A`           |           |                        |        |
+----------------------------+-----------+------------------------+--------+

Through that we can find out gauge invariant variables.



What Frame Are We In
------------------------

Synge once said, use space and time, and define them.

This post is aimed to make clear what frame are we in.


In general relativity, we often transform coordinates. Here is an
example.

**The general form of metric with spherical space component is**

.. math::
   \mathrm ds^2 = - \gamma(r,t)c^2\mathrm dt^2 + \beta(r,t)c\mathrm dr\mathrm dt + \alpha(r,t)[\mathrm dr^2 + r^2 (\mathrm d\theta^2 + \sin^2\theta \mathrm d\phi^2)]
   :label: MetricForm1

With a transformation :math:`\alpha(r,t)r^2 = r'^2`,

.. math::
   \mathrm ds^2 = - \gamma'(r',t)c^2\mathrm dt^2 + \beta'(r',t)c\mathrm dr\mathrm dt + \alpha(r,t)[\mathrm dr^2 + r^2 (\mathrm d\theta^2 + \sin^2\theta \mathrm d\phi^2)]

Then compose the integral multiplier

.. math::
   c\mathrm dt'= \eta(r',t) [ - \gamma'(r',t) c \mathrm dt + \frac{1}{2} \beta'(r',t)\mathrm dr']

And finally,

.. math::
   \mathrm ds^2 = -\eta^{-2}(r',t) \gamma'^{-1}(r',t)c^2\mathrm dt'^2 + [\alpha'(r',t) + \frac{\beta'^2(r',t)}{4r'} ]\mathrm dr'^2 + r'^2(\mathrm d\theta^2 + \sin^2\theta\mathrm d\phi^2)

In general

.. math::
   \mathrm ds^2 = -b(r,t)c^2\mathrm dt^2 + a(r,t)\mathrm dr^2 + r^2(\mathrm d\theta^2 + \sin^2\theta\mathrm d\phi^2)
   :label: MetricForm2

Then what? The two forms of metric demonstrate different properties.
Take Birkhoff theorem as an example. The results could be very different
startting from the form :eq:`MetricForm1` and :eq:`MetricForm2`.

It is obviously very important to show what the coordinate
transformation means and what frame are the observers in indicated by
the coordinates.


Experiments
-----------

Eotvos Torsion Balance
~~~~~~~~~~~~~~~~~~~~~~

How
^^^

-  Inertial mass :math:`m_I`
-  Gravitational mass :math:`m_G`

In Newtonian system, the acceleration of an object will be

.. math::
   \vec a  \propto \frac{\vec F}{m_I}.

In a static and uniform gravitation field, the gravity force is

.. math::
    G = - g m_G \hat r

Thus the acceleration in this case should be

.. math::
   \vec a\propto -\hat r g \frac{m_G}{m_I}

When :math:`m_G/m_I` is constant, the falling accerelation are the same
for different objects with same mass. However, if :math:`m_G/m_I` is not
a constant, say :math:`m_G\ne m_I`, different objects would fall at
different acceleration.

Now if we put two ball with different mass on the Eotvos torsion
balance, the balance would rotate and we can measure it.

Results
^^^^^^^

Detection of
:math:`R^k_{0l0}=(1/c^2)\partial^2\Phi/\partial x^k\partial x^l \sim 10^{-32} \text{cm}^{-2}`.

Hughes-Drevershiy Experiment, etc
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Anisotropy of gravitation/electromagnetism is not proved in our galaxy.

Radio Signal
~~~~~~~~~~~~

Similar to Eddington and Dyson's bending light observation, radio
signals serve as a more precise experiment to test Einstein's theory.
And these experiments are against scalar tensor theories because scalar
tensor theories give a smaller bending angle (1.66 second of arc less
than the observations).



Summary Table
-------------

Tables constructed according to arXiv:1106.2476v3.

Test of fundamental principles

1. WEP：
   1. Eotvos torsion balance： :math:`\eta = (0.3 \pm 1.8) \times 10^{-13}`, More precise in space exp.[1a]_ [1b]_ [1c]_
   2. Gravitational redshift of light [2]_
2. EEP:
   1. Hughes-Drever Experiment: :math:`n \le 10^{-27}`, references [3a]_ [3b]_

Test of GR:


1. Null geodesics test:
   1. photon trajectory, spatial deflection:  :math:`\theta = (0.99992\pm 0.00023)\times 1.75''`, where 1.75 is the theoretical value; Achieved through observing star position, etc [4]_
   2. Shapiro time-delay effect: :math:`\Delta t = (1.00001\pm 0.00001)\Delta t_{GR}`, references [5a]_ [5b]_
2. Time like geodesics:
   1. Anomalous perihelion precession: Just use the PPN formalism [6a]_ [6b]_ [6c]_
   2. Nordtvedt effect: :math:`\eta = (-1.0 \pm 1.4) \times 10^{-*13}`, references [7a]_ [7b]_
   3. Spinning objects obiting [8a]_ [8b]_
3. Small-range:
   1. Potential probing [9a]_ [9b]_
4. Radiation
   1. Speed of gravitational waves
   2. Polarity of gravitational radiation
   3. Dynamics of source objects



Footnote
--------

.. [1a] arXiv:0712.0607

.. [1b] **Eotvos experiment**: using torsion balance to test the equality of gravitational mass and inertial mass. Wikipedia has a photo of how this works.

.. [1c] :math:`\eta=2\frac{ABS(a1-a2)}{ABS(a1+a2)}`. :math:`a1` and :math:`a2` are the accelerations of the two bodies in Eotvos torsion balance. Thus :math:`\eta` is the accleration difference of the two objects.

.. [2] To be added

.. [3a] References: **R. W. P. Drever**. A search for anisotropy of inertial mass using a free precession technique. Philosophical Magazin, 6:683-687, May 1961. ; **V. W. Hughes, H. G. Robinson, and V. Beltran-Lopez**. Upper Limit for the Anisotropy of Inertial Mass from Nuclear Resonance Experiments. Physical Review Letters, 4:342-344, Apr. 1960. ; **S. K. Lamoreaux, J. P. Jacobs, B. R. Heckel, F. J. Raab, and E. N. Fortson**. New limits on spatial anisotropy from optically-pumped 201 Hg and 199 Hg. Physical Review Letters, 57:3125–3128, Dec. 1986. ; **T. E. Chupp, R. J. Hoare, R. A. Loveman, E. R. Oteiza, J. M. Richardson, M. E. Wagshul, and A. K. Thompson**. Results of a new test of local Lorentz invariance: A search for mass anisotropy in 21 Ne. Physical Review Letters, 63:1541–1545, Oct. 1989.

.. [3b] **Hughes-Drever Experiment**: test the isotropy of mass and space through the NMR spectrum, or the mono-metric spacetime.

.. [3c] **n**: four momentum of the test particle  is $p_\mu = \frac{m g_{\mu\nu}u^\nu}{\sqrt{-g_{\alpha\beta}u^\alpha u^\beta}} + \frac{ n h_{\mu\nu}u^\nu }{ -h_{\alpha\beta} u^\alpha u^\beta }$. Thus $n$ is the effect of another metric.

.. [4] **S. S. Shapiro, J. L. Davis, D. E. Lebach, and J. S. Gregory**. Measurement of the Solar Gravitational Deflection of Radio Waves using Geodetic Very-Long-Baseline Interferometry Data, 1979 1999. Physical Review Letters, 92(12):121101, Mar. 2004.


.. [5a] References, **I. I. Shapiro**. Fourth Test of General Relativity. Physical Review Letters, 13:789–791, Dec. 1964.   ;   **B. Bertotti, L. Iess, and P. Tortora**. A test of general relativity using radio links with the Cassini spacecraft. Nature, 425:374–376, Sept. 2003.

.. [5b]  **Shapiro time-delay effect**: time delay when light travels through a massive object.

.. [6a]  Observational data for the value of perihelion precession of Mercury are summarized in **E. V. Pitjeva**. Modern Numerical Ephemerides of Planets and the Importance of Ranging Observations for Their Creation. Celestial Mechanics and Dynamical Astronomy, 80:249–271, July 2001.

.. [6b] PPN formalism is the lowest order of GR.

.. [6c] **Anomalous precession**:

.. [7a]  **K. Nordtvedt**. Equivalence Principle for Massive Bodies. I. Phenomenology. Physical Review, 169:1014–1016, May 1968.   ;  **J. G. Williams, S. G. Turyshev, and D. H. Boggs**. Progress in Lunar Laser Ranging Tests of Relativistic Gravity. Physical Review Letters, 93(26):261101, Dec. 2004, arXiv:gr-qc/0411113.

.. [7b] **Nordtvedt effect**: massive objects in Eotvos torsion balance experiments. We can use the whole Earth-Moon system to test this effect.

.. [8a] To be added

.. [8b] There is a Lense Thirring effect here. GPB has done this.

.. [9a] GR can be reduced to Newtonian potential at small range.

.. [9b] Currently, most of the modification has a Yukawa potential form.
