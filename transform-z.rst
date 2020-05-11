
.. Put any comments here
   Be sure to indent at this level to keep it in comment.

The z-Transform is defined by

.. math::

   X(z)=\sum_{n=0}^{\infty}x[n]z^{-n}

where

.. math::

   z=re^{j\omega}

   z^{-n}=r^{-n}e^{-j\omega n}

Notice that on the unit circle, where :math:`|z|\equiv |r|=1` and :math:`z=e^{j\omega}` , the z-transform reduces to the discrete Fourier transform (DTFT):

.. math::

   X(e^{j\omega})=\sum_{n=0}^{\infty}x[n]e^{-j\omega n}



z-transforms of linear time-invariant (LTI) systems described by difference equations play an important role in signal processing

The General form of a difference equation is:.

.. math::

   \sum_{k=0}^{N}a_{k}y[n-k]=\sum_{k=0}^{M}b_{k}x[n-k],

where :math:`a_{0}\ne0` (e.g., the coefficient of y[n] can't be zero)


Taking the z-transform of both sides,

.. math::

   \sum_{k=0}^{N}a_{k}z^{-k}Y(z)]=\sum_{k=0}^{M}b_{k}z^{-k}X(z)

or

.. math::

   Y(z)=\frac{\sum_{k=0}^{M}b_{k}z^{-k}}{\sum_{k=0}^{N}a_{k}z^{-k}}X(z)


From this we can write the (system) transfer function 

.. math::

   H(z)=\frac{Y(z)}{X(z)}=\frac{\sum_{k=0}^{M}b_{k}z^{-k}}{\sum_{k=0}^{N}a_{k}z^{-k}}

The transfer function is the z-transform of the system impulse response, h[n], or

.. math::

   H(z)=\sum_{n=0}^{\infty}h[n]z^{-n}

The transfer function can also be factored in terms of poles and zeros (for :math:`b_{0}\ne0`)

.. math::

   H(z)=\frac{b_{0}}{a_{0}}\frac{\Pi_{k=1}^{M}(1-c_{k}z^{-1})}{\Pi_{k=1}^{N}(1-d_{k}z^{-1})}

where :math:`c_{k}` are the M zeros of the system, and :math:`d_{k}` are the N poles.

For a system to be both stable and causal, its poles must lie inside the unit circle, or 
:math:`|d_{k}|<1 k=1,N`
