# AS-1 Hydrophone Specifications

This document summarizes the AS-1 hydrophone specifications that are useful for designing the analog front-end (LNA + filters + ADC).

---

## 1. Signal Level & Sensitivity
- **Receiving Sensitivity:** -208 dBV re 1 μPa (~40 μV / Pa)  
  - Output signal is very weak; requires **high-gain, low-noise LNA**.
- **Maximum Input Voltage:** 30 V p-p (continuous); 150 V p-p (<10% duty cycle, <100 kHz)  
  - LNA input range and protection circuits should prevent saturation during strong signals.

---

## 2. Frequency Response
- **Linear Range:** 1 Hz – 100 kHz ±2 dB  
  - LNA and filters should cover this range.  
  - Design filter stage (HPF/LPF/BPF) to ensure ADC receives signals within effective frequency band.

---

## 3. Electrical Characteristics
- **Nominal Capacitance:** 5 nF ±15% (plus cable @ 118 pF/m)  
  - Use for **input impedance matching** and optimizing LNA performance.  
- **Output Connection:** BNC (standard)  
  - Convenient for PCB or test setup integration.

---

## 4. Mechanical & Environmental  
- **Cable Length:** 10 m standard, Polyurethane jacket (OD: 4.5 mm)  
  - Consider cable parasitics in LNA input design (capacitance and signal attenuation).

---

## 5. Recommended Usage for Analog Front-End Design
1. **LNA Modeling in LTSpice:**  
   - Model hydrophone as a **voltage source + 5 nF capacitance + cable parasitic capacitance**.
2. **Filter Design:**  
   - Design HPF and anti-aliasing filters based on target pinger frequency and ADC sampling rate.
3. **Protection Circuit:**  
   - Consider voltage-limiting or resistor network to prevent over-voltage at LNA input.
4. **PCB / Test Integration:**  
   - Use BNC output to connect directly to the analog front-end.

