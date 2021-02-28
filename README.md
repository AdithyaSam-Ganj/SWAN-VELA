# SWAN-VELA
Vela  Pulsar timing from data provided by SWAN (Sky Watch Array Network - RRI)
This is the Pulsar Timing and d-Dispersion analysis of Vela Pulsar. I data file can be obtained if people are taking part in the SWAN imaging challenge conducted by RRI every year. 

==========================================Data File Format===============================================
- ascii files
- one second worth of data of vela pulsar 
- 2 columns of data representing N and S array seperately 
- Nyquist sampled data 16.5 MHz bandwidth centered at 326.5MHz
- interval between each row is (1/33) microseconds

==================================================Anaylsis ===================================================================================================


- taking 512 points (from a chosen column) at a time, Fourier transforming them,
- taking one half of the spectrum (corresponding to the +ve frequencies) and
- computing modulus-square for each of the 256 spectral channels to obtain power (spectrum) as a function of channel number (1 to 256).Each such power spectrum corresponds a time interval of (or as averaged over) (512/33) microseconds.

- Such power spectra may be averaged together in sets of M, based on the desired time resolution ... given by (M*512/33) microseconds.  (say, M=60, corresponding to 1 msec resolution)

- The 256-point power spectra thus averaged may be stacked one after another to form a 2-d matrix of intensities, as a function of frequency and time.T

- Similar analysis can be done for the data in other column. To observe correlated signal between the two halves of the telescope, you may first compute the Fourier transform of each set of 512 points taken separately from the two columns and multiply (channel-wise) the spectrum of N by the complex conjugate of spectrum of S. And then follow steps 4 onward, for this cross-power-spectrum.

- Once you have such 2-d data (dynamic spectrum), one can fold it at the pulsar period, and also dedisperse it to obtain average profile. One also estimate the pulsar period and dispersion measure separately. You may also estimate the amount of broadening of the pulse due to interstellar scattering.  
====================================================Results =====================================================================================================
I do not think I have the liberty to put the data files here. I will be uplaoding the end result of pulsar after dedispersion and before that in the form of a picture. 
