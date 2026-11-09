# Circuit-Repository

This repository aims to act as a general guide to circuit and IC selection. The project culminates in a massive 100+ page document containg circuit types, use cases, and comparisons. Most all circuits are accompanied by a schematic diagram, and implemetation guidelines.
The circuits are each headed by a overarching header grouping them by use case. The document's content is largely assisted by anthropic's claude for the compilation and prodcution of the document. The full encompasing list includes the following, broken up by category:


1. Getting Power onto the Board
DC barrel jack
USB-C, 5 V only (CC pull-down resistors)
USB-C Power Delivery sink (PD trigger IC)
Micro-USB / USB-B / Mini-USB
Screw terminals, terminal blocks, and pluggable blocks
Banana jacks and binding posts
JST and pin headers (internal power)
Batteries (cells and holders)
Power over Ethernet (PoE powered device)
Bias tee (DC power over coax)
Automotive 12 V and wide-input rails
2. Changing and Regulating DC Voltage
Linear regulators

LDO (low-dropout linear regulator)
Standard linear regulator (78xx / LM1117 class)
Adjustable linear regulator (LM317)
Zener shunt regulator
TL431 programmable shunt regulator
Emitter-follower pass regulator
Capacitance multiplier (ripple filter)
Inductive switching converters

Buck (step-down) converter
Boost (step-up) converter
Inverting buck-boost
Four-switch (non-inverting) buck-boost
SEPIC and Zeta
Cuk converter
Flyback (isolated)
Forward, push-pull, half-bridge, and full-bridge (isolated, higher power)
Capacitive (inductorless) converters

Charge pump: inverter and doubler
Regulated charge pumps and switched-capacitor converters
Dickson multiplier and Cockcroft-Walton ladder
Low-noise power for RF and precision circuits

Buck followed by an LDO (post-regulation)
Ferrite bead and pi filter on a supply
Voltage references (series and shunt)
Power modules (integrated inductor)
3. Switching, Protecting, and Sequencing Power
Switching loads on and off

Low-side N-MOSFET switch
High-side P-MOSFET switch (with level shifter)
Load switch IC
Reverse polarity and source selection

Series diode reverse-polarity protection
P-MOSFET reverse-polarity protection
Ideal diode controller
Power ORing and power multiplexers
Overcurrent, surge, and overvoltage

Fuses and PTC resettable fuses
eFuse and hot-swap controller
TVS diode (transient voltage suppressor)
Surge stopper and overvoltage protection switch
Crowbar circuit
Inrush current limiting
Supervision and sequencing

Voltage supervisor / reset IC
Power sequencing
4. Batteries and Energy Storage
Linear Li-ion charger (CC/CV)
Switching charger and power-path management
Battery protection IC
Fuel gauge
Cell balancing and battery management (BMS)
Supercapacitor backup
Energy harvesting
5. Current Sources and Sinks
BJT and MOSFET current mirrors
JFET and depletion-mode MOSFET current source
IC current sources: LM334, LT3092, LM317
Constant-current LED drivers
Electronic load
Laser diode driver
6. Converting Signals
Current to voltage

Shunt resistor
Current-sense amplifier (high-side and low-side)
Transimpedance amplifier (TIA)
Charge amplifier
Integrating TIA
Logarithmic amplifier
Hall-effect current sensor
Current transformer and Rogowski coil
Voltage to current

Op-amp with MOSFET current sink
Howland current pump
OTA (operational transconductance amplifier)
4-20 mA current loop
Analog to digital and back

ADC architectures
DAC architectures
Voltage-to-frequency and frequency-to-voltage
Interfaces between domains

Single-ended to differential
Logic level shifting
Scaling a signal into an ADC range
Isolation amplifiers and isolated ADCs
7. Detection and Rectification
Rectifiers

Half-wave, full-wave, and bridge rectifiers
Precision rectifier (superdiode)
Peak detector
RF and envelope detectors

