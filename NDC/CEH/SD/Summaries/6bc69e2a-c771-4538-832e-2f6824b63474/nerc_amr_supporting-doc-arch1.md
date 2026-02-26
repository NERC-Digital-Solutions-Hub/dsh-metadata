# Functionalisation data, materials, and method statements of a carbon electrode biosensor for detection of antimicrobial resistance

## Overview and context
- Addresses antimicrobial resistance (AMR) as a major global threat; aims to develop low-cost, point-of-care AMR sensing platforms.
- The project reports handover notes and results from Heriot-Watt University on functionalising carbon electrode electrochemical sensors (LTCC-based SPCEs) for detection of AMR genes, notably using PNA probes to detect OXA-1.

## Sensor design, equipment, and data-generating approach
- Sensor: Electrochemical biosensor based on screen-printed carbon electrodes (SPCE) on a low-temperature co-fired ceramic (LTCC) substrate.
- Target and control DNAs: Complementary DNA target (CT) for OXA-1 gene and non-complementary DNA target (NCT) as control.
- Readout method: Electrochemical impedance spectroscopy (EIS) measuring charge transfer resistance (R_CT) as the primary signal reflecting hybridization of target DNA to immobilized PNA probes.
- Instrumentation: Autolab PGSTAT12 in conjunction with Nova software; Nyquist plots used to extract R_CT via the Randles-equivalent circuit.
- Data organization: Files are named with a specific convention A_B_C_D_E_.jpeg, encoding date, experiment number, target type (CT/NCT), DNA concentration, and incubation time (in seconds).

## Functionalisation and fabrication data (procedural focus)
- Fabrication flow (high level): LTCC sheet laser-cut, silver electrode patterning, multi-layer LTCC assembly, hydrostatic pressing, LTCC sintering, carbon and dielectric layer print, and dicing into sensors.
- PNA and DNA handling:
  - PNA immobilisation targets the OXA-1 gene sequence.
  - Positive control: complementary OXA-1 DNA target (CT); Negative control: non-complementary target (NCT).
  - Blocking step to reduce non-specific binding.
- Functionalisation steps (A–Z, time ~3 h 20 min total):
  - Pre-treatment: Chronoamperometric cleaning in saturated Na2CO3.
  - Electrodeposition: In-situ generation of 4-carboxyphenyl film via diazonium chemistry to form a functional coating on SPCEs.
  - Activation: Carboxyl groups activated with EDC/NHS in MES buffer (pH 5.0).
  - PNA immobilisation: Incubation of amino-modified PNA probe on the activated electrode.
  - Blocking: Ethanolamine/PBS blocking to minimize non-specific adsorption.
- PNA-DNA hybridisation and measurement:
  - Incubation with target DNA in EIS buffer followed by EIS measurement.
  - R_CT extracted from Nyquist plot; comparing R_CT before and after hybridization (with CT vs NCT) to gauge binding.
- Data and protocols: Appendices detail base materials, sequences (OXA-1 template, primers), SPCE functionalisation protocol (Appendices 1–5), connector/wiring (Appendix 6), checklists (Appendix 8), and full change-in-R_CT data (Appendix 9).

## Key results and data-driven findings
- General trend: R_CT increases with incubation time and with complementary target (CT) concentration, indicating stronger interfacial impedance upon successful CT hybridisation.
  - CT-specific time progression (example CT at 20 μM):
    - 0 min: R_CT ≈ 6.68 × 10^4 MΩ
    - 30 min: R_CT ≈ 3.95 × 10^5 MΩ
    - 52 min: R_CT ≈ 1.66 × 10^6 MΩ
  - CT vs NCT discrimination: CT produces substantially larger increases in R_CT than NCT, particularly evident after longer incubations (52 min).
    - Example NCT at 20 μM:
      - 0 min: R_CT ≈ 1.25 × 10^4 MΩ
      - 30 min: R_CT ≈ 1.18 × 10^4 MΩ
      - 52 min: R_CT ≈ 1.08 × 10^4 MΩ
- Concentration dependence (CT):
  - Strong positive correlation between CT concentration and R_CT (Pearson correlation ≈ 0.81, p < 0.001), indicating higher CT concentrations yield larger R_CT changes.
  - Representative trend (CT concentrations 0.25–20 μM) shows higher CT levels corresponding to higher R_CT on Nyquist plots.
- Limit of detection (LOD):
  - LOD for the HW SPCE sensor with OXA-1 CT was observed around 500 nM CT, where a significant R_CT change emerges relative to lower concentrations and NCT/no-target controls.
- Data scale and variability:
  - The Appendix 9 dataset contains extensive measurements across multiple experiments and time points, illustrating reproducibility patterns and the CT vs NCT discrimination across concentration ranges and incubation times (0, 30, 52 minutes).

## Data formats, labeling, and reproducibility
- File naming format: A_B_C_D_E_.jpeg
  - A = date (ddmmyy, e.g., 150721 for 15 July 2021)
  - B = Experiment No. (EX01, EX02, etc.)
  - C = Target Type (CT or NCT)
  - D = DNA concentration (μM)
  - E = Incubation time (seconds)
- Example: 160721_EX02_CT_20_30 denotes 16 July 2021, Experiment EX02, CT target at 20 μM, measured after 30 seconds incubation.
- Data provenance: Detailed appendices (Appendix 9) present the raw R_CT values and experimental identifiers to support traceability and re-analysis.

## Future work
- Complete the readout multiplexing system.
- Assess readout system stability and accuracy.
- Design a microfluidic multiplexer for multiple sensors.
- Develop a multi-work electrode (multi-WE) sensor approach to reduce readout system size.

## Appendices (content highlights)
- Appendix 1: Sensor fabrication steps (LTCC and SPCE construction).
- Appendix 2: OXA-1 DNA sequences and related targets.
- Appendix 3–5: SPCE functionalisation protocols (pre-treatment, diazonium-based film formation, activation, PNA functionalisation, blocking) with material lists and stepwise instructions.
- Appendix 6: Autolab connector wiring and electrode mapping details.
- Appendix 8: Checklists for chemicals and processes during SPCE functionalisation and EIS measurements.
- Appendix 9: Comprehensive dataset of R_CT values by identifier, date, experiment, target type, concentration, and incubation time, including CT and NCT cases across multiple runs.