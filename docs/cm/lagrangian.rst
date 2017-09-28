Lagrangian and Equation of Motion
======================================================


Euler-Lagrangian equation is

.. math::
   \frac{d}{dt} \left(  \frac{\partial L}{\partial \dot{\boldsymbol q}} \right) - \frac{\partial L}{\partial \boldsymbol q} = 0.
   :label: eqn-euler-lagragian-equation

The component form is

.. math::
   \frac{d}{dt} \left(  \frac{\partial L}{\partial \dot{q_i}} \right) - \frac{\partial L}{\partial q_i} = 0.
   :label: eqn-euler-lagragian-equation-component




.. admonition:: Conserved Quantities
   :class: notes

   A quantity is conserved through time if :math:`\frac{d}{dt}Q = 0`.

   We notice that the second term in :eq:`eqn-euler-lagragian-equation-component` vanishes if the lagragian doesn't depend on :math:`q_i`. That is

   .. math::
      \frac{d}{dt} \left(  \frac{\partial L}{\partial \dot{q_i}} \right) = 0

   for Lagragian that doesn't depend on :math:`q_i`.

   We immediately spot that the quantity

   .. math::
      \frac{\partial L}{\partial \dot{q_i} }

   is a conserved quantity.
