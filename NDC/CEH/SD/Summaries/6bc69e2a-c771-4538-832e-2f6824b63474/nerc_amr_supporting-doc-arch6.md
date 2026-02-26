# Functionalisation data, materials, and method statements of a carbon electrode biosensor for detection of antimicrobial resistance

- Scope: handover notes from Heriot-Watt University for a low-cost carbon electrode electrochemical sensor on LTCC SPCEs aimed at detecting AMR genes, focusing on PNA-based functionalisation and EIS readouts (R_CT) for nucleic acid targets like OXA-1.
- Context: AMR represents a major global health and economic threat; goal is point-of-care diagnostics to enable rapid AMR gene detection with self-serve data outputs.

## Sensor design and fabrication (high level)

- Platform: Electrochemical biosensor using screen-printed carbon electrodes on a low-temperature co-fired ceramic (LTCC) substrate.
- Fabrication workflow: Laser cutting of LTCC, screen-printing silver and carbon layers, multi-layer stacking, hydrostatic pressurization, sintering, dicing into sensors.
- Output: A low-cost, LTCC SPCE sensor suitable for molecular detection of nucleic acids.

## Chemistry and biorecognition components

- Target and controls:
  - Complementary DNA target (CT) for positive control.
  - Non-complementary DNA target (NCT) as negative control.
  - Positive control uses OXA-1 gene sequence; two ssDNA targets specified for CT and NCT.
- Biorecognition elements:
  - Peptide Nucleic Acid (PNA) probe immobilised on the carbon electrode to capture target DNA.
  - OXA-1 DNA sequence provided; complementary and non-complementary targets defined.
- Surface chemistry workflow:
  - PNA immobilisation is preceded by surface activation and coupling chemistry (EDC/NHS in MES buffer) after deposition of a 4-carboxyphenyl (AP) film.
  - Blocking step with ethanolamine/PBS to suppress non-specific binding.

## Functionalisation and sensor preparation protocol (key steps)

- Pre-treatment: Chronoamperometric cleaning of electrodes in saturated Na2CO3 solution.
- In-situ diazonium formation: Generate 4-carboxyphenyl diazonium in situ from 4-aminobenzoic acid, sodium nitrite, and HCl; prepare under cold conditions.
- Electrodeposition: Form a 4-carboxyphenyl film on SPCE by cyclic voltammetry (±0.4 to -0.6 V).
- Activation: 60-minute incubation in MES buffer containing EDC and NHS to activate carboxyl groups.
- PNA immobilisation: Incubate amino-modified PNA probe on the activated electrode surface.
- Blocking: 30-minute incubation with ethanolamine/PBS to prevent non-specific binding.
- Target exposure: 52-minute incubation with CT or NCT targets in EIS buffer prior to measurement.

## Measurement methodology (EIS)

- Instrumentation: Autolab PGSTAT12 (Nova software) for Electrochemical Impedance Spectroscopy.
- Measurement conditions:
  - EIS buffer comprised of PBS with ferri/ferrocyanide redox couple (1 mM K3[Fe(CN)6]/K4[Fe(CN)6], 1 mM KCl; pH 7.4).
  - Incubation with target DNA (CT or NCT) followed by EIS readouts.
  - Nyquist plots used to extract charge transfer resistance (R_CT) from the equivalent circuit.
- Data handling: R_CT is tracked as a function of incubation time (0, 30, 52 minutes) and target concentration; comparisons CT vs NCT demonstrate specificity.

## Data and results (core findings)

- Relationship between R_CT and CT concentration:
  - Strong positive correlation between CT concentration and R_CT (Pearson r = 0.810, p < 0.001; n = 19).
  - Higher CT concentrations yield higher R_CT values, as shown in Nyquist plots and R_CT versus concentration graphs.
- Time dependence:
  - R_CT increases with longer incubation; 52 minutes generally yields larger R_CT than 0 or 30 minutes for CT.
- CT vs NCT discrimination:
  - CT produces substantially larger increases in R_CT compared with NCT at corresponding incubation times and concentrations; NCT results show only modest changes.
  - This demonstrates specificity of PNA-functionalised SPCE for complementary targets.
- Limit of detection (LOD):
  - LOD for the HW SPCE AMR sensor identified at around 500 nM CT (OXA-1 gene) in the tested dataset; concentrations below this show R_CT similar to controls (NCT or no DNA).
- Data organization:
  - Data are recorded with descriptive filenames and a defined schema:
    - File name format: A_B_C_D_E_.jpeg
    - A = date (ddmmyy), B = experiment number, C = CT or NCT, D = DNA concentration (μM), E = incubation time (seconds).
  - Example: 160721_EX02_CT_20_30 indicates 16/07/2021, Experiment 02, CT target at 20 μM, 30 seconds incubation readout.
- Appendices and datasets:
  - Appendix 9 collects change in R_CT across multiple CT/NCT experiments, concentrations, and incubation times (EX01–EX06, EX03, EX04, EX05, etc.), including 0–52 minute incubations and a range of CT concentrations (0.25–20 μM) and NCT controls.
  - Data include R_CT values in megaohms (MΩ) with corresponding experiment identifiers.

## Data management and quality practices

- Data provenance and traceability:
  - Clear labeling scheme for files and experiments; explicit CT/NCT designation, concentrations, and incubation times.
  - Experimental series documented across multiple days with downstream data in Appendix 9.
- Data analysis tools:
  - Pearson correlation (SPSS) used to quantify R_CT versus CT concentration.
  - Nyquist plots and R_CT extraction guided by referenced equivalent circuits and prior literature.
- Checklists and appendices:
  - Appendices provide detailed protocols for fabrication, functionalisation, EIS measurements, and readiness checklists (Appendix 8).

## Data products and potential uses

- Readouts and dashboards:
  - R_CT values and CT concentration relationships can be turned into simple dashboards or pivoted views for end users to assess target presence and concentration levels.
- Validation and reproducibility:
  - Negative controls (NCT and no DNA) included to validate specificity and reduce false positives.
- Future data products:
  - Sensor readout multiplexing, stability assessments, microfluidic multiplexers, and multi-working-electrode sensor arrays planned for more scalable data outputs.

## Future work (as identified)

- Complete readout multiplexing system and assess stability/accuracy.
- Design a microfluidic multiplexer for simultaneous reads from multiple sensors.
- Develop a multi-working-electrode sensor to reduce overall readout system size.