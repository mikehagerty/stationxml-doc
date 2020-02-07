.. Put any comments here
   Be sure to indent at this level to keep it in comment.


Theory of Instrument Response
===========================================


Introduction
-----------------------------------------

The theory of instrument response is contained in the theory of
linear, time invariant systems, used to describe differential equations
where the coefficients are constant and hence do not change with time.

Linear Time Invariant (LTI) Systems
-----------------------------------------

Linear and time invariant systems can be fully described
in several ways, all equally valid:

#. By the linear differential equation that describes the system
#. By the system impulse response
#. By the system step response
#. By the Laplace transfer function
#. By the complex (Fourier) frequency response

Any one of these is a complete description of the system.
If we know any one of these we can derive the others.
For instance, the system step response is found by integrating
the impulse response with respect to time.
Similarly, the Fourier response can be found by evaluating
the Laplace transfer function along the imaginary axis as described
below.


The Fourier Transform
-----------------------------------------

.. include:: transform-fourier.rst


The Laplace Transform
-----------------------------------------

.. include:: transform-laplace.rst


The z-Transform
-----------------------------------------

.. include:: transform-z.rst

