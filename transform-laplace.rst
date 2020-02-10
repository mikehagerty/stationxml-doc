
.. Put any comments here
   Be sure to indent at this level to keep it in comment.

Introduction
'''''''''''''''''''''''

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

In practice, we are often only interested in causal signals that begin at :math:`t=0`.
Using the unit step function, 

.. math::

   \begin{equation*}
       u(t)=\begin{cases}
         1 & t\ge0\\
         0 & t<0
         \end{cases}
   \end{equation*}

we may ensure causality by writing :math:`x(t)=u(t)x(t)` , so that the Laplace Transform becomes

.. math::

   X(s)=\int_{0}^{\infty}x(t)e^{-s t}dt


Poles and Zeros
'''''''''''''''''''''''


Suppose we have a data processing system (e.g., analog sensor + datalogger) that can be characterized
by the linear differential equation,

.. math::

   c_{2}\ddot{f}(t)+c_{1}\dot{f}(t)+c_{0}f(t)=d_{2}\ddot{g}(t)+d_{1}\dot{g}(t)+d_{0}g(t)

where :math:`f(t)` is the input signal (e.g., the ground motion), :math:`g(t)` is the output signal (the signal recorded)
and the :math:`c_{k}` and :math:`d_{k}`  are constant (time-invariant) coefficients.
If we assume the system is causal, so that the signals + derivatives are all 0 for :math:`t<0` ,
then the Laplace Transform of the equation gives

.. math::

   c_{2}s^{2}F(s)+c_{1}sF(s)+c_{0}F(s)=d_{2}s^{2}G(s)+d_{1}sG(s)+d_{0}G(s)

or

.. math::

   (c_{2}s^{2}+c_{1}s+c_{0})F(s)=(d_{2}s^{2}+d_{1}s+d_{0})G(s)

from which we can write the transfer function of the system as

.. math::

   H(s) = \frac{G(s)}{F(s)}=\frac{c_{2}s^{2}+c_{1}s+c_{0}}{d_{2}s^{2}+d_{1}s+d_{0}}


which can be written as a ratio of polynomials as

.. math::

   H(s) =\frac{\sum_{n=0}^{N}c_n s^n}{\sum_{m=0}^{M}d_n s^n}

This is the coefficient representation of the transfer function.

Often, for analog stages, it is more convenient to factor the numerator
and denominator polynomials of the transfer function 
into the polezero representation,

.. math::

   H(s)=\frac{\Pi_{k=1}^{M} (s-z_{k})} {\Pi_{k=1}^{N} (s-p_{k})}

where :math:`z_{k}` are the M zeros of the system, and :math:`p_{k}` are the N poles.


