
.. Put any comments here
   Be sure to indent at this level to keep it in comment.

The Laplace Transform is defined by

.. math::

   X(\sigma,\omega)=\int_{-\infty}^{\infty}x(t)e^{-\sigma t}e^{-j\omega t}dt

If we make the substitution, :math:`s=\sigma + j\omega`, this becomes

.. math::

   X(s)=\int_{-\infty}^{\infty}x(t)e^{-s t}dt

Each point in the complex s-plane is associated with a frequency, :math:`\omega`  and
an exponent :math:`\sigma`.
Thus, each point in the s-plane describes a sinusoid of frequency :math:`\omega`  that is either 
exponentially growing (:math:`\sigma>0`) or exponentially decaying (:math:`\sigma<0`) with time.

Note that the laplace transform evaluated along the imaginary axis (where the attenuation parameter,
:math:`s=0`), reduces to the complex Fourier transform, :math:`X(\omega)`.

The laplace transform at point :math:`s`  is a measure of the
similarlity between the input signal, :math:`x(t)`, and the corresponding
exponentially growing/decaying sinusoid corresponding to that value of :math:`s`.
A large value of :math:`X(s)`  corresponds to a strong similarity between the 
input signal and the sinusoid :math:`e^{-(\sigma + j\omega)t}`, indicating a
strong presence of the sinusoid in the input signal.

Poles and Zeros
^^^^^^^^^^^^^^^^^^^^^

