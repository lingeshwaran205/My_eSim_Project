Project Title: Design and Simulation of a 4-Stage Dickson Charge Pump using eSim

Short Description:
This project presents the design and simulation of a 4-Stage Dickson Charge Pump using eSim, an open-source EDA tool based on KiCad and NgSpice.
The Dickson Charge Pump is a voltage multiplier that converts a low DC or AC input into a higher DC output using only diodes and capacitors, driven by clock pulses. It eliminates the need for inductors and is widely used in on-chip voltage boosters, EEPROM/Flash programming circuits, and low-power DC–DC converters.

Objective:
To design and simulate a 4-stage Dickson Charge Pump capable of stepping up an input voltage of approximately 3.4674 V (rms) to an output voltage of around 12.663 V (rms) using eSim.

Software / Tools Used:

eSim (KiCad + NgSpice) – for schematic design and simulation

NgSpice – for transient and steady-state analysis

KiCad component libraries – for diode and capacitor modeling

Circuit Description:
The circuit consists of four pumping capacitors and four diodes connected in a cascaded arrangement. Each stage transfers charge during alternate clock cycles. When the clock toggles, the capacitors charge and discharge sequentially through the diodes, stacking the voltage at each node.
For a 4-stage configuration, the theoretical output can be estimated by:
Vout ≈ Vin + (n × Vclk) – (n × Vd)
where n = 4, Vclk is the clock amplitude, and Vd is the diode drop.

Measured Simulation Results:

Input Voltage (RMS): 3.4674 V

Output Voltage (RMS): 12.663 V

Voltage Gain: ≈ 3.65×
The simulation verifies that the Dickson Charge Pump successfully multiplies the input voltage through four charge-transfer stages.

How to Run / Reproduce:

Open the schematic file dickson_charge_pump_4stage.sch in eSim.

Ensure the input source and clock parameters match the given conditions.

Run the NgSpice simulation to view the transient response.

Measure RMS voltage values at input and output nodes.

Compare results with theoretical predictions.

Repository Contents:

schematic/ – eSim schematic files

netlist/ – NgSpice netlist file

simulation_results/ – Output waveforms and measurements

eSimReport.pdf – Detailed report with analysis

LICENSE – GPL v3 license file

Applications:

On-chip voltage boosters

Flash memory and EEPROM programming

Sensor bias generation and low-power charge-pump circuits