Diode envelope (AM) detector
Schottky diode RF power detector
Logarithmic detector (successive detection)
RMS power detector
Thermal power sensor
Frequency and phase detectors

FM detectors: discriminator, quadrature detector, PLL
Phase detectors: mixer, XOR, phase-frequency detector
Sampling and timing detectors

Sample-and-hold / track-and-hold
Zero-crossing detector
8. Op-Amp Circuits
Inverting amplifier
Non-inverting amplifier
Voltage follower (buffer)
Summing amplifier
Difference amplifier
Instrumentation amplifier
Integrator
Differentiator
Comparator with hysteresis (Schmitt trigger)
Rail splitter (virtual ground)
Driving capacitive loads (isolation resistor)
Fully differential amplifier
Choosing an op-amp
9. Discrete and Power Amplifiers
Common-emitter (common-source) amplifier
Common-base (common-gate) amplifier
Common-collector (emitter follower) and source follower
Cascode
Differential pair
Darlington and Sziklai pairs
Push-pull output stage
Biasing schemes
Amplifier classes (A, B, AB, C, D)
10. RF Amplifiers
Specs that describe any RF amplifier
Receive-side amplifiers

LNA with inductive source degeneration
Common-gate (common-base) LNA
MMIC gain block
Resistive feedback amplifier
Balanced amplifier
Distributed (traveling-wave) amplifier
Variable-gain amplifier and AGC
Limiting amplifier
Transmit-side amplifiers

Power amplifier classes
Driver amplifier
Doherty amplifier
Biasing, stability, and linearization

RF biasing: choke feed and active bias
Stability and stabilizing networks
Linearization: backoff, predistortion, feedforward, envelope tracking
11. Filters
Response types

Butterworth, Chebyshev, elliptic, Bessel, and Gaussian
Passive RC and simple filters

RC low-pass
RC high-pass (AC coupling)
RC band-pass (high-pass then low-pass)
Passive LC filters

LC low-pass (pi and T ladders)
LC high-pass
LC band-pass (coupled resonators)
LC band-stop (notch and trap)
Active filters (op-amp)

Sallen-Key (low-pass and high-pass)
Multiple feedback (MFB)
State-variable and biquad filters
Twin-T notch
All-pass (phase-shift) filter
Gyrator (simulated inductor)
Transmission-line and microwave filters

