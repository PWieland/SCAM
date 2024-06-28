# SCAM
Stereo Composite Amplifier Module 

This is my take of the popular VFA-CFA composite amplifier using 2*TPA6120A2/THS6012 and a dual OpAmp like OPA1612.
Many of the most high performance headphone amplifiers on the market use this exact combination and topology.
The name is supposed to poke fun at some of the corny names people give to their projects on audio forums, nothing more.

My version features extensive options for loop compensation, including the common 2-Pole-Compensation, Noise-Gain-Shaping and an extra Lead-Lag-Compensator in the forward path.
It can be compensated to be a headphone amplifier but will also do exceptionally well in any test and measurement application where heavy loads have to be driven with low noise and distortion.

An effort was made to design a PCB that is compact (50x50mm) and visually pleasing without making any compromises regarding pure performance. I let you be the judge of the result.
The cutouts on the bottom layer are strategically placed to avoid load currents from disturbing sensitive nodes and to minimise parasitic capacitances on the inverting input of the CFAs.
![IMG_0499](https://github.com/PWieland/SCAM/assets/65927363/e0684f82-0ebd-4883-a797-c145dff60224)


## Performance

An un-optimised version driving 2Vrms at 1kHz into 50Ω. Signal source is Victor's low distortion oscillator: https://viccc42.wixsite.com/uld-audio
![VO1kHz_buffered_50OhmLoad_2Vrms_Cosmos192kStereoR](https://github.com/PWieland/SCAM/assets/65927363/d08946e6-f100-46e1-b124-ea06afb240d9)

