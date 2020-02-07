.. Put any comments here
   Be sure to indent at this level to keep it in comment.


Theory of Instrument Response
===========================================


.. image:: ./stage_sequence.png

A seismic recording system can be considered a sequence of stages.


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

Any one of these is a complete description of the system; which one
we choose to work with usually depends on our purpose.
For instance, for edge detection, a common task of image processing,
we care most about the shape of the step response,
whereas
in digital filtering, the complex frequency response is often
most important.

For analog sensors (e.g., seismic sensors) that measure in continuous time, we 
generally describe the effect of the sensor stage using the poles and zeros of 
the Laplace transform of the stage transfer function, :math:`H(s)`,
while for purely digital stages (e.g., anti-alias FIR filters), we use 
either the poles and zeros of the z-transform of the transfer function, :math:`H(z)`,
or the corresponding polynomial coefficients.

Fortunately, if we know any one of these we can derive the others.
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

