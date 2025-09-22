# Hydrophone Acoustic Acquisition Project (Preliminary Phase)

## Overview
This project aims to acquire underwater acoustic signals using the AS-1 hydrophone. 
The current focus is on **analog circuitry design**: amplifying, cleaning, and filtering 
the hydrophone output to prepare it for ADC conversion. FPGA processing will be done in a later phase.

**Current Phase:** Initial understanding and planning of analog front-end circuitry.

## System Block Diagram (Preliminary)
AS-1 Hydrophone → Protection → Low-Noise Amplifier (LNA, preliminary) → Filter (high/low/band-pass, preliminary) → ADC → FPGA (future)

## Two-Week Goals
- Study AS-1 hydrophone datasheet: output voltage, impedance, frequency response
- Learn basic op-amp circuits (inverting, non-inverting) and RC filter concepts
- Draw a preliminary **system block diagram**
- Identify **key design constraints and considerations**, such as:
  - Hydrophone signal range
  - Gain range for LNA
  - Filter frequency bands
  - Avoid ADC saturation
- Prepare a short report/presentation summarizing the understanding and plan

## Two-Week Preliminary Milestones

| Week | Tasks | Deliverables |
|------|-------|-------------|
| Week 1 (22/09-28/09)| - Read AS-1 hydrophone datasheet<br>- Note output voltage range, impedance, frequency response<br>- Understand basic signal chain (Hydrophone → LNA → Filter → ADC) | - Datasheet summary table<br>- Notes on signal characteristics and key parameters |
| Week 2 (29/09-05/10)| - Learn basic op-amp circuits (inverting, non-inverting)<br>- Learn basic RC filter concepts (high-pass, low-pass, band-pass)<br>- Draw preliminary system block diagram<br>- Identify key design constraints (gain range, filter bands, ADC input limits, noise considerations) | - Preliminary system block diagram (hand-drawn or digital)<br>- List of design constraints and assumptions<br>- Short report summarizing understanding and plan for analog front-end |

## Expected Outcomes
- Clear understanding of the signal chain from hydrophone to ADC
- Preliminary choices for LNA topology and filter type
- Documentation of assumptions and design considerations for next phase
