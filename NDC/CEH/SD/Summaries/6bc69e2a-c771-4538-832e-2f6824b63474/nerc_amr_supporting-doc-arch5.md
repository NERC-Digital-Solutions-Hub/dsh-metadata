# Functionalisation data, materials, and method statements of a carbon electrode biosensor for detection of antimicrobial resistance

## Overview and purpose
- Describes handover notes and results from Heriot-Watt University for functionalising a carbon electrode electrochemical sensor to detect antimicrobial resistance (AMR) genes.
- Long-term goal: enable low-cost, point-of-care AMR diagnostics using SPCEs on LTCC substrates; measure charge transfer resistance (R_CT) via electrochemical impedance spectroscopy (EIS).

## Data assets and types
- Sensor fabrication data: LTCC stack construction, screen-printed silver/carbon layers, sintering, dicing (Appendix 1).
- Functionalisation data: PNA immobilisation, AP (4-carboxyphenyl) diazonium film, EDC/NHS activation, blocking with ethanolamine (Appendix 3).
- Biorecognition elements: OXA-1 DNA targets (complementary CT and non-complementary NCT), ssDNA controls, amino-modified PNA probes (Appendix 2, 3).
- Electrochemical data: R_CT measurements, Nyquist plots, equivalent circuit modeling; EIS buffers and target incubation details (Section 2.4; Figures 4–5, 6–8).
- File naming conventions and identifiers: A_B_C_D_E_.jpeg format capturing date, experiment number, target type, DNA concentration, incubation time (Section 2.1).
- Dataset in Appendix 9: Change in R_CT vs target concentration and incubation time across multiple experiments (EX01–EX06; NCT/CT; various concentrations and times).

## Data collection and provenance
- Fabrication protocol: LTCC assembly, screen printing, curing, vacuum packing, isostatic pressing, sintering, and patterning steps (Appendix 1).
- Functionalisation workflow (A–Z): pre-treatment, in-situ diazonium formation, electrodeposition of 4-carboxyphenyl film, surface activation, PNA immobilization, and blocking (Appendix 3; Step 1–6).
- PNA/DNA hybridisation and measurement: incubation with target DNA, EIS measurements across a frequency range, and comparisons between CT and NCT (Section 1.5; Figure 4; 2.3).
- Measurement tooling: Autolab PGSTAT12/PGSTAT204 with Nova software; Randles-equivalent circuit fitting to extract R_CT (Section 1.5; Appendix 9).
- Documentation and traceability: unique database serials (Appendix 9), date-stamped experiment IDs, and explicit conventions for file naming (Section 2.1).

## Metadata, data schema, and standards
- Metadata fields for data records: unique ID, Date, Experiment Number, Target Type (CT/NCT), DNA Concentration (μM), Incubation Time (s), and R_CT (MΩ) (Appendix 9).
- Data interpretation rules: R_CT increases with incubation time and with CT concentration; CT produces markedly larger R_CT changes than NCT (Section 2.2, 2.3).
- Data relationships: R_CT vs CT concentration shows a strong positive correlation (Pearson r = 0.810, p < 0.001) across 19 measurements in Table 1 of Appendix 9 (Section 2.4).
- LOD determination: significant R_CT change observed starting at 500 nM OXA-1 CT (Section 2.4; Figure 11).

## Data storage, sharing, and governance
- Data organization: results and figures referenced by labeled experiment identifiers; images stored with descriptive A_B_C_D_E_ filenames (Section 2.1).
- Documentation reuse: appendices provide full protocols (Appendices 1–7) and checklists (Appendix 8) to support reproducibility and auditing.
- Data stewardship considerations: multi-step fabrication and functionalisation processes across different equipment (Autolab, LTCC, SPCE) highlight the need for standardized metadata, versioned protocols, and clear data provenance to enable discoverability and reuse.

## Data quality, validation, and limitations
- Validation approaches: comparison of CT vs NCT responses; repeated experiments; correlation analysis for R_CT vs target concentration.
- Observed trends: longer incubation yields higher R_CT; CT targets produce larger R_CT increases than NCT; LOD around 500 nM for CT-OXA-1.
- Limitations and challenges noted: incomplete capture of user needs and priorities, integration across different systems and formats, and potential data transfer considerations for large datasets (Data Stewards challenges).

## Data lifecycle and maintenance
- Data generation lifecycle: fabrication → functionalisation → probe immobilisation → target incubation → EIS measurement → data analysis (R_CT extraction) → reporting/archiving.
- Update and versioning: clearly documented experiment numbers, dates, and CT/NCT targets; file naming encodes key experiment parameters for traceability.
- Future work hints: readout multiplexing, system stability/accuracy, microfluidic multiplexer, and multi-working-electrode sensor designs (Section 3).

## Practical takeaways for Data Stewards
- Enforce consistent metadata: ensure all datasets include date, experiment number, target type, concentration, incubation time, and R_CT.
- Preserve provenance: maintain alignment between fabrication/functionalisation steps and resulting measurements; link Appendices 1–7 to corresponding data records.
- Support discoverability: maintain standardized file naming (A_B_C_D_E_.jpeg) and keep a master index mapping identifiers to experimental conditions and results.
- Plan for interoperability: the use of multiple instruments and protocols necessitates harmonized data schemas and clear documentation to enable cross-study reuse.
- Capture data quality signals: store CT vs NCT comparisons, replication counts, correlation metrics, and LOD determinations alongside primary measurements.