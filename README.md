# SCAM
Stereo Composite Amplifier Module 

This is my take of the popular VFA-CFA composite amplifier using 2*TPA6120/THS6012 and a dual OpAmp like OPA1612.
Many of the most high performance headphone amplifiers on the market use this exact combination and topology.
The name is supposed to poke fun at some of the corny names people give to their projects on audio forums, nothing more.

My version features extensive options for loop compensation, including the common 2-Pole-Compensation, Noise-Gain-Shaping and an extra Lead-Lag-Compensator in the forward path.
It can be compensated to be a headphone amplifier but will also do exceptionally well in many test and measurement applications where heavy loads have to be driven with low noise and distortion.

## Schematic

A conceptual schematic without any power supply components but showing the different options for compensation:
<img width="956" alt="image" src="https://github.com/PWieland/SCAM/assets/65927363/9b25dd3d-7e08-4c55-889e-c6a8c37ea628">

For more information regarding this arrangement consider reading some of Dr. Sergio Franco's articles on the web.
VFA-CFA composite amplifiers also sometimes show up in app-notes and datasheets (e.g. AD797, ADA4870,...).
Optimising the performance of this arrangement is mainly an exercise in applied control theory and patience.
Don't put too much trust in simulations, as OpAmp models are notoriously imperfect and approximations of parasitics only ever so accurate.
Verifying stability of these arrangements presents it's own challenges due to the 100s of MHz of bandwidth of the TPA6120/THS6012.
An oscilloscope with bandwidth in excess of 300MHz is recommended to look at some square wave or square-wave modulated sine wave responses into capacitive loads.


## PCB

An effort was made to design a PCB that is compact (50x50mm) and visually pleasing without making any compromises regarding pure performance. I let you be the judge of the result.
The cutouts on the bottom layer are strategically placed to avoid load currents from disturbing sensitive nodes and to minimise parasitic capacitances on the inverting input of the CFAs.
![IMG_0499](https://github.com/PWieland/SCAM/assets/65927363/e0684f82-0ebd-4883-a797-c145dff60224)

After SMD assembly and ultrasonic cleaning and before mounting of the TH-components (tall TH-capacitors would block the view.
Obviously with so many compensation options, some footprints will usually remain empty. This picture shows an implementation of 2-Pole-Compensation.
![IMG_0553](https://github.com/PWieland/SCAM/assets/65927363/4f7e634b-d011-4822-a6bf-9ff3e0a2fa77)



## Performance

An un-optimised version driving 2Vrms at 1kHz into 50Ω. Signal source is Victor's low distortion oscillator: https://viccc42.wixsite.com/uld-audio
![VO1kHz_buffered_50OhmLoad_2Vrms_Cosmos192kStereoR](https://github.com/PWieland/SCAM/assets/65927363/d08946e6-f100-46e1-b124-ea06afb240d9)

