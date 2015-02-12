Vocabulary
*****************

Functional Derivative
==============================

By definition, [#physmath]_ functional derivative of a functional :math:`G[f]` with respect to :math:`f` along the 'direction' of :math:`h` is

.. math::
   \delta G[f][h] = \frac{d}{d\epsilon} G[f+\epsilon h]\vert_{\epsilon=0}.

As an example, the functional derivative of :math:`G[f]=\int dx f^n(x)` :math:`\delta G[f][h]` is

.. math::
   \delta G[f][h] &= \frac{d}{d\epsilon} G[f+\epsilon h] \vert_{\epsilon=0} \\
   & = \int nf^{n-1}(x) h(x) dx.

Now the problem appears. We have an unknown function :math:`h` which makes sense because we haven't specify a direction of the derivative yet.

For a physicist, the savior of integral is Dirac delta. So we use delta distribution as the direction in the functional derivative of action which is an integral,

.. math::
   \frac{\delta G[f]}{\delta f(y)} = \delta G[f][\delta_y].

It can be ambiguous to just write down :math:`\delta_y` without an example. Here is the previous example continued,

.. math::
   \frac{\delta G[f(y)]}{\delta f(y)} &= \int nf^{n-1}(x) h(x) dx \vert_{h(x)= \delta(x-y)} \\
   & = \int nf^{n-1}(x) \delta(x-y) dx \\
   & = n f^{n-1}(y) .

It seems that we can just think of :math:`f` as a variable then take the ordinary derivative with respect to it. It is NOT true.

Consider such a functional :math:`G[f]=\int (f'(x))^2 dx` where ' means the derivative of :math:`f(x)`.

.. math::
   \frac{\delta G[f]}{\delta f} & = -\int dx 2 f''(x) h(x) \vert_{h(x)=\delta(x-y)}  \\
   & = -2 f''(y) ,

which is not that straightforward to understand from function derivatives.






.. [#physmath] Chapter 15 of `Physical Mathematics <http://www.amazon.com/Physical-Mathematics-Kevin-Cahill/dp/1107005213>`_









Refs & Notes
==================


