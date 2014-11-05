Special Functions
===================


There are a lot of useful special function in physics. Some of them provides physics understanding of the problem, some of them helps us writing down a solution quickly.

Among them, Gamma functions, Legendre polynomials, Bessel functions, spherical harmonics, modified bessel functions, spherical bessel functions, and elliptical functions are the most used ones.


Gamma Functions
------------------------

Gamma function satisfies the following relatioin,

.. math::
   \Gamma(z+1) = z\Gamma(z) .

For some cases, it can also be written as 

.. math::
   \Gamma(n) = \int_0^\infty dt t^{n-1} e^{-t} .

One can prove that

.. math::
   \Gamma(z)\Gamma(1-z) = \frac{\pi}{\sin(\pi z)} .




Legendre Polynomials
-------------------------


Legendre polynomials are solutions to Legendre equation, which is

.. math::
   \left(\frac{d}{dx}\left[(1-x^2)\frac{d}{dx}\right] + n(n+1)\right) P_n(x) = 0.



Legendre polynomials has many different representations.

**Integral**

.. math::
   P_n(z) = \frac{1}{2\pi i} \oint (1 - 2 t z + t^2)^{1/2} t^{-n-1} dt.

**Rodrigues representation**

.. math::
   P_n(z) = \frac{1}{2^l l!} \frac{d^l}{d x^l} (x^2 - 1)^l .


It's generation function is

.. math::
   \frac{1}{\sqrt{1 + \eta^2 - 2 \eta x }} = \sum_{k=0}^\infty \eta^k P_k(x) .


.. admonition:: Properties
   :class: note

    **Orthogonality**

    .. math::
       \int_{-1}^1 P_m(x) P_n(x) dx =  \frac{2}{2n + 1}\delta_{mn} .

    They all have value 1 at :math:`z=1`. 

    The parity is alternating.

    **Examples**

    .. math::
       P_0(x) & = 1 \\
       P_1(x) & = x \\
       P_2(x) & = \frac{1}{2}(3x^2-1).

    Through these, we can solve out 

    .. math::
       x &= P_1(x) \\
       x^2 &= \frac{1}{3}(P_0(x) + 2 P_2(x) ).

    Notice that they have physics meanings although it's better to understand it together with spherical harmonics.




Associated Legendre Polynomials
-----------------------------------


The associated Legendre equation is

.. math::
   \left(\frac{d}{dx}\left[(1-x^2)\frac{d}{dx}\right] + n(n+1) - \frac{m^2}{1-x^2} \right) P_n(x) = 0.

The solution to this equation is Associated Legendre polynomial, which can be represented by 

.. math::
   P_n^{\nu}(x) = (-1)^m(1-x^2)^{m/2} \frac{d^m}{dx^m} P_l(x) .








Bessel Functions
--------------------


Bessel functions are solutions to Bessel equation,


.. math::
   \left( x \frac{d}{dx} x \frac{d}{dx} + x^2 - \nu^2 \right) J_{\nu} (x) = 0.

They all satisfy these recurrence relations,

.. math::
   Z_{n+1} + Z_{n-1} &= \frac{2n}{x} Z_n  \\
   Z_{n-1} - Z_{n+1} & = 2 \frac{d}{dx}Z_n .



Bessel Function of the first kind
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Use notation :math:`J_n(x)` for the first kind.

**Generating function** is

.. math::
   e^{\frac{z}{2}\left(t-\frac{1}{t}\right)} = \sum_{n=-\infty}{infty} t^n J_n(z) .

**Integral representation**

.. math::
   J_n(z) = \frac{1}{2\pi} \int_{-\pi}^{\pi} e^{i(n\tau - x \sin \tau)} d\tau .

It also has a **summation representation**,

.. math::
   J_\alpha(z) = \sum_{m=0}^\infty \frac{(-1)^m}{m!\Gamma(m+\alpha +1)}  \left( \frac{x}{2} \right)^{2m+\alpha} .



At large :math:`\vert x \vert` limits, we have

.. math::
   \lim_{\vert x\vert \to \infty} J_l(x) &= \frac{\sin(z-l\frac{\pi}{2})}{x} \\
   \lim_{\vert x\vert \to \infty} J_l'(x) &= \frac{\cos(z-l\frac{\pi}{2})}{x} .


By playing with the recurrence relation,

.. math::
   2J_n' &= J_{n-1} - J_{n+1} \\
   2n J_n & = J_{n+1} + J_{n-1},

we can get two more useful relations,

.. math::
   \frac{d}{dz} (z^n J_n) & = z^n J_{n-1} \\
   \frac{d}{dz} (z^{-n} J_{n}) & = - z^{-n} J_{n+1} .

They are very useful when integrating by part.










Graphics and Properties
~~~~~~~~~~~~~~~~~~~~~~~~

.. figure:: math/assets/BesselZeros.png
   :align: center

   The first 10 zeros of Bessel functions from order 0 to 4.




.. figure:: math/assets/sphericalBesselZeros.png
   :align: center

   The first 10 zeros of spherical Bessel functions from order 0 to 4.



.. figure:: math/assets/besselZerosListPlt.png
   :align: center

   Bessel function zeros in a list plot. Horizontal axis is nth zero point, while vertical axis is the value.


.. figure:: math/assets/sphbesselZerosListPlt.png
   :align: center

    Spherical Bessel function zeros.


.. figure:: math/assets/besselZerosDifferencePlt.png
   :align: center

    The difference between zeros of Bessel functions. They are almost the same, which a around Pi.



.. figure:: math/assets/sphbesselZerosDifferencePlt.png
   :align: center

   Spherical Bessel function zeros differences.








Refs & Notes
-------------