Stepped-impedance low-pass
Stub filters (Richards' transformation and Kuroda identities)
Coupled-line, hairpin, interdigital, and combline band-pass
Cavity and waveguide filters
Acoustic and crystal resonator filters

Crystal and ceramic filters
SAW (surface acoustic wave) filters
BAW and FBAR filters
Multiplexers

Diplexer, duplexer, and triplexer
EMI and supply filters

Ferrite beads
Common-mode choke
Feedthrough capacitors and filtered connectors
Sampled and digital filters

Switched-capacitor filters
Anti-alias and reconstruction filters
Digital filters: FIR, IIR, CIC
12. Impedance Matching
What are you matching for?
Lumped-element networks

L-network
Pi and T networks
Transmission-line matching

Quarter-wave transformer
Multi-section (binomial, Chebyshev) and tapered lines
Single-stub and double-stub matching
Transformers and baluns

Wideband transformers
Baluns (LC lattice, Marchand, transformer, coaxial)
Other methods and tools

Resistive (minimum-loss) pad
Smith chart workflow and tools
13. Generating Frequencies
Phase noise and jitter (what makes a frequency source good)
Oscillators

Pierce crystal oscillator
LC oscillators: Colpitts, Hartley, and Clapp
Packaged reference oscillators: XO, VCXO, TCXO, OCXO, MEMS
Voltage-controlled oscillator (VCO)
Ring oscillator
RC oscillators: phase-shift, Wien bridge, relaxation
Dielectric resonator and YIG oscillators
Synthesis and distribution

Integer-N phase-locked loop (PLL)
Fractional-N PLL
Direct digital synthesis (DDS)
Frequency multipliers
Dividers and prescalers
Clock buffers, fanout, and jitter cleaners
14. Mixing and Frequency Translation
Mixer specs
Mixer circuits

Single-diode mixer
Single-balanced mixer
Double-balanced diode-ring mixer
Gilbert cell (active double-balanced mixer)
Passive FET (switching) mixer
IQ (quadrature) demodulator and modulator
Image-reject mixers (Hartley and Weaver)
Harmonic and subharmonic mixers
Subsampling (bandpass sampling)
Receiver architectures

Superheterodyne receiver
Direct-conversion (zero-IF) receiver
Low-IF receiver
Direct RF sampling
Transmitter architectures
15. RF Routing and Control
Switches

PIN diode switch
FET / SOI switch ICs (SPDT, SP4T, SPnT)
Transmit/receive (T/R) switch
Attenuators

Fixed attenuators (pi and T pads)
Digital step attenuator (DSA)
Voltage-variable attenuator (VVA)
Splitting, combining, and coupling

Wilkinson power divider
Resistive power divider
Directional coupler
Branch-line
Rat-race
Lange coupler
Non-reciprocal and protection devices

Circulator and isolator
RF limiter
DC blocks and RF terminations
16. Sensing and Measurement Front Ends
Wheatstone bridge
Thermistor divider
RTD (2-, 3-, and 4-wire)
Thermocouple amplifier with cold-junction compensation
Capacitive sensing
Kelvin (4-wire) resistance measurement
Lock-in amplifier
Chopper and auto-zero (zero-drift) amplifiers
17. Signal Integrity and Board-Level Practice
Biasing digital lines

Pull-up and pull-down resistors
Power integrity

Decoupling (bypass) capacitors
Bulk capacitance
Protection at the connectors

ESD protection
Transmission lines and termination

Controlled-impedance traces
Series (source) termination
Parallel, Thevenin, and AC termination
Differential pairs
Length matching and skew
Grounding and layout

Ground planes and return paths
Split ground planes (vs. one unified plane)
Via stitching and via fencing
Crosstalk and spacing (3W rule)
Guard rings and guard traces
Kelvin (4-wire) connections
Shielding cans
Clock routing and spread spectrum
Test points and probing
18. Digital and Interface Glue
Open-drain outputs and wired-AND
Switch debouncing
Schmitt trigger
Window comparator
Relay and inductive load driver
H-bridge
Gate drivers
Optocouplers and digital isolators
Serial bus physical layers
GPIO expanders and shift registers
LED drive
19. Timing and Pulses
555 timer (astable and monostable)
Power-on reset
RC delay
Edge detector and pulse stretcher
Watchdog timer
Real-time clock (RTC)
20. Antennas and PCB RF Structures
Antenna specs and the link budget
Wire and external antennas

Dipole
Monopole and whip (quarter-wave over ground)
Helical antennas (normal mode and axial mode)
Yagi-Uda and log-periodic
PCB and compact antennas

Inverted-F (IFA) and PIFA
Chip antenna
Patch (microstrip) antenna
Loop antennas
Antenna matching and keep-out rules
PCB transmission lines and connectors

Microstrip, coplanar waveguide (CPWG), and stripline
RF connector launches (SMA, U.FL)
PCB materials for RF


Below each section header is also a table detailing circuits, usefulness, and when to use. Each entry gets exactly one row, in the order it appears in the chapter, and one verdict:

Default: The usual choice for that job, use unless there are unique constrains.
Good: A solid choice depending on the situation.
Niche: Only for a specific case, nice to know, might never use.
Know it: Often times an outdated circuit, but one that is useful for theory and interviews.
Avoid: Bad, don't make the same mistakes as me.
Always: Every board needs itm this one is mostly for board level design and usually one or two components.
Reference: Not a circuit, usually a guide or process for design.

As this project stand for more time, it will be periodically updated with LTspice simulations and similar implementations to act as a further guide to the reader. 
In addition, I will take time to parse through the application notes and/or textbook chapters that I have found particularly useful and slowly integrate them into (Useful Referances)[Useful References].