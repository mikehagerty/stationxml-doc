
.. Put any comments here
   Be sure to indent at this level to keep it in comment.

The Fourier Transform (:math:`t \rightarrow \omega`) is defined by

.. math::

   X(\omega)=\frac{1}{2\pi}\int_{-\infty}^{\infty}x(t)e^{-j\omega t}dt

while the Inverse Fourier Transform (:math:`\omega \rightarrow t`)  is given by

.. math::

   x(t)=\int_{-\infty}^{\infty}X(\omega)e^{+j\omega t}d\omega

Note that the choice of which transform (forward vs. reverse) has which
sign of the complex exponent and 
which gets the 
:math:`\frac{1}{2\pi}` scalefactor is optional.

For instance, some authors prefer to scale each transform by
:math:`\frac{1}{\sqrt(2\pi)}`.

What is important is that the signs of the exponents in each transform
must be opposite, and the product of their scalefactors must equal
:math:`\frac{1}{2\pi}`.


Poles and Zeros
^^^^^^^^^^^^^^^^^^^^^

