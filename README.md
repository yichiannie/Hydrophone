# Acoustic Communication Front-End: Hydrophone → LNA → Filter → ADC → FPGA

## 1. Project Overview
This project aims to design a **custom analog front-end** for the AS-1 hydrophone, replacing the off-the-shelf pre-amplifier, to acquire clean underwater acoustic signals and feed them to an FPGA for digital processing.

**Current Scope (Phase 1):**
- Analog circuitry design:
  - Low Noise Amplifier (LNA)  
  - Filtering (High-Pass, Low-Pass, Anti-Aliasing)  
  - ADC interface for FPGA  

**Goal:**  
Build a functional and well-characterized analog front-end for underwater pinger localization experiments.

---

## 2. High-Level Block Diagram


---

## 3. Progress Thus Far
- **High-Level Block Diagram:** Completed (system overview)
- **Analog Knowledge Learning:**  
  - Learned how op-amps operate at the analog level  
  - Studied methods to filter high- and low-frequency noise using RC circuits and other filter topologies  
  - Gained understanding of gain, bandwidth, and noise considerations in analog front-end design

- **AS-1 Hydrophone Data Understanding:**  
  - Analyzed the AS-1 hydrophone output characteristics (~40 µV/Pa)  
  - Studied signal type, impedance, and frequency range  
  - Identified key constraints for amplification and filtering stages

- **LNA Circuit in LTSpice:** Currently in design and simulation  
  - Initial schematic drawn
    <img width="2191" height="1477" alt="image" src="https://github.com/user-attachments/assets/3faf77ee-68db-42a7-be5e-df89d8c7d17b" />

  - Simulation issues: LNA current signal is not properly transmitted; output current amplitude too low to drive subsequent stages
    <img width="2850" height="649" alt="image" src="https://github.com/user-attachments/assets/5a945a8e-4357-4fb3-904a-fc1da53fea51" />

  - Planning improvements: adjust feedback network, optimize biasing, and consider output buffer stage

- **Filter Stage Planning:**  
  - Identified high-pass, low-pass, band-pass, and anti-aliasing filters as necessary  
  - Started preliminary design considerations for cutoff frequencies and component selection

---

## 4. Challenges Encountered
1. **LNA Current Signal Issue**  
   - Problem: Current signal cannot be properly transmitted; output current amplitude too low  
   - Possible causes and solutions:  
     - Input impedance mismatch with hydrophone model  
     - Improper amplifier feedback or biasing  
     - Inaccurate LTSpice model parameters  
     - Potential fixes: adjust feedback network, add output buffer/driver stage, tune biasing

2. **Hydrophone Signal Characteristics**  
   - Extremely small signal (~40 µV/Pa) is highly sensitive to noise  
   - Requires low-noise components and careful PCB design to minimize parasitics  

3. **ADC & FPGA Interface**  
   - Ensure anti-aliasing and proper signal amplitude  
   - Multi-channel synchronization may be challenging in future phases  

---

## 5. Next Steps
- Refine **LNA circuit in LTSpice** to resolve current transmission issue  
- Design and simulate **filter stage**  
- Define **ADC interface specification** for FPGA input  
- Record simulation results and update block diagram if necessary
