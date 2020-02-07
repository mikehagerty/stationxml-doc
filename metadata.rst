.. Put any comments here
   Be sure to indent at this level to keep it in comment.

What is Metadata
===========================================


What Is Metadata And Why Do We Need It ?
-----------------------------------------

In the most general sense, metadata is simply 'data' (=information)
that describes other data.
For instance, when we take a digital photograph, 
the resulting image is stored in a file, along with information
that describes it (including the date it was taken, the camera
settings, etc).

In this sense, metadata describes how the underlying data was
collected, processed, etc.


How is metadata used in geophysics ?
-----------------------------------------

When we install a scientific instrument (a sensor), we are generally interested in recording
some physical quantity (with corresponding input units) associated with environmental changes.
Different geophysical sensors are used to measure different aspects of ground motion.
For instance, a GPS receiver is used to measure changes in 
ground position (input units = m),
a broadband seismometer is used to measure changes in ground velocity
(input units = m/s), 
a strong-motion accelerometer is used to measure changes
in ground acceleration (input units = :math:`m/s^2`) and an extensometer is
used to measure changes in strain (input units = m/m) or strain-rate (input units = 1/s).

Similarly, we may wish to measure changes in atmospheric temperature
using a temperature probe (input units = :math:`°C`),
and changes in atmospheric pressure using a pressure transducer
(input units = Pa).

The physical quantity (m, m/s, Pa, etc) is what we are interested in.
However, the sensor and datalogger system used to measure and record it 
imparts its own signature
to the recorded data.  It is this signature, or instrument response, that we must remove
from the recorded data in order to recover the underlying physical quantity
that was measured.
The metadata associated with a data record must provide enough information
about the recording system so that its effects can be modeled accurately
and therefore removed from the recorded signals.

Stationxml provides a general and highly flexible way to express and store
the metadata information needed to fully describe the instrumentation used
to measure and record the signal.


