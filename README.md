# Circuit-Repository

This repository aims to act as a general guide to circuit and IC selection. The project culminates in a massive 100+ page document containg circuit types, use cases, and comparisons. Most all circuits are accompanied by a schematic diagram, and implemetation guidelines.
The circuits are each headed by a overarching header grouping them by use case, in addition, there is a use case table which acts as a tldr for circuit selection. The document's content is largely assisted by anthropic's claude for the compilation and prodcution of the document. The original set of ciruits and classifications can be seen below:

1. Changing and regulating DC voltage

Linear: LDO, standard linear regulator (78xx), adjustable regulator (LM317), Zener shunt, TL431 shunt regulator, emitter-follower pass regulator, capacitance multiplier
Switching (inductive): buck, boost, inverting buck-boost, 4-switch buck-boost, SEPIC, Cuk, Zeta, flyback, forward, push-pull, half bridge, full bridge
Switching (capacitive): charge pump doubler and inverter, regulated charge pump, Dickson multiplier, Cockcroft-Walton
Low-noise rails for RF: buck followed by an LDO, ferrite bead with a pi filter, star distribution, a separate AVDD/DVDD split
References: bandgap, buried Zener, shunt vs. series references

2. Power control and protection
Load switch, high-side and low-side MOSFET switch, reverse-polarity protection (diode, P-FET, ideal-diode controller), power ORing and muxing, eFuse and hot-swap, inrush limiting, crowbar, TVS clamp, PTC fuse, supervisor/reset IC, power sequencing, soft-start

3. Batteries and energy
Linear Li-ion charger, switching charger, power-path management, fuel gauge, protection IC, supercap charging, energy harvesting (solar, RF)

4. Current sources and sinks
Resistor plus voltage reference, op-amp with FET current sink, Howland pump, BJT and MOSFET current mirrors (basic, Wilson, cascode), LM334, constant-current LED driver, JFET current source

5. Converting current to voltage (and back)

I->V: shunt resistor, TIA, charge amplifier, integrating TIA, log amplifier, current-sense amp (high-side and low-side), Hall sensor, current transformer, Rogowski coil
V->I: Howland, op-amp plus transistor, OTA, transconductance stage

6. Other signal conversions
V->F and F->V, PWM to analog (RC filter), ADCs (SAR, sigma-delta, flash, pipeline, dual-slope), DACs (R-2R, resistor string, current-steering, PWM), single-ended to differential (fully differential amp, transformer, balun), logic level shifting (divider, BSS138 bidirectional, translator ICs), op-amp offset and gain scaling

7. Detection and rectification
Half-wave and full-wave rectifiers, bridge, precision rectifier, peak detector, envelope detector, diode RF power detector, log detector (AD8318 style), RMS detector, AM/FM/phase detectors, sample-and-hold

8. Baseband amplifiers

Op-amp configurations: inverting, non-inverting, buffer, summing, difference, instrumentation amp, integrator, differentiator, PGA, composite amp, bridge amp
Discrete: common emitter/source, common base/gate, common collector/drain, cascode, differential pair, Darlington, push-pull
Power amp classes: A, B, AB, C, D

9. RF amplifiers
LNA (inductive degeneration, common gate, MMIC gain block), driver amp, PA (classes A/AB/C/E/F, Doherty), balanced amp, feedback amp, distributed amp, VGA, limiting amp. Plus biasing: bias tee, active bias, RF choke feed, GaN sequencing.

10. Filters

Response types: Butterworth, Chebyshev I and II, elliptic, Bessel, Gaussian
Passive LC: low-pass, high-pass, band-pass, band-stop (each in pi and T form)
Active: RC, Sallen-Key, multiple feedback, state variable, biquad, Twin-T notch, all-pass, gyrator
RF and microwave: stepped impedance, stub, coupled-line, hairpin, interdigital, combline, cavity, waveguide
Resonator-based: crystal, ceramic, SAW, BAW/FBAR, LTCC
Multiplexers: diplexer, duplexer, triplexer
EMI: ferrite bead, common-mode choke, feedthrough cap, pi and T EMI filters
Other: switched-capacitor, anti-alias and reconstruction filters, FIR and IIR (brief)

11. Impedance matching
L-network, pi, T, quarter-wave transformer, single and double stub, multi-section binomial and Chebyshev, tapered line, wideband transformer, baluns (LC lattice, Marchand, transformer, coax)

12. Generating frequencies

Oscillators: Pierce crystal, Colpitts, Hartley, Clapp, VCO (varactor-tuned), ring, relaxation (555), RC phase-shift, Wien bridge, TCXO/OCXO/MEMS, DRO, YIG
Synthesis: integer-N PLL, fractional-N PLL, DDS, frequency multiplier, divider/prescaler, clock buffer and fanout, jitter cleaner

13. Mixing and frequency translation
Single-diode mixer, single-balanced, double-balanced diode ring, Gilbert cell, passive FET mixer, IQ modulator and demodulator, image-reject (Hartley, Weaver), harmonic mixer, subsampling. Plus receiver architectures: superhet, direct conversion, low-IF, direct RF sampling.

14. RF routing and control
PIN and FET switches, T/R switch, fixed attenuators (pi, T), digital step attenuator, voltage-variable attenuator, phase shifters, directional coupler, branch-line hybrid, rat-race, Lange coupler, Wilkinson and resistive dividers, circulator, isolator, limiter, DC block

15. Sensing and measurement front ends
Wheatstone bridge, strain gauge amp, thermistor divider, RTD, thermocouple amp, photodiode front end, piezo/charge sensing, capacitive sensing, lock-in amplifier

16. Digital and interface glue
Pull-up and pull-down, open-drain, switch debounce (RC and Schmitt), Schmitt trigger, comparator with hysteresis, window comparator, relay driver with flyback diode, H-bridge, gate driver, optocoupler, digital isolator, ESD protection, I2C/SPI/UART/USB/CAN/RS-485 interface basics

17. Timing and pulses
555 astable and monostable, power-on reset, RC delay, edge detector, pulse stretcher, watchdog

18. Antennas and PCB RF structures
Dipole, monopole, PIFA, patch, chip antenna, helical, loop, Yagi. Microstrip, CPWG, stripline, via fencing, ground stitching.


As this project stand for more time, it will be periodically updated with LTspice simulations and similar implementations to act as a further guide to the reader. 
In addition, I will take time to parse through the application notes and/or textbook chapters that I have found particularly useful and slowly integrate them into (Useful Referances)[Useful References].