# Antimicrobial resistance and pollutants: interactive studies and novel sensor technologies

## Executive snapshot
- Investigation of a low-cost carbon-electrode electrochemical sensor (SPCE on LTCC) for detecting antimicrobial resistance (AMR) genes, aiming to support point-of-care diagnostics and environmental monitoring of AMR.
- Development and functionalization workflow includes PNA immobilization, ssDNA targets (complementary CT and non-complementary NCT), and electrochemical impedance spectroscopy (EIS) to monitor binding via changes in charge transfer resistance (R_CT).
- Key performance signal: R_CT increases with CT concentration; NCT shows minimal changes, enabling discrimination between target and non-target DNA.
- Report provides detailed fabrication, functionalization, measurement protocols, data labeling formats, and a dataset of R_CT versus CT/NCT concentrations and incubation times, with initial limits of detection (LOD) and correlations.
- Future directions focus on multiplexing, readout stability, microfluidics, and multi-working-electrode sensor designs to scale monitoring capability.

## Data and metadata management
- Primary measurement: R_CT (in MΩ) from electrochemical impedance spectroscopy (EIS) using Autolab PGSTAT12, controlled by Nova software; Nyquist plots used to extract R_CT via a Randles-equivalent circuit.
- Experimental variables tracked:
  - Target type: CT (complementary) vs NCT (non-complementary) vs no DNA
  - Target concentration: ranges up to 20 μM with finer points (e.g., 0.25–2.5–5–10–20 μM)
  - Incubation time: 0, 30, 52 minutes (52 min is a standard readout after incubation)
  - Buffer conditions: 1 mM KCl + 2 mM ferri/ferrocyanide in EIS buffer
- Data labeling and traceability:
  - File naming convention: A_B_C_D_E_.jpeg, where
    - A = date in ddmmyy (e.g., 160721)
    - B = Experiment number (e.g., EX02)
    - C = Target Type (CT or NCT)
    - D = DNA concentration in μM
    - E = Incubation time in seconds
  - Example: 160721_EX02_CT_20_30 indicates a 20 μM CT target read after 30 minutes in the second experiment.
- Data scope:
  - Appendix 9 contains compiled R_CT values for multiple experiments, showing the relationship between R_CT, CT concentration, and incubation time, including discrimination between CT and NCT.
  - Relationships quantified via Pearson correlation (e.g., r = 0.810, p < .001) for CT concentration versus R_CT.
- Data provenance and protocols:
  - Detailed methodologies for SPCE fabrication, PNA functionalization, and EIS measurements are provided (Appendices 1–7), ensuring reproducibility and auditability.
  - Measurements include comparisons of CT vs NCT responses and baseline/no-target conditions.

## Data generation, quality, and governance
- Quality assurance and standardization:
  - Use of standardized electrochemical measurement protocols (Nyquist plots, R_CT extraction, Randles circuit) and consistent incubation times to enable comparability across experiments.
  - Inclusion of negative controls (NCT and no-target) to validate specific CT responses.
- Metadata richness and transparency:
  - Comprehensive appendices with step-by-step fabrication (Appendix 1), surface chemistry (PNA functionalization in Appendix 3–4), sensor activation (Appendix 3), and target preparation (Appendix 4–7) support data interpretation and auditing.
  - File-naming and experimental metadata enhance traceability for monitoring frameworks.
- Potential data governance considerations:
  - The document emphasizes public sharing of underlying data and datasets as a governance goal, but explicit policies on public data repositories or licenses are not detailed; however, the extensive appendices provide a strong basis for data reuse.
  - Data completeness is high for experimental conditions and outcomes; raw data sharing policies would benefit from formalized governance to align with monitoring frameworks.

## Key findings relevant to monitoring frameworks
- Discrimination capability:
  - CT targets produce significant increases in R_CT over CT-free baselines and NCT controls, enabling reliable detection of AMR gene presence at given concentrations.
- Quantitative relationship:
  - Clear positive correlation between CT concentration and R_CT (e.g., r = 0.810), indicating potential for quantitative interpretation of AMR signal strength.
- Sensitivity and detection limits:
  - LOD identified around 500 nM for the OXA-1 gene CT in this platform, with detectable R_CT changes observed at higher CT concentrations.
  - Sensitivity improves with incubation time (R_CT increases over 0, 30, 52 minutes), informing timing considerations for environmental monitoring workflows.
- Data breadth and repeatability:
  - Multiple experiments across different dates demonstrate repeatable CT vs NCT discrimination and concentration-dependent responses.
- Practical outputs for monitoring:
  - Feasibility of integrating carbon SPCE-based AMR sensors into monitoring frameworks for environmental health surveillance and policy evaluation, with potential for dashboards or reports summarizing R_CT versus CT concentration and time.

## Recommendations for monitoring frameworks
- Standardize data schemas and metadata:
  - Adopt the file-naming convention and capture CT/NCT status, concentrations, incubation times, and R_CT values to enable cross-study comparability.
- Ensure data governance and openness:
  - Publish underlying data and protocols in accessible repositories with clear licensing to support replication and comparative monitoring across jurisdictions.
- Extend data infrastructure:
  - Develop multiplexed and multi-working-electrode readouts to broaden sensor coverage while reducing system size, aligned with future work.
- Integrate with decision-making tools:
  - Translate R_CT versus CT concentration into actionable indicators for environmental AMR risk, with dashboards that track detection thresholds and time-to-detection.
- Plan for scale and sustainability:
  - Pursue microfluidic multiplexers and multi-WE sensor arrays to enable scalable environmental monitoring and policy evaluation.

## Future work and alignment with monitoring goals
- Complete readout multiplexing system and assess stability and accuracy for broader deployment.
- Design microfluidic multiplexer to enable simultaneous readings from multiple sensors.
- Develop multi-working-electrode (WE) sensor architectures to reduce overall readout system size and enhance scalability.
- These directions support broader environmental monitoring capabilities and more comprehensive policy evaluation through sensor networks.

## Appendixal methods (summary)
- Sensor fabrication: LTCC-based SPCE sensors prepared via laser cutting, silver electrode printing, lamination, hydrostatic pressing, sintering, and final carbon/dielectric layer processing.
- PNA functionalization: Involves electrode pre-treatment, in-situ diazonium salt formation, AP film deposition, EDC/NHS activation, PNA immobilization, and blocking with ethanolamine.
- Target preparation and EIS measurement: CT/NCT targets prepared as ssDNA, incubation on sensor, EIS data collection, and Nyquist-plot-based R_CT extraction.
- Data formats and checklists: Appendices include detailed process checklists, labeling schemes, and data recording formats to support consistent monitoring outputs.