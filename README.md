# 🔋 Design and Simulation of a 4-Stage Dickson Charge Pump using eSim

## 📘 Short Description
This project presents the **design and simulation of a 4-Stage Dickson Charge Pump** using **eSim**, an open-source EDA tool based on **KiCad** and **NgSpice**.  
The Dickson Charge Pump is a **voltage multiplier** that converts a low DC or AC input into a higher DC output using only diodes and capacitors, driven by clock pulses.  
It eliminates the need for inductors and is widely used in:
- On-chip voltage boosters  
- EEPROM/Flash programming circuits  
- Low-power DC–DC converters  

---

## 🎯 Objective
To design and simulate a **4-stage Dickson Charge Pump** capable of stepping up an input voltage of approximately **3.4674 V (RMS)** to an output voltage of around **12.663 V (RMS)** using **eSim**.

---

## 🧰 Software / Tools Used
- **eSim (KiCad + NgSpice)** – for schematic design and simulation  
- **NgSpice** – for transient and steady-state analysis  
- **KiCad component libraries** – for diode and capacitor modeling  

---

## ⚙️ Circuit Description
The circuit consists of **four pumping capacitors** and **four diodes** connected in a cascaded arrangement.  
Each stage transfers charge during alternate clock cycles.  
When the clock toggles, the capacitors charge and discharge sequentially through the diodes, stacking voltage at each node.

For a 4-stage configuration, the theoretical output can be estimated by:

\[
V_{out} \approx V_{in} + (n \times V_{clk}) - (n \times V_d)
\]
where  
- \( n = 4 \)  
- \( V_{clk} \) is the clock amplitude  
- \( V_d \) is the diode forward voltage drop  

---

## 📊 Measured Simulation Results
| Parameter | Value |
|------------|--------|
| **Input Voltage (RMS)** | 3.4674 V |
| **Output Voltage (RMS)** | 12.663 V |
| **Voltage Gain** | ≈ 3.65× |

✅ The simulation verifies that the Dickson Charge Pump successfully multiplies the input voltage through four charge-transfer stages.

---

## 🧪 How to Run / Reproduce
1. Download and unzip **`esimproject.zip`**.  
2. Open the schematic file **`dickson_charge_pump_4stage.sch`** in **eSim**.  
3. Ensure the input source and clock parameters match the given conditions.  
4. Run the **NgSpice simulation** to view the transient response.  
5. Measure RMS voltage values at input and output nodes.  
6. Compare results with theoretical predictions.

---

## 📁 Repository Contents
| File | Description |
|------|-------------|
| **LICENSE** | GPL v3 license file |
| **README.md** | Project description and instructions |
| **eSimReport.pdf** | Detailed project report with circuit, results, and conclusions |
| **esimproject.zip** | Compressed project files (schematic, netlist, simulations, etc.) |

---

## ⚡ Applications
- On-chip voltage boosters  
- Flash memory and EEPROM programming circuits  
- Sensor bias generation  
- Low-power charge-pump circuits  

---

## 🧾 Contributor
**Lingeshwaran**  
Project: *Design and Simulation of a 4-Stage Dickson Charge Pump using eSim*  

