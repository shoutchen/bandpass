The testbed for the design is comprised of Olimex ice40 devboards.
These include an FPGA board, several ADC boards, several DAC boards,
several GPIO boards, and an 32u4 arduino clone with a progrramming interface
to the FPGA.

The arduino
1.  Can program the FPGA. The sketch is also open source.
2.  Provides a HMI to control the frequency, amplitude, and phase
of the test signal to the ADC.
3.  Generates the test signal via a DAC.
4.  Produces a human readable analysis of the filter performance.

The ice40 FPGA
0.  Generates the system timing of a DAC to generate the test signal
and to control the sampling of it.
1.  Produces samples via the ADC.
2.  Generates the 100 khz reference sine, cosine, and Blackman 
filter coefficients for each ADC Sample via 3 DACS/ADC pairs.
3.  Computes the VSUM of the input signal using that signal and the 100khz reference data.
4.  Signals the arduino when the VSUM is ready.
5.  Produces the VSUM data upon demand from the arduino.

See the testbed block diagram and the devboard schematics for more information.

Here is a link to some reference material that is the basis for the filters inner workings.




 https://jackschaedler.github.io/circles-sines-signals/index.html







