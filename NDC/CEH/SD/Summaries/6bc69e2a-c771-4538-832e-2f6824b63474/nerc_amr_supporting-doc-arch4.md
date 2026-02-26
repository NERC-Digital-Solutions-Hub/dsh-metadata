# Antimicrobial resistance and pollutants: interactive studies and novel sensor technologies

- Overview and objective
  - Develop low-cost, point-of-care AMR sensing platforms using carbon electrode SPCEs on LTCC substrates.
  - Detect AMR genes via PNA-DNA hybridization with electrochemical impedance spectroscopy (EIS) to measure Charge Transfer Resistance (R_CT).
  - Use Nyquist plots and Randles circuit fitting to quantify R_CT as a readout of target binding.

- Data types, structure, and formats
  - Experimental measurements: R_CT values (in MΩ) at multiple incubation times (e.g., 0, 30, 52 minutes) for complementary targets (CT) and non-complementary targets (NCT).
  - Metadata schema (as per Appendix 9 and data notes):
    - Date, Experiment Number (EX01, EX02, etc.), Target Type (CT or NCT), Target Concentration (μM), Incubation Time (seconds/minutes), R_CT values.
  - File naming and data traceability:
    - File name format: A_B_C_D_E_.jpeg
    - A = date (ddmmyy), B = Experiment No., C = DNA Type (CT or NCT), D = DNA concentration (μM), E = incubation time (seconds).
    - Example: 160721_EX02_CT_20_30 corresponds to 16/07/2021, experiment EX02, CT target, 20 μM, 30 s incubation.
  - Data analysis approach:
    - EIS measurements controlled by Autolab Nova software; R_CT extracted from Nyquist plots using a Randles circuit.
    - Comparative analysis of CT vs NCT to establish specificity; linear relationships between CT concentration and R_CT reported (Pearson correlation r = 0.810).

- Methods and data capture
  - Sensor fabrication and functionalization data (Appendices 1–6) inform data provenance (LTCC SPCE sensors, silver/carbon layers, PNA immobilization, blocking steps).
  - PNA functionalization and DNA hybridization procedures generate the primary data inputs for R_CT changes.
  - EIS readouts captured in buffer conditions with defined redox couple (KCl ferri/ferrocyanide) and 1 mM KCl; Nyquist plots used to determine R_CT.

- Key data findings and indicators
  - CT vs NCT: CT targets produce notable increases in R_CT over incubation time; NCT shows much smaller changes, supporting assay specificity.
  - Concentration effect: higher CT concentrations yield larger R_CT values; strong positive correlation with CT concentration (r = 0.810, p < 0.001).
  - Limit of detection: approximately 500 nM for the OXA-1 gene CT in this system (Figure 11 reference).
  - Temporal dynamics: longer incubation (up to ~52 minutes) enhances the R_CT signal for CT.

- Data governance, provenance, and documentation
  - Appendices provide comprehensive protocols, sequences, primers, and probe information (e.g., OXA-1 DNA sequences, Forward/Reverse primers, OXA-1 ssDNA targets, PNA probe).
  - Process and chemical checklists (Appendix 8) support reproducibility and audit trails.
  - Sensor assembly and functionalization procedures (Appendix 3, 4, 5) detail reagent preparation and instrumentation requirements.
  - Equipment and connectivity notes (Appendix 6) describe Autolab wiring and electrode mapping for data integrity.

- Challenges and considerations for Data Leaders
  - Data fragmentation and standardization: diverse appendices and protocols necessitate a unified data model and metadata standard for easier integration and reproducibility.
  Data quality and comparability: variability in reagents, buffers, and incubation parameters across experiments; need for consistent metadata capture (date, experiment, target type, concentration, incubation, and R_CT).
  Data disclosure and sharing: rich methodological detail supports reproducibility but requires careful governance for sharing alongside raw R_CT results and spectral plots.
  Scalability and future data architecture: current work anticipates multiplexing and multi-work electrode (WE) sensors; future data systems should support multiplexed readouts and microfluidic integration (as outlined in Future Works).

- Future Work and data-related roadmap
  - Complete and validate a readout multiplexing system and assess stability/accuracy.
  - Design a microfluidic multiplexer to enable parallel readings from multiple sensors.
  - Develop a multi-WE sensor approach to reduce readout system size and improve scalability.
  - Leverage the rich Appendix data (protocols, sequences, file naming, and experiment identifiers) to build a standardized data schema for AMR sensing datasets and enable broader data sharing within the community.