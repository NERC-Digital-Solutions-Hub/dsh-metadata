# Functionalisation data, materials, and method statements of a carbon electrode biosensor for detection of antimicrobial resistance

- Overview
  - Addresses antimicrobial resistance (AMR) as a global threat and presents a low-cost electrochemical sensor platform to detect AMR genes, using carbon-SPCE on LTCC substrates.
  - Focuses on functionalising electrodes, immobilising PNA probes, and detecting target DNA via electrochemical impedance spectroscopy (EIS) to measure the charge-transfer resistance (R_CT).

- Data types and structure
  - Manufacturing, functionalisation, and measurement data across multiple steps, with explicit protocols and parameters (Appendices 1–9).
  - Primary measurement data: R_CT values from EIS as a function of target type (complementary CT vs non-complementary NCT), DNA concentration, and incubation time.
  - Appendix 9 contains a structured dataset of experiments (identifiers EX01–EX06, CT/NCT, DNA concentrations, incubation times, and R_CT in MΩ), plus corresponding dates and labels.
  - File naming conventions for experimental data: A_B_C_D_E_.jpeg, encoding date, experiment number, target type, DNA concentration, and incubation time.

- Sensor fabrication and material statements
  - Sensor architecture: electrochemical biosensor based on screen-printed carbon electrodes (SPCE) on LTCC substrate; fabrication steps include laser-cut LTCC, screen printing of silver electrodes, carbon/dielectric layers, sintering, dicing, and cleanroom handling (Appendix 1).
  - Materials inventory and equipment are detailed in Appendix 6, including Autolab instruments, screenprinters, LTCC, silver paste, and ceramic/substrate materials.

- Functionalisation and surface chemistry
  - PNA-based functionalisation: immobilisation of amino-modified PNA probes on carbon electrodes to detect the OXA-1 AMR gene (Appendix 2; 1.4 PNA functionalisation describes steps from electrode cleaning to blocking).
  - Key steps in functionalisation (Appendix 3): pre-treatment, in-situ diazonium salt formation to form a 4-carboxyphenyl (AP) film via electrochemical deposition, activation with EDC/NHS in MES buffer, PNA immobilization, and blocking with ethanolamine.
  - Surface activation and coupling enable subsequent DNA hybridisation and EIS measurements (Appendix 3).

- DNA targets and sequences
  - Complementary (CT) and non-complementary (NCT) targets defined; OXA-1 DNA sequences and PNA probe details provided (Appendix 2).
  - Probes and targets used for validation: OXA-1 CT vs NCT, with specific target sequences and control oligos (Appendix 2).

- Hybridisation and measurements
  - EIS measurements performed with Autolab PGSTAT12 (Nova software) to extract R_CT from Nyquist plots; incubation times assessed at 0, 30, and 52 minutes after target exposure (Figure references in the text).
  - Buffer conditions for EIS include 1 mM KCl with 2 mM ferri/ferrocyanide, and measurement in an EIS buffer; CT hybridisation elevates R_CT due to increased surface charge.
  - Nyquist plots and an equivalent circuit are used to derive R_CT (Appendix figures and discussion).

- Data formats, labeling, and metadata
  - File naming and labeling conventions for experiments (Appendix 2 and Section 2.1): A_B_C_D_E_.jpeg format, where A = date (ddmmyy), B = experiment number, C = CT or NCT, D = DNA concentration in μM, E = incubation time in seconds.
  - Data management and instrumentation details are supported by appendices outlining connector wiring (Appendix 6) and checklists (Appendix 8).

- Results and key findings
  - R_CT increases with CT concentration, showing a significant positive correlation (Pearson r = 0.810, p < 0.001) across measured data (Appendix 9 and accompanying Table 1).
  - Higher CT concentrations yield larger R_CT values; NCT targets produce smaller changes, enabling discrimination between CT and non-complementary targets (Appendix 9 and Figures 6–8).
  - Limit of detection (LOD) for the HW SPCE sensor with OXA-1 CT identified at 500 nM, based on notable R_CT increase relative to NCT/zero-target controls (Appendix 9 and Figure 11).

- Data quality, assurance, and analysis
  - Emphasis on early prototype testing, data verification, and iterative improvement throughout the functionalisation and measurement workflow (aligns with GIS-like emphasis on stakeholder feedback and data quality).
  - Correlation analyses and visualization via Nyquist plots and R_CT versus CT concentration support quantitative assessment of sensor performance (Appendix 9).

- Appendices and supporting material
  - Appendix 1: Detailed sensor fabrication steps and room equipment setup (LTCC stacking, sintering, printing sequences).
  - Appendix 2: OXA-1 DNA sequences, OXA-1 DNA template, primers, and target lists (CT/NCT).
  - Appendix 3: SPCE functionalisation protocol (pre-treatment, diazonium deposition, activation, PNA immobilisation, blocking).
  - Appendix 4–6: Data management details, Autolab connector wiring, and instrument setup.
  - Appendix 8: Checklists for chemical inventory and process steps to ensure protocol fidelity.
  - Appendix 9: Comprehensive results dataset for R_CT across multiple experiments, with identifiers, target types, concentrations, incubation times, and R_CT values.

- Future work
  - Complete readout multiplexing system and assess stability/accuracy.
  - Develop microfluidic multiplexer to enable multi-sensor readouts.
  - Design and implement multi-working-electrode sensors to reduce readout system size.

- References
  - Foundational sources on AMR threat assessment and prior SPCE-on-ceramic sensor work supporting the methodology and sensor architecture.

- Relevance to GIS Specialists
  - Data-centric: demonstrates end-to-end data handling for a sensor platform, including structured data capture, metadata conventions, and dataset organization suitable for map-based or spatially contextualized data products.
  - Data quality and integration: showcases the importance of consistent data standards, provenance, and clear labeling to enable integration with larger data ecosystems.
  - Iterative testing and proto-typing: emphasizes user-centered validation and feedback loops, aligning with GIS workflows that require reliable,Explorable data visuals and analyses.