The testbed for the design is comprised of Olimex ice40 devboards.
These include an FPGA board, several ADC boards, several DAC boards,
and several GPIO boards.

The ice40 FPGA
1.  Controls the ADC to sample the signal being analyzed.
2.  Generates the reference sine, cosine, and Blackman coefficients for each ADC Sample.
3.  Computes the VSUM of the input signal using the reference data.
4.  Generates a human readable representation of the VSUM.
5.  Provides a method to substitute a sweeping signal for the ADC in order to 
determine the response of the bandpass filter.

See the testbed block diagram and the devboard schematics for more information.

Here is a link to some reference material regarding the inner workings of the filter.




