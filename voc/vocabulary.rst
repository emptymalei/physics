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


Legendre Transformation
==========================


Legendre transformation is NOT just some algebra. Given :math:`f(x)` as a function of :math:`x`, which is shown in blue, we could find the distance between a line :math:`y=px_i` and the function value :math:`f(x_i)`.

.. figure:: assets/legendreTransformation.png
   :align: center

   Meaning of Legendre transformation


However, as we didn't fix :math:`x`, this means that the distance

.. math::
   F(p,x) = p x - f(x) 

varies according to :math:`x`. This is a transformation that maps a function :math:`f(x)` to some other function :math:`F(p,x)` which depends on the parameter :math:`p`.

To have a Legendre transformation, let's choose a relation between :math:`x` and :math:`p`. One choice is to make sure we have a maximum distance given :math:`p`, which means the :math:`x` we choose is the point that makes the slope of :math:`f(x)` the same as the line :math:`y=px`. In the language of math, the condition we require is

.. math::
   0 = \frac{\partial F(p,x)}{\partial x} \equiv f'(x) - p,

which indeed shows that the slope of function and slope of the straight line match eath other at the specified point. Thus we have a relation between :math:`x` and :math:`p`.

Substitute :math:`x(p)` back into :math:`F(p,x)`, we will get the Legendre transformation :math:`F(p,x(p))` of :math:`f(x)`.











Vector Analysis
==========================


The ultimate trick is to use component form.

.. math::
   &\vec a \times (\vec b \times \vec c)
   = & \hat e_i \epsilon_{ijk} a_j (\epsilon_{kmn} b_m c_n ) \\
   = & \hat e_i \epsilon_{kij}\epsilon_{kmn} a_j b_m c_n \\
   = & \hat e_i ( \delta_{im}\delta_{jn} - \delta_{in}\delta_{jm} )a_j b_m c_n \\
   = & \hat e_i \delta_{im}\delta_{jn} a_j b_m c_n -  \hat e_i \delta_{in}\delta_{jm} a_j b_m c_n \\
   = & \hat e_i a_j b_i c_j - \hat e_i a_j b_j c_i \\
   = & \vec b (\vec a\cdot \vec c) - \vec c (\vec a \cdot \vec b) .

One should be able to find the component forms of gradient :math:`\vec \nabla \cdot`, divergence :math:`\vec \nabla \times`, Laplace operator, in **spherical coordinates, cylindrical coordinates and cartisian coordinates**.



   





Refs & Notes
==================


